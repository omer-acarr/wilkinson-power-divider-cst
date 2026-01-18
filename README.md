# C-Band Microstrip Wilkinson Power Divider Design & Simulation

This repository contains the design and electromagnetic simulation of a **Microstrip Wilkinson Power Divider** optimized for the **4-5 GHz** frequency range, developed using **CST Studio Suite 2024**. 

---

## 📌 Project Overview
The Wilkinson Power Divider is a critical passive component used in RF systems for equal power splitting and high port-to-port isolation. This specific design is tailored for **C-Band** applications, commonly used in satellite communications and weather radar systems.

---

## 🛠 Design Specifications & Parameters
The design uses specific geometric parameters to achieve impedance matching at the center frequency.

| Parameter | Value | Description |
| :--- | :--- | :--- |
| **Center Frequency** | 4.5 GHz | Optimized for 4-5 GHz C-Band range |
| **Substrate Height ($h_{sub}$)** | 1.524 mm | Standard high-frequency substrate |
| **Copper Thickness** | 0.035 mm | Standard 1 oz copper layer |
| **Quarter-Wave Arm ($lengthram$)** | 7.0 mm | Optimized for 4.5 GHz $\lambda/4$ matching |
| **Isolation Gap ($mezera$)** | 1.3 mm | Precise gap for 100 Ohm resistor placement |
| **Outer Radius ($Out\_rad$)** | 9.0 mm | Circular feed geometry |
| **Inner Radius ($In\_rad$)** | 7.0 mm | Circular feed geometry |

---

## 🚀 Simulation Setup & Performance
* **Solver Type:** Time Domain Solver
* **Mesh Density:** 16,632 mesh cells ensuring high simulation fidelity
* **Convergence:** Steady state energy criterion successfully met
* **Accuracy:** -40 dB steady state accuracy limit

---

## 📊 Expected Results
* **$S_{11}$ (Return Loss):** Strong resonance observed at 4.5 GHz with reflections below -20 dB.
* **$S_{21} / S_{31}$ (Insertion Loss):** Equal power distribution achieved with ~3.1 dB split loss.
* **$S_{23}$ (Isolation):** High isolation between output ports facilitated by the lumped resistor.

