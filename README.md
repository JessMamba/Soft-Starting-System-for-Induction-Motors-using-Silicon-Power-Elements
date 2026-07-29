# Thyristor-Controlled Soft Starter for Three-Phase Asynchronous Motors

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![MATLAB/Simulink](https://img.shields.io/badge/Simulation-MATLAB%20Simulink-orange.svg)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)

This repository contains the simulation models, theoretical calculations, and performance evaluation reports for starting a three-phase asynchronous motor using a **Thyristor-based Soft Starting System**.

---

## 📌 Project Overview

Asynchronous motors draw high starting currents (several times their nominal rating) during direct-on-line (DOL) startup, which can cause significant voltage drops and affect the stability of the power grid and connected equipment[cite: 3]. The objective of this project is to model, analyze, and compare direct-on-line starting versus a thyristor-controlled soft-start method in MATLAB/Simulink to limit initial high currents and control electromagnetic torque spikes[cite: 3].

* **Institution:** Bursa Technical University[cite: 3]
* **Faculty:** Faculty of Engineering and Natural Sciences, Department of Electrical and Electronics Engineering[cite: 3]
* **Course:** EEM0303 Electrical Machines (2025–2026 Fall Semester)[cite: 3]
* **Project Advisor:** Dr. Öğr. Üyesi Gürkan AYDEMİR[cite: 3]
* **Project Team:** 
  * Azime Sena YILDIRIM[cite: 3]
  * Musab ALİ[cite: 3]
  * Mehmet Eren DİKMEN[cite: 3]
  * Jess Edmond RAZAFIMANOVOLİLY[cite: 3]
  * Sercan KUL[cite: 3]

---

## ⚡ System Specifications & Parameters

The simulations are based on a 3-phase industrial asynchronous motor configuration[cite: 3]:
* **Nominal Power ($P_n$):** $1100\text{ W}$[cite: 3]
* **Line-to-Line RMS Voltage ($V_n$):** $400\text{ V}$[cite: 3]
* **Frequency ($f$):** $50\text{ Hz}$[cite: 3]
* **Nominal Speed ($n_n$):** $2850\text{ rpm}$ (Synchronous Speed: $3000\text{ rpm}$)[cite: 3]
* **Nominal Current ($I_n$):** $1.868\text{ A}$[cite: 3]
* **Power Factor ($pf$):** $0.85$ (lagging)[cite: 3]

---

## 🛠️ Working Principle & Methodology

1. **Thyristor Phase Control:** Anti-parallel connected thyristors in each phase control the applied voltage waveform by adjusting the firing angles[cite: 3].
2. **Voltage Ramping:** During startup, the initial firing angles restrict the voltage applied to the motor stator, keeping the initial current low[cite: 3]. As the motor accelerates, the firing angles are advanced to gradually increase the voltage[cite: 3].
3. **Bypass Operation:** Once the motor reaches its nominal speed, a bypass contactor engages to short-circuit the thyristors, minimizing semiconductor conduction losses during steady-state operation[cite: 3].

---

## 📈 MATLAB / Simulink Simulation Results

A comparative analysis between direct-on-line starting and thyristor-controlled soft starting yielded the following results:
* **Starting Current:** Direct startup produced an initial peak current of approximately $9.35\text{ A}$[cite: 3], whereas the soft starter successfully reduced the initial starting current to roughly $7.39\text{ A}$[cite: 3].
* **Torque Control:** The maximum transient starting torque dropped significantly from roughly $5.07\text{ Nm}$ (direct starting) down to $2.42\text{ Nm}$ (soft starting), preventing abrupt mechanical shocks[cite: 3].
* **Speed Profile:** The soft starter introduced smooth, controlled acceleration, mitigating violent mechanical stress on shafts, gears, and bearings[cite: 3].

---

## 📂 Repository Structure

```text
├── models/             # MATLAB/Simulink .slx models for direct and soft-starting schemes
├── docs/               # Full project report PDF
└── README.md           # Project documentation
