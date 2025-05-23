# 🧠 8×8 SRAM Memory System | VLSI Final Project ⚙️🔬

This repository hosts the final project for the **Introduction to VLSI Design** course at **Braude Academic College of Engineering**. It features the complete custom design and simulation of an **8×8 Static Random-Access Memory (SRAM)** using **Cadence Virtuoso**, built with transistor-level CMOS components, full custom layout, and digital simulation.

> This project demonstrates a bottom-up, structured approach to digital memory design using industry-standard tools and CMOS technology.

---

## 📚 Project Overview

The system is based on **6-transistor (6T)** SRAM cells arranged in an 8×8 matrix, providing a total of 64 bits of storage. The memory includes custom-designed:
- Logic gates (INV, NAND2, NOR2, AND4)
- 3-to-8 row decoder
- Read/Write control logic
- Fully laid-out SRAM array with DRC/LVS verification
- Simulations verifying correct read and write functionality

The design achieved a maximum simulated operational frequency of **1.58 GHz**, maintaining stability, low power consumption, and layout efficiency.

---

## 🛠️ Design Flow

### ✅ 1. Gate-Level Design
- Designed custom logic gates using CMOS (Inverter, NAND2, NOR2, AND4)
- Verified through functional simulations and timing analysis

### ✅ 2. Row Decoder
- Implemented a 3-to-8 decoder using custom gates
- Generates one-hot wordline signals to enable a single row during access

### ✅ 3. 6T SRAM Cell
- Built using two cross-coupled inverters and two access transistors
- Layout optimized for matching and static noise margin
- Verified with read/write testbenches and transient simulations

### ✅ 4. SRAM Array Integration
- 64 memory cells arranged into an 8×8 grid
- Wordlines connected to decoder outputs; bitlines shared vertically
- Layout maintains modular structure and tiling consistency

### ✅ 5. Read/Write Interface
- Controlled using:
  - `WR`: toggles between read (0) and write (1) modes
  - `DataIn`: data signal for write operations
- Read operations validated by correct output on bitlines

---

## 📊 Performance Highlights

| Feature                 | Specification             |
|------------------------|---------------------------|
| Cell Type              | 6T CMOS                   |
| Array Size             | 8×8 (64 bits)             |
| Max Frequency          | 1.58 GHz (simulated)      |
| Layout Area            | 240 µm × 315 µm           |
| Verification           | DRC, LVS, Transient Sim   |

---

## 🎮 System Features

- ✅ Custom-built from transistor level up
- ✅ Modular, reusable cell design
- ✅ Seamless control using WR and DataIn
- ✅ DRC- and LVS-clean full layout
- ✅ Transient simulations demonstrate correct read/write behavior

---

## 🖼️ Visual Artifacts

### 1. Block Diagram  
> High-level overview of decoder, SRAM array, and control lines  
<img src="docs/System Block Diagram Scematic.png" alt="Block Diagram" width="600"/>

### 2. Layout Previews  
> Snapshots of 6T SRAM cell and tiled 8×8 array  
<img src="layout/8×8 SRAM Array Layout1.png" alt="SRAM Layout" width="600"/>

### 3. Simulation Waveforms  
> Transient analysis for successful write/read cycles  
<img src="docs/Transient Simulations.png" alt="Waveform" width="600"/>

---

## 📂 Repository Structure

```plaintext
.
├── README.md                → Project overview and technical summary
├── LICENSE                  → MIT License
├── docs/                    → PDF report and image assets
│   ├── Final_Project_SRAM.pdf
│   └── sram_block_diagram.png
│   └── waveform_read_write.png
├── schematics/              → Cadence schematic screenshots or exports
├── layout/                  → Layout files and images
├── simulations/             → Testbenches and Spectre simulation files

---

## 📜 Documentation

- 📘 [`Final_Project_SRAM.pdf`](docs/Final_Project_SRAM.pdf):  
  Full project report including schematics, layout screenshots, test setups, simulation outputs, and final conclusions.

- 📁 **Stimulus Files & Waveform Images:**  
  Located in the `/simulations/` and `/docs/` directories, covering inverter, decoder, SRAM cell, and array-level operations.

- 📎 **Schematic and Layout Snapshots:**  
  Available in `/schematics/` and `/layout/` folders, showcasing gate-level components, 6T SRAM cell, and full array layout.

---

## 🔭 Future Work

- ➕ Integrate **sense amplifiers** for faster and more accurate read operations  
- ➕ Implement a **column decoder** to enable full matrix addressability  
- ➕ Expand the design to a **16×16 SRAM array** or explore **multi-port memory architectures**  
- 🔋 Explore **low-power techniques** for energy-efficient SRAM operation, including leakage reduction and dynamic threshold control

---

## 👨‍💻 Authors

- Bshara Habib  
- Francis Aboud  
- Maria Nakhle
- Noor Zakour

