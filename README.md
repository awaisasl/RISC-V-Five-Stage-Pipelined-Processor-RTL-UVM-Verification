# RISC-V-Five-Stage-Pipelined-Processor-RTL-UVM-Verification
SystemVerilog five-stage RISC-V pipelined processor with hazard detection, forwarding, branch handling, and a Cadence Xcelium/UVM verification environment.

<p align="center">
  <b>SystemVerilog RTL Implementation + UVM Functional Verification</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/HDL-SystemVerilog-blue" alt="SystemVerilog">
  <img src="https://img.shields.io/badge/Architecture-RISC--V-orange" alt="RISC-V">
  <img src="https://img.shields.io/badge/Pipeline-5--Stage-green" alt="5 Stage Pipeline">
  <img src="https://img.shields.io/badge/Verification-UVM-purple" alt="UVM">
  <img src="https://img.shields.io/badge/Simulator-Cadence%20Xcelium-red" alt="Cadence Xcelium">
  <img src="https://img.shields.io/badge/Platform-Linux-lightgrey" alt="Linux">
</p>

---

## Overview

This project presents a **32-bit RISC-V five-stage pipelined processor** implemented in **SystemVerilog RTL** and verified using a dedicated **Universal Verification Methodology (UVM)** environment with **Cadence Xcelium**.

The processor is organized around the classical five-stage RISC pipeline:

```text
        ┌────────┐
        │   IF   │  Instruction Fetch
        └───┬────┘
            │
        ┌───▼────┐
        │   ID   │  Instruction Decode
        └───┬────┘
            │
        ┌───▼────┐
        │   EX   │  Execute
        └───┬────┘
            │
        ┌───▼────┐
        │  MEM   │  Memory Access
        └───┬────┘
            │
        ┌───▼────┐
        │   WB   │  Write Back
        └────────┘
