# ⚡ MOSFET XOR Gate – ELECENG 2EI4 (McMaster University)

## 📖 Project Overview  
This project focused on the **design, implementation, and testing** of a **CMOS XOR gate** for McMaster University’s **ELECENG 2EI4** course.  
The goal was to design a reliable logic gate using **NMOS and PMOS transistors** with correct sizing, implement it physically, and validate its performance through **functional, static, and timing tests**.  

---

## 🛠️ Tools & Components  
- **CMOS Transistors** – NMOS & PMOS devices  
- **Breadboard & Wiring** – Circuit assembly  
- **Capacitors:** 100 nF (for timing analysis)  
- **Signal Generator** – Square wave input source  
- **Oscilloscope (AD3 / WaveForms)** – Capturing logic levels, voltage swings, and timing behavior  

---

## 🔍 Design Details  
- **Circuit Type:** CMOS XOR gate  
- **Transistor Sizing:** PMOS transistors sized **2.5× larger** than NMOS (to compensate for carrier mobility differences)  
- **Symmetry:** Pull-up and pull-down networks designed symmetrically → ensures balanced rise/fall times  
- **Implementation Feasibility:** The design supported ideal CMOS sizing assumptions and produced expected XOR logic  

---

## 📊 Simulation & Testing  
### ✅ Functional Testing  
- Verified XOR truth table:  
  | Input A | Input B | Output |  
  |---------|---------|--------|  
  | 0       | 0       | 0      |  
  | 1       | 0       | 1      |  
  | 0       | 1       | 1      |  
  | 1       | 1       | 0      |  
- Output confirmed XOR behavior on hardware.  

### 📉 Static Level Testing  
- **Case 1:** A = 5V, B = 0–5V square wave → V<sub>OH</sub> ≈ 4.98 V, V<sub>OL</sub> ≈ 3.11 mV  
- **Case 2:** A = 0–5V square wave, B = 5V → V<sub>OH</sub> ≈ 4.97 V, V<sub>OL</sub> ≈ 2.42 mV  
- Percent difference in V<sub>OH</sub>: **0.2%**  
- Percent difference in V<sub>OL</sub>: **24.96%** (due to noise/connection imperfections)  

### ⏱️ Timing Analysis  
- **Rise Time (10% → 90%):** 223.7 µs  
- **Fall Time (90% → 10%):** 213.2 µs  
- **Average Time Constant (τ):** ≈ 109.2 µs  

---

## 🚀 Key Learnings  
- Importance of **PMOS-to-NMOS sizing ratio (2.5:1)** in CMOS design  
- How **symmetry** in pull-up/pull-down networks improves performance  
- Hardware measurements can show noise-induced discrepancies compared to theory  
- Practical experience in verifying **static logic levels** and **timing response**  

---

## 📚 References  
1. ELECENG 2EI4 Lab Guide – *CMOS Logic Design*  
2. Sedra/Smith – *Microelectronic Circuits*  
3. AD3/WaveForms User Documentation  

---

✍️ **Author:** Dhruv Anand  
📅 **Date:** April 2025  
