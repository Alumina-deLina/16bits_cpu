# 16bits_cpu
the specific instruction is under Lab_Assignment_3.pdf

# 16-bit Single Cycle CPU
## 📌 Overview
- This project implements a **16-bit single-cycle CPU** in Logisim.
- Uses a **4-bit opcode** to execute **R-type and I-type instructions**.
- Designed for **educational purposes**, focusing on CPU architecture fundamentals.

## 🛠️ Features
- **Fixed-length instructions** with **R-type and I-type formats**.
- **16 general-purpose registers** for computation.
- **Arithmetic, logical, and memory-related operations**.
- **Program Counter (PC)** that increments by **2 per cycle**.
- **Instruction decoder** to control internal signals.
- **Register file provided** with restricted access to A_Out and B_Out.

## 🔄 Instruction Set
- **NOP (0000)** – Do nothing.
- **STOP (0001)** – Halt CPU execution.
- **Arithmetic Operations**:
  - `ADDR` (0010): Addition (RegC = RegA + RegB).
  - `SUBR` (0011): Subtraction (RegC = RegA - RegB).
- **Logical Operations**:
  - `ANDR` (0100), `ORR` (0101), `XORR` (0110).
  - `ANDI`, `ORI`, `XORI` for immediate values.
- **Data Movement**:
  - `MOVE` (1110): Copy register value.
  - `LOAD` (1111): Load immediate value into register.
- **Unary Operations**:
  - `NEGATE` (1100): Negation.
  - `NOT` (1101): Bitwise NOT.

## 📥 Inputs
- **Instruction (16-bit)** – Current instruction to be executed.
- **Clock (1-bit)** – Controls register updates.

## 📤 Outputs
- **Instruction Address (5-bit)** – Next instruction location.
- **Registers (Reg0 - Reg15)** – Holds computed values.

## 🏗️ CPU Components
- **Program Counter (PC)** – Tracks the current instruction.
- **Instruction Decoder** – Generates control signals.
- **Register File** – Holds 16 registers, accessible via A_Out and B_Out.

## 🚀 Example Program
| Instruction | Description | Result |
|------------|------------|--------|
| `LOAD REG0, 3` | Load 3 into REG0 | `REG0 = 3` |
| `LOAD REG1, 6` | Load 6 into REG1 | `REG1 = 6` |
| `MOVE REG2, REG1` | Copy REG1 to REG2 | `REG2 = 6` |
| `ANDR REG3, REG0, REG1` | REG3 = REG0 & REG1 | `REG3 = 2` |
| `ORI REG6, REG3, 12` | REG6 = REG3 OR 12 | `REG6 = 14` |

## 📂 Project Setup
1. Open **Logisim**.
2. Load the **provided Register File circuit**.
3. Implement CPU components (PC, Decoder, ALU, etc.).
4. Test using sample programs.

## 📜 Notes
- Follows **single-cycle CPU design** principles.
- Uses **Logisim's built-in arithmetic and logic gates**.
- CPU must work for **any valid instruction sequence**.
