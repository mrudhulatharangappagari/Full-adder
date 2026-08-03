# Full Adder using Verilog HDL

## Project Overview

A Full Adder is a combinational logic circuit that adds three 1-bit binary inputs:
- A
- B
- Cin (Carry-in)

It produces two outputs:
- Sum
- Cout (Carry-out)

This project implements a Full Adder using Verilog HDL and verifies its functionality with a testbench.

---

## Truth Table

| A | B | Cin | Sum | Cout |
|---|---|-----|-----|------|
| 0 | 0 |  0  |  0  |  0   |
| 0 | 0 |  1  |  1  |  0   |
| 0 | 1 |  0  |  1  |  0   |
| 0 | 1 |  1  |  0  |  1   |
| 1 | 0 |  0  |  1  |  0   |
| 1 | 0 |  1  |  0  |  1   |
| 1 | 1 |  0  |  0  |  1   |
| 1 | 1 |  1  |  1  |  1   |

---

## Logic Equations

Sum = A ⊕ B ⊕ Cin

Cout = (A & B) | (B & Cin) | (A & Cin)

---

## Files

- full_adder.v – Verilog design
- full_adder_tb.v – Testbench
- simulation_result.png – Simulation waveform
- README.md – Documentation

---

## Software Required

- Icarus Verilog
- GTKWave (Optional)
- ModelSim / Vivado

---

## Simulation Steps

### Compile

```bash
iverilog -o fulladder full_adder.v full_adder_tb.v
```

### Run

```bash
vvp fulladder
```

### View Waveform

```bash
gtkwave fulladder.vcd
```

---

## Expected Output

```
A B Cin | Sum Cout
0 0 0   | 0   0
0 0 1   | 1   0
0 1 0   | 1   0
0 1 1   | 0   1
1 0 0   | 1   0
1 0 1   | 0   1
1 1 0   | 0   1
1 1 1   | 1   1
```

---

## Applications

- Arithmetic Logic Unit (ALU)
- Binary Adders
- Processors
- Digital Computers
- DSP Systems
- FPGA and ASIC Designs

---

## Author

Your Name
