# FPGA-ASIC-Resources
A list of resources for learning about FPGAs and ASICs. Hardware can be bit pricier than microcontrollers and Raspberry Pis, so start with fundamentals and use hobby/learning boards and open source tooling

## FPGAs: Field Programmable Gate Arrays

### Foundations and Programming Practice
* *Digital Design and Computer Architecture* – Harris & Harris (le bible)
  * [Video Edition on YouTube](https://www.youtube.com/playlist?list=PLtPO_rucDaUxt1bdmBpLwU7XjwsnmV8eC)
* [Beej's Guide to Network Programming](https://beej.us/guide/bgnet/html/)
* [Nandland.com](https://nandland.com/) – free, excellent beginner VHDL/Verilog tutorials
* [HDLBits](https://hdlbits.01xz.net/wiki/Main_Page) – interactive Verilog exercises (basically LeetCode for FPGA)
* *SystemVerilog for Design* – Sutherland
* [Doulos SystemVerilog Golden Reference Guide](https://www.doulos.com/grg-exclusive/systemverilog-golden-reference-guide-resources/)
* [The Complete Guide to Preparing for a High-Frequency Trading FPGA Developer Interview](https://thedatabus.in/hft_interview/)

### Hardware
* [Arty A7-100T: Artix-7 FPGA Development Board](https://digilent.com/shop/arty-a7-100t-artix-7-fpga-development-board/?srsltid=AfmBOopSCCTm36s_PC5miB9WsMjXNiy4Wcielw0k4o8ofjHMX7dEuTu_)
* Xilinx Vivado (free for most devices)

### Project Ideas
* ITCH market data parser
* Order book (top-of-book)
* Hardware UDP/IP stack
* SMA/EMA calculator at line rate
* PCIe DMA interface

### Concepts to Focus on
**Introductory**
* Boolean algebra, combinational vs sequential logic
* Flip-flops, registers, finite state machines (FSMs)
* Clock domains, metastability, synchronization
* Timing analysis: setup/hold times, critical paths

**HDL Programming in SystemVerilog**
* RTL design: always blocks, assign statements, modules, ports
* Parameterized modules, generate statements
* Simulation and testbenches
* Synthesis vs simulation semantics (critical distinction)
* Interfaces and packages in SystemVerilog
* Using Xilinx Vivado

**Computer Networking**
* UDP/IP stack in hardware — implement a minimal one yourself
* 10GbE / 100GbE — standard in trading infra
* PCIe — how FPGAs connect to host servers
* RDMA / kernel-bypass concepts

**Market Data Protocols**
* ITCH (NASDAQ) — fixed-width binary, easy to parse in hardware
* OUCH, FIX/FAST, SBE (Simple Binary Encoding)

**Latency Optimization**
* Pipelining and throughput vs latency tradeoffs
* Timing closure — meeting timing constraints, fixing violations
* Critical path analysis, retiming
* Avoid BRAM latency where possible; use registers/LUT-RAM
* Resource utilization: LUTs, FFs, DSPs, BRAMs

**High-Speed Design**
* CDC (Clock Domain Crossing) — essential for multi-clock systems
* FIFO design and flow control
* AXI4-Stream — industry-standard handshaking protocol
* Avoid asynchronous resets in most cases

**Order book on FPGA**
* Price-level aggregation at line rate
* Top-of-book tracking

## ASICs: Application Specific Integrated Circuits

* LibreLane
  * SkyWater 130nm PDK
  * Yosys
  * OpenROAD

*(This file is still under construction. Stay tuned for more resources.)*
