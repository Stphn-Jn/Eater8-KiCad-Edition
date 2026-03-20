# Ben Eater 8-Bit Computer: Proteus to KiCad Implementation

This repository contains a complete hardware reconstruction of the 8-bit breadboard computer originally designed by Ben Eater. The project transitions the design from a modular breadboard prototype into a verified digital simulation in Proteus and a professional multi-sheet PCB layout in KiCad.

## Project Overview
This project provides the full design files for an 8-bit TTL-based computer. Unlike the original breadboard version, this implementation focuses on hardware reliability and scalability through the use of printed circuit boards.

* **Simulation:** Verified logic and timing using Proteus 8.x.
* **Hardware:** Fully routed PCBs designed in KiCad, optimized for signal integrity and modular assembly.
* **Architecture:** SAP-1 (Simple As Possible) inspired, featuring a 4-bit program counter, 8-bit ALU, and microcode-based control logic.

## Key Features
* **Full Proteus Digital Twin:** A complete .pdsprj file to test programs and verify logic before hardware fabrication.
* **Modular PCB Design:** The system is organized into functional blocks (Registers, ALU, RAM, Control Logic) to assist in troubleshooting and signal tracing.
* **Instruction Set:** Supports standard operations including LDA, ADD, SUB, OUT, and HLT.
* **Visual Debugging:** Integrated LED bus monitors for the Data Bus and Address Bus to track real-time execution.

## Repository Structure
```text
├── Simulation/          # Proteus project files and logic testing
├── Hardware/            # KiCad schematics, PCB layouts, and Footprints
├── Firmware/            # Arduino sketches for EEPROM microcode programming
├── Documentation/       # Datasheets for 74-series ICs used
└── README.md
```

## Technical Specifications
| Component | Implementation |
| :--- | :--- |
| **CPU** | 8-bit Breadboard-inspired TTL Logic |
| **Clock** | Variable frequency (Manual Pulse / Auto-run) |
| **RAM** | 16 Bytes (utilizing 74LS189 or equivalent) |
| **ALU** | Addition and Subtraction (74LS283) |
| **Control Logic** | EEPROM-based (28C16) microcode |
| **Display** | Triple 7-segment output for decimal/hex viewing |

## Tools Used
* **Simulation:** Proteus Design Suite
* **PCB Design:** KiCad EDA
* **Microcode Programming:** Arduino (for flashing the 28C16 EEPROMs)

## Usage Instructions
1. **Simulate:** Open the files in the Simulation folder using Proteus to verify the logic gates and timing diagrams.
2. **Fabricate:** Utilize the Gerber files located in the Hardware folder for PCB manufacturing.
3. **Program:** Use the provided Assembly examples and EEPROM flashing scripts to load instructions into the system memory.

---
*Developed by Calista as a 4th-year Computer Engineering project.*

