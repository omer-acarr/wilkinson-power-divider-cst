# 📡 Wilkinson Power Divider Design & Simulation (4.5 GHz)

This repository contains the design, electromagnetic modeling, and S-parameter analysis of a **Wilkinson Power Divider** optimized for the **4.5 GHz** center frequency using **CST Studio Suite 2025**.

## 🚀 Project Overview
The project focuses on developing a high-performance microstrip power divider with the following objectives:
* **Equal Power Splitting:** 50/50 power distribution from Port 1 to Ports 2 and 3.
* **Impedance Matching:** All ports matched to $50 \Omega$ to minimize reflections.
* **Isolation:** High isolation ($>20$ dB) between output ports via a $100 \Omega$ lumped resistor.

## 🛠 Design Parameters (4.5 GHz Optimization)
The dimensions were calculated based on transmission line theory for the **Rogers RO4350B** substrate ($\epsilon_r = 3.66$, $h = 1.524$ mm).

| Parameter | Value (mm) | Description |
| :--- | :--- | :--- |
| **in_rad** | 6.0 | Inner radius of the circular transformation arms |
| **out_rad** | 7.8 | Outer radius of the circular transformation arms |
| **width** | 3.1 | Feed line width for $50 \Omega$ matching |
| **mejera** | 1.8 | Quarter-wave arm width for $70.7 \Omega$ impedance |
| **R_iso** | 100 $\Omega$ | Isolation resistor (Lumped element) |

## 📊 Simulation Results (4.0 - 5.0 GHz)

### 1. S-Parameters Analysis
* **S11 (Input Return Loss):** Below -20 dB at 4.5 GHz, indicating excellent input matching.
* **S21 & S31 (Insertion Loss):** Approximately -3.2 dB, representing near-ideal power division.
* **S23 (Isolation):** Significant dip at 4.5 GHz, confirming port-to-port isolation.

### 2. Tolerance & Sensitivity Analysis
To ensure design reliability against manufacturing variations, a sensitivity analysis was performed on the **Rogers RO4350B** substrate:
* **Dielectric Tolerance:** Simulated $\epsilon_r$ variations within $\pm 0.05$.
* **Findings:** Despite production-level variations, isolation performance remained consistently below the **-20 dB safety threshold**. 
* **Frequency Shift:** The center frequency shift remained within acceptable limits, confirming the design's robustness for real-world fabrication.



## ⚠️ Engineering Insights & Optimization
1. **Port Narrowing:** Resized Waveguide Ports from full-substrate width to the specific microstrip width ($3.1$ mm) to eliminate parasitic capacitance.
2. **Frequency Tuning:** Adjusted the `in_rad` and `out_rad` parameters iteratively to center the resonance precisely at 4.5 GHz.
3. **Boundary Conditions:** Utilized "Open (add space)" boundaries to accurately account for fringe fields and radiation effects.

## 💻 Setup & Simulation
1. Open the `.cst` project file in **CST Studio Suite 2025**.
2. Check the **Parameter List** for 4.5 GHz values.
3. Run the **Transient Solver** (use Parameter Sweep for further tolerance tests).
4. Verify results in **1D Results -> S-Parameters**.
