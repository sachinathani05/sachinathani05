# Sachin Balappa Athani

**MSc Microelectronics · Newcastle University UK (2025–2026)**  
Design Verification · Analog/IC Layout · Physical Design  
SystemVerilog · UVM · Cadence Virtuoso · OpenLane/SKY130

[![LinkedIn](https://img.shields.io/badge/LinkedIn-sachin--athani-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/sachin-athani)
[![GitHub](https://img.shields.io/badge/GitHub-sachinathani05-181717?style=flat&logo=github)](https://github.com/sachinathani05/VLSI)
[![IEEE](https://img.shields.io/badge/Published-IEEE%20Xplore-00629B?style=flat)](https://ieeexplore.ieee.org/document/9688429)
[![IJRASET](https://img.shields.io/badge/Published-IJRASET-orange?style=flat)](https://www.ijraset.com/research-paper/paper-on-crop-gen-forecast)

---

## About

I'm a Microelectronics postgraduate bridging 2.5 years of industry verification experience with formal VLSI training across the full design-to-silicon stack. My background is in functional verification and test automation at Checkpoint Systems — skills I'm applying directly to RTL testbench design, UVM environments, and analog IC layout.

Two peer-reviewed publications (IEEE Xplore + IJRASET). Currently targeting **Design Verification Engineer** and **Analog/IC Layout Engineer** roles in the UK and India.

---

## ✅ Completed Projects

### Analog IC Design — Cadence Virtuoso (GPDK090 / UMC 65nm)

| Project | Key Results | Tools |
|---------|------------|-------|
| [CMOS Inverter — Schematic, Layout, DRC/LVS](https://github.com/sachinathani05/VLSI/tree/main/Cadence%20Virtuoso/90nm%20(GPDK090)/CMOS%20Inverter) | DC + transient char · VM sweep · W/L parametric · LTSpice cross-check | Cadence Virtuoso · LTSpice |
| [3-Stage Ring Oscillator](https://github.com/sachinathani05/VLSI/tree/main/Cadence%20Virtuoso/90nm%20(GPDK090)/Ring%20Oscillator) | **f = 1.45 GHz**, tp = 115 ps · W-L sweep (freq/power CSV + plots) | Cadence Virtuoso · GPDK090 |
| [UMC 65nm Standard Cell Design — Inverter, Tri-State Inverter, D Flip-Flop](https://github.com/sachinathani05/VLSI/tree/main/Cadence%20Virtuoso/65nm%20(UMC)/Standard%20Cell%20Design%20(EEE8127)) | Full DRC/LVS/PEX flow · pre/post-PEX timing & energy · fanout analysis · wire delay · energy-VDD sweep | Cadence Virtuoso · Calibre · Spectre |

**45nm Two-Stage Miller-Compensated OTA highlights (GPDK045):**

- **Pre-layout:** DC gain 75.6 dB · GBW 57.5 MHz · Phase margin 60.9° · CMRR 76.4 dB · PSRR 164.4 dB
- **Corner sweep (9 points):** TT/SS pass all corners; FF corner fails PM at 27°C/125°C — root-caused to PMOS mobility degradation, fix proposed (Cc 1.35pF → 1.55pF)
- **Layout signoff:** DRC clean (0 violations) · LVS matched (2 documented waivers) · PEX extracted
- **Post-layout debugging:** Root-caused a genuine LVS-vs-RCX extraction discrepancy (`_avConflict` net), a tail-node short from a shared substrate tap, and a structural M6 finger-wiring defect (25-finger device wired as a series chain instead of parallel) — the leading cause of a closed-loop bias-point convergence issue, now logged with a concrete layout fix

---

**Newcastle University — EEE8127 Digital IC Design highlights:**

- **Inverter (65nm):** Logical Effort sizing with DRC-driven correction (2:1 → 1.6:1 for dual-contact rule). Post-PEX: tpHL +12.3%, energy/cycle +42.6% vs. schematic. Physical explanation documented.
- **Fanout Analysis:** LE model tested at FO0–FO4. Schematic Cin = 0.703 fF, extracted Cin = 1.078 fF (+53%). LE overestimates delay by up to 60% at FO4 — Cpar/Cin ≈ 4:1 at 65nm.
- **Wire Delay:** Elmore RC validated — 1 µm vs 100 µm M1 wire. Crossover at **~55 µm** (one gate delay = wire delay). M1 capacitance: 0.113 fF/µm (matches PDK spec).
- **Energy–VDD Sweep:** 48-stage chain, 0.4V–2.0V. **MEP at 0.8V** (25.5% energy saving, 2× delay cost). EDP minimum at 1.2–1.4V. Alpha-power law non-linearity quantified.
- **D Flip-Flop:** Master-slave from verified sub-cells. Post-PEX energy = 174.6 fJ vs 89.5 fJ schematic (+95.1%). Dual-spike structure explained and linked to clock gating motivation.

---

### Digital RTL — Verilog on Vivado & iVerilog

| Project | What It Shows | Tools |
|---------|--------------|-------|
| [4-Bit ALU](https://github.com/sachinathani05/VLSI/tree/main/Verilog/Vivado/ALU_4Bit) | ADD/SUB/AND/OR/XOR · carry + zero flags · synthesis utilization report | Vivado · Verilog |
| [UART Transmitter FSM](https://github.com/sachinathani05/VLSI/tree/main/Verilog/Vivado/UART%20Transmitter%20FSM) | Baud generator + 4-state FSM (IDLE/START/DATA/STOP) · simulation waveform | Vivado · Verilog |
| [Traffic Light Controller](https://github.com/sachinathani05/VLSI/tree/main/Verilog/Vivado/Traffic%20Light%20Controller) | Moore FSM · tick divider · FPGA constraints (.xdc) · synthesis report | Vivado · Verilog |
| [4-Bit Counter](https://github.com/sachinathani05/VLSI/tree/main/Verilog/Vivado/4-Bit%20Counter) | Synchronous counter · testbench · Vivado simulation | Vivado · Verilog |
| [Sequence Detector FSM (Moore)](https://github.com/sachinathani05/VLSI/tree/main/Verilog/iverilog/Sequence%20Detector%20FSM%20%28Moore%29) | 101-pattern detector · two-process FSM style · iVerilog + VCD | iVerilog · GTKWave |
| [Full Adder, Comparator, MUX 4×1, 8-bit Register](https://github.com/sachinathani05/VLSI/tree/main/Verilog/iverilog) | RTL building blocks with testbenches + waveform captures | iVerilog |

---

### Digital Logic Fundamentals — Sequential Circuits

| Module | Type |
|--------|------|
| [D Latch, SR Latch (NOR), D Flip-Flop, JK Flip-Flop](https://github.com/sachinathani05/VLSI/tree/main/Fundamentals/Sequential%20Logic) | Logic simulation (.circ) |
| [4-Bit Ripple Counter, 4-Bit Synchronous Counter](https://github.com/sachinathani05/VLSI/tree/main/Fundamentals/Sequential%20Logic) | |
| [PIPO, PISO, SIPO, SISO Shift Registers](https://github.com/sachinathani05/VLSI/tree/main/Fundamentals/Sequential%20Logic) | |

---

### Real-Time Operating System — M68K Assembly

**[RTOS in Motorola 68000 Assembly](https://github.com/sachinathani05/VLSI/tree/main/RTOS/RTOS%20in%20M68K%20Assembly)** — Newcastle University EEE8087

Built from scratch on EASy68K simulator. Features:
- Round-robin scheduler with circular TCB ready list
- Context switching — full 16-register save/restore via FLIH + RTE dispatch
- Mutex (wait/signal) with blocked task queue
- 6 system calls via `trap #0`: create, delete, wait_time, wait_mutex, signal_mutex, init_mutex
- Two application programs: stopwatch (concurrent task + polling) and radiation monitor (shared counter with mutex protection)

*Demonstrates: interrupt handling, context switching, critical sections, deadlock prevention — directly analogous to DV lab infrastructure design.*

---

### UART — Full RTL-to-GDSII Flow (OpenLane/SKY130)

**[UART RTL-to-GDSII — SKY130 130nm](https://github.com/sachinathani05/VLSI/tree/main/RTL_to_GDSII_Projects/P3_RTL_to_GDSII_OpenLane_SKY130)**

Complete physical design flow from RTL to manufacturing-ready GDSII using OpenLane 2, Yosys, OpenROAD, Magic, KLayout, and Netgen on SkyWater SKY130A.

- **Synthesis:** 267 cells, 60 flip-flops, 3034.16 µm² — 0 CHECK problems
- **Floorplan:** 40.1% core utilisation (target 40%)
- **Placement:** HPWL optimised 4127.8 → 3925.2 µm, 0.0 µm displacement
- **CTS:** H-tree, real measured clock skew **~1.6 ps**
- **Routing:** 0 congestion overflow, 0 antenna violations, 0 DRC violations
- **STA:** **0 setup/hold violations across all 9 PVT corners** — worst setup 10.55 ns, worst hold 0.144 ns
- **Sign-off:** DRC clean (Magic + KLayout independent cross-check), LVS matched uniquely (Netgen)
- **Output:** 3 GDSII files generated, ready for foundry submission

*Full debugging log included — toolchain setup on WSL2, Yosys/Pyosys version conflicts, KLayout display issues, and 10+ other real environment fixes documented.*

---

## 🔨 In Progress

### Full-Stack Digital — UVM Verification + Physical Implementation

| # | Project | Tools | Status |
|---|---------|-------|--------|
| 1 | [SPI Master — RTL & Directed Verification (Week 1 ✅)](https://github.com/sachinathani05/VLSI/tree/main/RTL_to_GDSII_Projects/P1_SPI_Master_RTL_Directed_Verification) | SystemVerilog · QuestaSim | 🟡 Week 2 In Progress |
| 2 | [AXI4-Lite Verification IP (VIP)](https://github.com/sachinathani05/VLSI/tree/main/RTL_to_GDSII_Projects/P2_AXI4_Lite_UVM_Verification) | SystemVerilog · UVM · Sequences | 🟡 In Progress |
| 4 | [STA Timing Closure — Custom Constraints & ECO](https://github.com/sachinathani05/VLSI/tree/main/RTL_to_GDSII_Projects/P4_STA_Timing_Closure) | OpenSTA · SDC · TCL Scripting | 🟡 In Progress |
| 5 | [RISC-V ALU — Full Stack Integration](https://github.com/sachinathani05/VLSI/tree/main/RTL_to_GDSII_Projects/P5_RISCV_ALU_Full_Stack) | RTL → Synthesis → P&R → GDSII | 🟡 In Progress |

### Advanced Analog IC Design — Cadence Virtuoso 45nm

| # | Project | Key Technique | Status |
|---|---------|--------------|--------|
| 1 | [Two-Stage Miller-Compensated OTA](https://github.com/sachinathani05/VLSI/tree/main/Cadence%20Virtuoso/45nm/Project_01_Two_Stage_OTA_45nm) | Schematic + DRC/LVS/PEX signoff complete · post-PEX root-cause debugging documented | 🟡 PEX fix in progress |
| 2 | Low-Dropout Regulator (LDO) | Full IP sub-system · Loop stability · Load transient | 🔜 Planned |
| 3 | 6T SRAM Bit-Cell Array (4×4) | SNM butterfly curves · DRC/LVS · Yield analysis | 🔜 Planned |
| 4 | StrongARM Latch — High-Speed Comparator | Metastability · Common-centroid layout · PEX timing | 🔜 Planned |
| 5 | Switched-Capacitor Integrator | Charge injection · Capacitor matching · MOM layout | 🔜 Planned |

### MSc Dissertation — Newcastle University (2026)
*Details to follow on completion — September 2026.*

---

## 🛠 Technical Skills

### EDA & Simulation
`Cadence Virtuoso` · `Mentor Calibre (DRC/LVS/PEX)` · `Cadence Spectre` · `Xilinx Vivado` · `ModelSim / QuestaSim` · `LTSpice` · `Electric VLSI` · `OpenLane` · `OpenSTA` · `iVerilog`

### HDL & Programming
`SystemVerilog` · `UVM` · `Verilog` · `VHDL` · `Python` · `TCL Scripting` · `C/C++ (embedded)` · `M68K Assembly`

### VLSI Design Concepts
`CMOS Layout` · `DRC / LVS / PEX` · `Parasitic Extraction` · `Static Timing Analysis (STA)` · `Logical Effort Sizing` · `Coverage-Driven Verification` · `Constrained-Random Testing` · `RTL Design` · `Logic Synthesis` · `Power Optimisation` · `RTOS Design`

### Protocols & Interfaces
`SPI` · `AXI4-Lite` · `I2C` · `RS232` · `UART` · `AMBA`

### Hardware Platforms
`FPGA (Xilinx ISE / Vivado)` · `Arduino` · `ESP8266` · `RISC-V`

---

## 📄 Publications

### Smart Band Communication for Visually and Auditory Impaired People
**IEEE Xplore — ICMNWC 2021**

Wearable assistive device for deafblind communication. ESP8266 (Bolt IoT) + 3 vibrating modules (200Hz, 10mm×2.8mm). SqueezeNet CNN (TensorFlow/Keras) trained on 1,000 images across 8 gesture categories — 75–78% recognition accuracy. Google SpeechRecognition API — ~95% speech-to-text accuracy.

### Crop Gen Forecast — IoT + ML Crop Price Prediction
**IJRASET**

Soil NPK sensor (TTL-485 Modbus) + pH sensor (analogue) → NodeMCU/ESP8266 → ThingSpeak cloud. Random Forest classifier + Decision Tree regression. Flask web app with 6/12-month crop price forecasting.

---

## 🎓 Certifications

**Chip-based VLSI Design for Industrial Applications** — L&T EduTech / Coursera · June 2025  
Electric VLSI · LTSpice · VHDL on Xilinx ISE/Vivado · SPI, I2C, RS232 sensor interfacing

**VLSI CAD Part I: Logic & Part II: Layout** — University of Illinois / Coursera · March 2025  
BDD · SAT-based verification · Logic synthesis · ASIC placement · Maze routing · STA (AT/RAT/slack · Elmore delay)

---

## 🎓 Education

**MSc Microelectronics: Systems and Devices** — Newcastle University, UK · 2025–2026  
Low-Power VLSI Design · Microelectronics Design Tools · Advanced Device Fabrication · Advanced Electronic Devices · Real-Time Embedded Systems

**BE Electronics and Communication Engineering** — BNM Institute of Technology (VTU), India · 2022 · CGPA 8.2/10

---

## 💼 Industry Experience

**Software Engineer II — Checkpoint Systems, Bengaluru** · Sept 2022 – Nov 2024  
Functional verification and test automation across 3 concurrent RFID-based retail product lines. 900+ test cases, 500+ verified defects, 200+ API validations. Regression suites, root-cause documentation, defect triage — directly transferable to RTL testbench workflows.

---

## 📬 Contact

📧 sachinathani05@gmail.com  
🔗 [linkedin.com/in/sachin-athani](https://www.linkedin.com/in/sachin-athani)  
📍 Newcastle, UK · Graduate Route Visa (open to UK work)

---

*Active build — updated progressively through September 2026.*
