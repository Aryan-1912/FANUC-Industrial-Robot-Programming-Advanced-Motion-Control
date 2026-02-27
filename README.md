# FANUC Industrial Robot Programming – Advanced Motion Control

## Overview
This project demonstrates advanced industrial robot programming using a FANUC robot and teach pendant in a hands-on lab environment at Sheridan College. The program was developed as part of the Industrial Robotics course (ENGI25469) and showcases real-world automation concepts including cycle timing, iteration tracking, dynamic positional offsets, and conditional program flow control.

## What the Program Does
The robot executes a multi-cycle automated motion sequence that:
- Runs a predefined path of joint and linear movements across 3 complete cycles
- Dynamically shifts the robot's Z-axis position by 15mm after each cycle using position register offsets
- Tracks the number of completed cycles using a data register counter
- Measures and records total cycle time using a built-in timer
- Uses conditional branching logic to loop back or exit based on the cycle count

## Concepts Implemented

**Timers**
A timer was initialized at the start of the program and stopped at the end to record total cycle time, stored in a dedicated data register.

**Counters**
A cycle counter register was initialized to zero and incremented after each completed semi-circle movement to track program iterations.

**Position Register Offsets**
A position register was created with X, Y, Z, W, P, R values. The Z element was incremented by 15mm after each cycle, causing the robot to rise progressively with each pass — simulating a real stacking or layering operation.

**Conditional Branching**
A conditional branch instruction checks the cycle counter value after each iteration. If the count is less than 3, the program jumps back to the start of the square positions. Once 3 cycles are complete, the program exits.

## Hardware and Software
- Robot: FANUC Industrial Robot
- Controller: FANUC R-30iB
- Programming Interface: FANUC Teach Pendant (iPendant)
- Programming Language: FANUC TP (Teach Pendant Language)
- Testing: Step mode and Continuous mode

## Proof of Work
Lab report and teach pendant screenshots are included in this repository as PDF documentation.

## Skills Demonstrated
- FANUC teach pendant programming
- Joint and linear motion instruction configuration
- Position and data register management
- Dynamic offset programming for automated path adjustment
- Conditional and unconditional branching logic
- Cycle time measurement and counter implementation
- Industrial robot safety procedures and DEADMAN switch operation

## Academic Context
**Course:** ENGI25469 – Industrial Robotics  
**Institution:** Sheridan College – Computer Engineering Technology  
**Term:** Summer 2024
