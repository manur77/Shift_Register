# 🔄 Universal Shift Register (4-bit) – Verilog HDL

## 📌 Project Overview
This project implements a **4-bit Universal Shift Register** using Verilog HDL.  
A universal shift register is a versatile digital circuit capable of performing multiple operations such as:

- Parallel Data Loading  
- Shift Left Operation  
- Shift Right Operation  
- Data Hold  

The design is **simulated in ModelSim** and **synthesized using Intel Quartus Prime**, with RTL (Register Transfer Level) verification.

---

## ⚙️ Key Features
- 4-bit register design  
- Supports multiple modes of operation  
- Synchronous with clock signal  
- Asynchronous reset functionality  
- RTL schematic generation  
- Functional simulation waveform verification  

---

## 🧩 Module Description

### 🔹 Inputs
- `clk` → Clock signal  
- `reset` → Asynchronous reset  
- `load` → Enables parallel loading  
- `shift_left` → Enables left shift  
- `shift_right` → Enables right shift  
- `data_in[3:0]` → 4-bit parallel input  
- `serial_in` → Serial data input  

### 🔹 Output
- `data_out[3:0]` → 4-bit register output  

---

## 🔁 Working Principle
On every rising edge of the clock:

- If `reset = 1` → Output is cleared (`0000`)  
- If `load = 1` → Parallel input is loaded into register  
- If `shift_left = 1` → Data shifts left and `serial_in` enters LSB  
- If `shift_right = 1` → Data shifts right and `serial_in` enters MSB  
- Otherwise → Register holds its previous value  

---

## 🧪 Simulation Waveform

![Simulation Waveform](./waveform.png)

### ✔️ Observation
- Shows correct sequential operation of register  
- Confirms proper working of clock and control signals  
- Data transitions are synchronized with clock  

---

## 🧱 RTL / Netlist Diagram

![RTL Diagram](./netlist.png)

### ✔️ Observation
- Flip-flops used for storage  
- Multiplexer selects operation (load/shift)  
- Represents actual hardware implementation  

---

## 🛠️ Tools & Technologies
- **Verilog HDL**  
- **ModelSim (Intel FPGA Starter Edition 10.5b)**  
- **Intel Quartus Prime Lite**  

---

## 📂 Project Structure
