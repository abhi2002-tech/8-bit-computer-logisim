# TinyCPU-8: An 8-Bit Computer Built in Logisim 🖥️

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Logisim Version](https://img.shields.io/badge/Logisim-3.7.2-green.svg)](http://www.cburch.com/logisim/)

A fully functional 8-bit computer designed in Logisim, capable of executing basic programs like arithmetic operations, conditional jumps, and I/O control. Perfect for learning CPU architecture and digital logic!

![Main Circuit Screenshot](images/cpu-screenshot.png)

---

## Table of Contents
- [Features](#features)
- [Architecture](#architecture)
- [Instruction Set](#instruction-set)
- [How to Use](#how-to-use)
- [Example Programs](#example-programs)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

---

## Features
- **8-bit Data Bus**: Processes 8-bit instructions and data.
- **ALU**: Supports `ADD`, `SUB`, `AND`, `OR`, and `XOR` operations.
- **Registers**: 4 general-purpose registers (`A`, `B`, `C`, `D`), Program Counter (`PC`), and Accumulator (`ACC`).
- **Memory**: 256-byte RAM and 512-byte ROM.
- **Clock Speed**: Adjustable clock (1Hz to 10kHz) for step-by-step debugging.
- **I/O**: Simple LED output and switch input.

---

## Architecture
### Block Diagram
![Architecture Diagram](images/architecture-diagram.png)

- **Von Neumann Architecture**: Shared bus for instructions and data.
- **Components**:
  - Control Unit (Finite State Machine)
  - 8-bit ALU with status flags (Zero, Carry)
  - 256-byte RAM
  - Program Counter (PC) and Instruction Register (IR)

---

## Instruction Set
| Opcode | Mnemonic | Description           | Example           |
|--------|----------|-----------------------|-------------------|
| `0000` | `NOP`    | No operation          | `NOP`             |
| `0001` | `ADD`    | Add memory to ACC     | `ADD 0x0A`        |
| `0010` | `SUB`    | Subtract from ACC     | `SUB 0x0B`        |
| `0011` | `JMP`    | Jump to address       | `JMP 0x1F`        |
| `0100` | `OUT`    | Output ACC to LEDs    | `OUT`             |

See the full [Instruction Set Documentation](docs/instruction-set.md).

---

## How to Use
### Prerequisites
- [Logisim Evolution](https://github.com/logisim-evolution/logisim-evolution) (version 3.7.2+).

### Steps
1.Clone this repository:
   ```bash
   git clone https://github.com/abhi2002-tech/8-bit-computer-logisim
## How to Run
1. Install [Logisim Evolution](https://github.com/logisim-evolution/logisim-evolution).
2. Open `circuits/main.circ`.
3. Load `examples/fibonacci.hex` into RAM.
4. Start the clock!   
