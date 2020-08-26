# ARM Cortex-A53: Is it 32-bit or 64-bit on a cold reset?

According to table A-3 of the [ARM Cortex-A53 MPCore Processor Technical Reference Manual (revision r0p4)](https://static.docs.arm.com/ddi0500/f/DDI0500.pdf), the signals received on the **AA64nAA32** pins during a reset will determine what mode each CPU core boots into.

I went looking for those pins on both the [Allwinner A64 Datasheet (v1.1)](http://dl.linux-sunxi.org/A64/A64_Datasheet_V1.1.pdf) and the [PinePhone schematics (v1.2)](http://files.pine64.org/doc/PinePhone/PinePhone v1.2 Released Schematic.pdf) and they were nowhere to be found.  Hmmm. 🤔

I eventually did find a reference to them in section 3.4.5.1 of the [Allwinner A64 User Manual](http://files.pine64.org/doc/datasheet/pine64/Allwinner_A64_User_Manual_V1.0.pdf) (v1.0).  The Cluster Control Register0 (**C_CTRL_REG0**) is used to represent the AA64nAA32 signals on bits 27:24 instead of receiving them from external pins.  The register defaults those bits to 0x0, which will result in all the CPU cores starting in AArch32 mode.