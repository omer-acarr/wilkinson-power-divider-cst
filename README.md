# 📡 Wilkinson Power Divider Design & Simulation (4.5 GHz)

This repository contains the design, electromagnetic modeling, and S-parameter analysis of a **Wilkinson Power Divider** optimized for the **4.5 GHz** center frequency using **CST Studio Suite 2025**.

## 🚀 Project Overview
The project focuses on developing a microstrip-based power divider that ensures:
* **Equal Power Splitting:** 50/50 power distribution from Port 1 to Ports 2 and 3.
* **Impedance Matching:** All ports are matched to $50 \Omega$ to minimize reflections.
* **Isolation:** High isolation between output ports using a $100 \Omega$ lumped resistor.

## 🛠 Design Parameters (4.5 GHz Optimization)
The physical dimensions were calculated using transmission line theory, ensuring the arms follow the $\lambda/4$ transformation rule for a substrate with $\epsilon_r \approx 3.66$ and $h = 1.524$ mm.

| Parameter | Value (mm) | Description |
| :--- | :--- | :--- |
| **in_rad** | 6.0 | Inner radius of the circular transformation arms |
| **out_rad** | 7.8 | Outer radius of the circular transformation arms |
| **width** | 3.1 | Feed line width for $50 \Omega$ matching |
| **mejera** | 1.8 | Quarter-wave arm width for $70.7 \Omega$ impedance |
| **R_iso** | 100 $\Omega$ | Isolation resistor (Lumped element) |



## 📊 Simulation Results (4.0 - 5.0 GHz)

### 1. S-Parameters Analysis
The simulation was narrowed down to the 4-5 GHz range to achieve higher resolution at the design frequency:
* **S11 (Input Return Loss):** Below -20 dB at 4.5 GHz, indicating excellent input matching.
* **S21 & S31 (Insertion Loss):** Approximately -3.2 dB, representing near-ideal power division with minimal loss.
* **S23 (Isolation):** Significant isolation dip at 4.5 GHz, confirming the effectiveness of the $100 \Omega$ resistor.



### 2. Field Visualization
* **E-Field Distribution:** Verified equal phase and magnitude distribution at output ports.
* **Power Flow (Poynting Vector):** Confirmed smooth energy transition without significant leakage or standing waves.



## ⚠️ Engineering Insights & Optimization
Key technical refinements made during the simulation process:
1. **Port Narrowing:** Resized Waveguide Ports from full-substrate width to the specific microstrip width ($3.1$ mm) to eliminate parasitic capacitance.
2. **Frequency Tuning:** Adjusted the `in_rad` and `out_rad` parameters iteratively to center the resonance precisely at 4.5 GHz.
3. **Boundary Conditions:** Utilized "Open (add space)" boundaries to accurately account for fringe fields in the microstrip structure.

## 💻 Setup & Simulation
1. Open the `.cst` project file in **CST Studio Suite 2025**.
2. Verify the **Parameter List** values for 4.5 GHz.
3. Run the **Transient Solver**.
4. Check **1D Results -> S-Parameters** for performance verification.
