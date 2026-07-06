# Simple CPU Instruction Simulator in C

## Overview

The **Simple CPU Instruction Simulator** is a C programming project that models the fundamental **CPU instruction execution cycle**. The simulator demonstrates how essential processor registers interact while executing a sequence of instructions, providing a practical introduction to computer architecture and processor design.

The program simulates the execution of basic CPU instructions—**LOAD**, **ADD**, **SUBTRACT**, and **JUMP**—while updating key processor registers such as the **Program Counter (PC)**, **Link Register (LR)**, and **Program Status Register (PSR)**. After each instruction is executed, the simulator displays the updated register values, allowing users to observe how a processor manages program execution internally.

This project serves as an educational tool for understanding the relationship between CPU registers, instruction flow, and the fetch–execute cycle.

---

# Project Objectives

The primary objectives of this project are to:

* Simulate a simplified CPU instruction execution cycle
* Execute multiple instructions sequentially
* Demonstrate the functionality of essential CPU registers
* Update processor registers as instructions are executed
* Display register states after every instruction
* Reinforce fundamental computer architecture concepts through software simulation

---

# CPU Registers Simulated

## Program Counter (PC)

The **Program Counter (PC)** stores the address of the next instruction to be executed. After each instruction completes, the PC advances to the following instruction, ensuring sequential program execution.

---

## Stack Pointer (SP)

The **Stack Pointer (SP)** identifies the current top of the system stack.

Since this simulator does not implement stack operations such as **PUSH**, **POP**, **CALL**, or **RETURN**, the Stack Pointer remains unchanged throughout execution.

---

## Link Register (LR)

The **Link Register (LR)** stores the return address whenever a jump instruction occurs.

During execution of the **JUMP** instruction, the simulator saves the address of the next instruction into the Link Register to emulate how processors preserve return locations during program flow changes.

---

## Program Status Register (PSR)

The **Program Status Register (PSR)** stores information describing the processor's current state.

Arithmetic instructions update the PSR to simulate processor status changes following mathematical operations.

---

# Project Resources

### Source Code

The complete C source code for this project is included in this repository.[Click here]()

### Project Images

Screenshots illustrating program execution and output are available in the project documentation.

### Demonstration

A demonstration video showcasing the simulator's execution process is included in the repository.

---

# Instruction Set

The simulator executes the following CPU instructions:

| Instruction  | Description                                              |
| ------------ | -------------------------------------------------------- |
| **LOAD**     | Simulates loading data into the processor                |
| **ADD**      | Performs a simulated addition operation                  |
| **SUBTRACT** | Performs a simulated subtraction operation               |
| **JUMP**     | Simulates a program jump while saving the return address |

Each instruction demonstrates how different CPU registers participate during execution.

---

# System Operation

## 1. Register Initialization

Execution begins by initializing four simulated CPU registers:

* Program Counter (PC)
* Stack Pointer (SP)
* Link Register (LR)
* Program Status Register (PSR)

Each register is assigned an initial value before instruction execution begins.

---

## 2. Instruction Loading

The simulator creates an instruction list containing the following sequence:

1. LOAD
2. ADD
3. SUBTRACT
4. JUMP

The Program Counter is initialized to the first instruction in the sequence.

---

## 3. Fetch–Execute Cycle

The simulator repeatedly performs the following operations:

1. Fetch the current instruction using the Program Counter.
2. Display the instruction being executed.
3. Simulate the corresponding CPU operation.
4. Update any affected processor registers.
5. Increment the Program Counter.
6. Display the updated register values.
7. Continue until all instructions have been executed.

This closely models the classic **Fetch–Execute Cycle** used by modern processors.

---

# Register Activity

| Instruction | Program Counter              | Stack Pointer | Link Register         | Program Status Register |
| ----------- | ---------------------------- | ------------- | --------------------- | ----------------------- |
| LOAD        | Advances to next instruction | No Change     | No Change             | No Change               |
| ADD         | Advances to next instruction | No Change     | No Change             | Updated                 |
| SUBTRACT    | Advances to next instruction | No Change     | No Change             | Updated                 |
| JUMP        | Advances to next instruction | No Change     | Stores Return Address | No Change               |

---

# Program Execution Flow

```text
Start
   │
   ▼
Initialize CPU Registers
   │
   ▼
Load Instruction List
   │
   ▼
Display Initial Register Values
   │
   ▼
Fetch Current Instruction
   │
   ▼
Execute Instruction
   │
   ▼
Update CPU Registers
   │
   ▼
Display Register Values
   │
   ▼
More Instructions?
   │
 ┌────── Yes ──────┐
 │                 │
 ▼                 │
Fetch Next         │
Instruction        │
 │                 │
 └─────────────────┘
   │
  No
   │
   ▼
Execution Complete
   │
   ▼
End
```

---

# Sample Output

```text
===== SIMPLE CPU INSTRUCTION SIMULATOR =====

Initial Register Values:
PC : 0    SP : 1000    LR : 0    PSR : 0

---------------------------------------
Current Executing Task: LOAD
Loading data into the CPU...

Updated Register Values:
PC : 1    SP : 1000    LR : 0    PSR : 0

---------------------------------------
Current Executing Task: ADD
Performing Addition...

Updated Register Values:
PC : 2    SP : 1000    LR : 0    PSR : 1

---------------------------------------
Current Executing Task: SUBTRACT
Performing Subtraction...

Updated Register Values:
PC : 3    SP : 1000    LR : 0    PSR : 0

---------------------------------------
Current Executing Task: JUMP
Jump Instruction Detected...
Return Address Saved in LR: 4

Updated Register Values:
PC : 4    SP : 1000    LR : 4    PSR : 0

---------------------------------------
CPU Instruction Execution Completed Successfully.
```

---

# Learning Outcomes

This project strengthened my understanding of processor architecture and instruction execution by demonstrating how multiple CPU registers cooperate during program execution.

Key concepts explored include:

* The role of the Program Counter in controlling execution flow
* Register updates during arithmetic operations
* Status flag management using the Program Status Register
* Return address storage through the Link Register
* The purpose of the Stack Pointer in stack management
* Sequential instruction processing through the Fetch–Execute Cycle

Although simplified, the simulator provides valuable insight into the internal operation of modern processors.

---

# Technical Highlights

* CPU Register Simulation
* Instruction Execution Cycle
* Fetch–Execute Cycle
* Program Counter Management
* Link Register Operations
* Program Status Register Updates
* Sequential Instruction Processing
* Computer Architecture Fundamentals
* Embedded Systems Concepts
* Structured Programming in C

---

# Skills Demonstrated

* C Programming
* GCC Compilation
* Control Flow Design
* Arrays and Data Structures
* Loop Implementation
* Conditional Logic
* Software Simulation
* Computer Architecture
* Processor Fundamentals
* Embedded Systems Programming

---

# Future Enhancements

Potential improvements include:

* Simulated memory architecture
* Stack implementation with PUSH and POP instructions
* CALL and RETURN instruction support
* Conditional branching and jump instructions
* Instruction decoding module
* User-defined instruction loading
* Arithmetic Logic Unit (ALU) simulation
* Register file expansion
* Complete CPU emulator architecture

---

# Technologies Used

**Programming Language**

* C

**Compiler**

* GCC

**Core Concepts**

* CPU Registers
* Instruction Execution
* Fetch–Execute Cycle
* Computer Architecture
* Embedded Systems Fundamentals

---

# Project Status

**Completed**

This project successfully demonstrates the core principles of CPU instruction execution and processor register management through software simulation. By modeling the interaction between the Program Counter, Stack Pointer, Link Register, and Program Status Register, it provides a practical foundation for understanding processor architecture and serves as a stepping stone toward more advanced CPU and embedded systems development.

---

# Author

**Muhammad Musa**

**Computer Engineering Student | Computer Architecture | Embedded Systems | C Programming | Microcontrollers**

Passionate about designing low-level systems, exploring processor architecture, and building efficient software that bridges hardware and computing fundamentals.
