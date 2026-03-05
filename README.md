# BE8-A4: The Breadboardless 8-Bit Computer

###  Overview
This project is a hardware reimagining of Ben Eater's famous 8-bit computer. While the original design spans 14+ breadboards and hundreds of jumper wires, this version integrates the entire architecture—CPU, RAM, Microcode, and Output—onto a single **A4-sized printed circuit board (PCB)**.



###  Improvements & Design Goals
* **Form Factor:** Transitioned from a modular breadboard layout to a rigid, single-board A4 footprint.
* **Signal Integrity:** Reduced noise and "cross-talk" inherent in long breadboard jumper wires.
* **Permanent Storage:** Replaced volatile breadboard connections with soldered reliability.
* **Visual Feedback:** Retained the iconic LED-per-register status indicators for educational debugging.

###  Architecture Modules
The board follows the classic Von Neumann architecture, including:
1.  **Clock Module:** Variable speed with manual pulse mode.
2.  **Registers (A, B, and Instruction):** 8-bit storage for ALU operations.
3.  **ALU:** Addition and Subtraction logic.
4.  **RAM & Program Counter:** 16 bytes of addressable memory.
5.  **Control Logic:** EEPROM-based microcode execution.
6.  **Output:** 4-digit 7-segment display logic.

###  Repository Structure
* `/Schematics`: Kicad/EasyEDA source files.
* `/Microcode`: Python scripts and binaries for the EEPROMs.
* `/Docs`: Wiring diagrams and logic tables.

###  Build Notes
