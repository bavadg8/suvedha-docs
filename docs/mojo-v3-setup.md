---
title: Mojo V3 Setup Guide
nav_order: 1
---

# 🚀 Mojo V3 FPGA Board – Setup Guide

A beginner-friendly tutorial to help you get started with the Mojo V3 FPGA board.

---

## 🧰 Requirements

- Mojo V3 board
- USB cable
- Mojo IDE (or Xilinx ISE for advanced use)
- A simple Verilog code example

---

## 🛠️ Steps

### 1. Install Mojo IDE
Download from [Embedded Micro](https://embeddedmicro.com/) and install it.

### 2. Connect the Board
Plug the Mojo V3 into your system via USB.

### 3. Load Verilog Code
```verilog
module mojo_top(
    input clk,
    output led
);
    reg [24:0] counter = 0;
    always @(posedge clk) begin
        counter <= counter + 1;
    end
    assign led = counter[24];
endmodule
