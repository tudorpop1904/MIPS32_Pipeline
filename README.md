# MIPS32 Pipeline
# Brief Description

This project aims to implement an improved version of the MIPS32 Single Cycle microprocessor in Vivado using VHDL (consult my MIPS32 Single Cycle repository for further details), by allowing multiple instructions to be executed simultaneously without having to wait for the currently running instruction to end entirely. This is done via implementing some auxiliary pipline-ing registers between each consecutive stages. Of course, this comes with the risk of a certain instruction (which I will be refering to as "the former") tampering with data stored within registers that a previous instruction ("the latter") is also currently using, which can cause erroneous and unexpected results from the latter. This phenomenon is commonly referred to as a "data hazard", and the most common way to prevent it is through voluntarily stalling the execution of the former until the latter finishes tampering with the registers. If this all sounds abstract, an example program ROM (Fibonacci Original.txt) has been provided alongside the .vhd files, as well as an Excel table which models the execution of said program (Fibonacci Without Fixed Hazards.xlsx), in which every hazard is addressed and highlighted. A fixed version of this program using microprocessor stalling was also proposed and attached in this repository, dubbed "Fibonacci Fixed.txt", as well as its execution table (ACFibonacciFixedHazards.xlsx). As in the case of the Single Cycle MIPS, example ROMS can be written in the IFetch.vhd file for further execution.

# Hardware Requirements:
- [ ] A **Xilinx Basys 3 Board**
- [ ] A **USB cable** for powering the board

# Software Requirements:
- [ ] The **Xilinx Vivado IDE**
