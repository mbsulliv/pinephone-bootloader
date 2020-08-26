# ARM CPU: Allwinner A64

![Allwinner A64](https://linux-sunxi.org/images/5/5c/A64_SoC.jpg)

[This site](https://linux-sunxi.org/A64) gives lots of details on the ARM CPU in the PinePhone:

* [Datasheet](http://files.pine64.org/doc/datasheet/pine64/A64_Datasheet_V1.1.pdf) 
* [User Manual](http://files.pine64.org/doc/datasheet/pine64/Allwinner_A64_User_Manual_V1.0.pdf) 

From the datasheet:

* Quad-core ARM Cortex-A53 processor
* Power-efficient ARM v8 architecture
* 64-bit and 32-bit execution states for scalable high performance
* Trustzone technology supported
* Support for NEON advanced SIMD (Single Instruction Multiple Data) instruction for acceleration of media and signal processing functions
* Support for Large Physical Address Extensions (LPAE)
* VFPv4 floating point unit
* 32 Kbyte L1 instruction cache and 32 Kbyte L1 data cache
* 512 Kbyte L2 cache

The Cortex-A53 processor implements the ARMv8-A (application ('A') profile) architecture.  This includes:

* Support for both AArch32 and AArch64 execution states
* Support for all exceptions levels, EL0, EL1, EL2, and EL3, in each execution state
* The A32 instruction set (previously called the ARM instruction set)
* The T32 instruction set (previously called the Thumb instruction set)
* The A64 instruction set
* Branch target indicators which enforce that indirect branches only go to code locations where the instruction is one of a small acceptable list
* Pointer authentication code to ensure functions return to the location expected by the program
* Memory tagging to decrease the number of exploitable memory safety errors
* 64-bit virtual addressing to enable memory accesses beyond 4 Gbytes of physical memory
* Automatic event signaling to enable power-efficient, high-performance spinlocks
* Larger register file to provide thirty-one 64-bit general purpose registers
* Efficient 64-bit immediate generation, reducing the need for literal pools
* Large PC-relative addressing range of +/- 4 Gbytes
* Additional 16 Kbyte and 64 Kbyte translation granules to reduce Translation Lookaside Buffer (TLB) miss rates and depth of page walks
* Efficient cache management allowing user-space cache operations and fast clearing
* Load-Acquire, Store-Release instructions to improve performance of thread-safe code by eliminating explicit memory-barrier instructions
* Extensions:
  * ARMv8-A Extension: NEON double-precision floating-point single instructions multiple data (SIMD) to speed up data-centric operations
  * ARMv8-A Extension: Hardware-accelerated cryptography provides 3x to 10x better software encryption performance