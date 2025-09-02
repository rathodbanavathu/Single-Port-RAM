# Single-Port RAM (Verilog)

A Verilog implementation of a **single-port synchronous RAM** with parameterized depth and width.  
The design supports both **read** and **write** operations through a single memory port and is verified with a self-checking testbench.

---

## ✨ Features
- Parameterized **data width** and **memory depth**.
- Single read/write port with:
  - `clk` : clock input  
  - `we`  : write enable  
  - `addr`: address bus  
  - `din` : data input  
  - `dout`: data output  
- Synthesizable RTL suitable for ASIC/FPGA.
- Verified with functional testbench and waveform inspection.

---

## 🏗️ Architecture
- **Memory Array**: `reg [DATA_WIDTH-1:0] mem [0:DEPTH-1];`
- **Write Operation**: If `we=1`, data at `din` is stored in memory at address `addr` on rising edge of `clk`.
- **Read Operation**: If `we=0`, memory content at address `addr` is driven to `dout`.

---
