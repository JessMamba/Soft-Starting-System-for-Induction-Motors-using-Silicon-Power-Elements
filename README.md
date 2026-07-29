# Thyristor-Controlled Soft Starter for Three-Phase Asynchronous Motors

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![MATLAB/Simulink](https://img.shields.io/badge/Simulation-MATLAB%20Simulink-orange.svg)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)

This repository contains the simulation models, theoretical calculations, and performance evaluation reports for starting a three-phase asynchronous motor using a **Thyristor-based Soft Starting System**

---

## 📌 Project Overview

Asynchronous motors draw high starting currents (several times their nominal rating) during direct-on-line (DOL) startup, which can cause significant voltage drops and affect the stability of the power grid and connected equipment. The objective of this project is to model, analyze, and compare direct-on-line starting versus a thyristor-controlled soft-start method in MATLAB/Simulink to limit initial high currents and control electromagnetic torque spikes

---

## ⚡ System Specifications & Parameters

The simulations are based on a 3-phase industrial asynchronous motor configuration:
* **Nominal Power ($P_n$):** $1100\text{ W}$
* **Line-to-Line RMS Voltage ($V_n$):** $400\text{ V}$
* **Frequency ($f$):** $50\text{ Hz}$
* **Nominal Speed ($n_n$):** $2850\text{ rpm}$ (Synchronous Speed: $3000\text{ rpm}$)
* **Nominal Current ($I_n$):** $1.868\text{ A}$
* **Power Factor ($pf$):** $0.85$ (lagging)

---

## 🛠️ Working Principle & Methodology

1. **Thyristor Phase Control:** Anti-parallel connected thyristors in each phase control the applied voltage waveform by adjusting the firing angles.
2. **Voltage Ramping:** During startup, the initial firing angles restrict the voltage applied to the motor stator, keeping the initial current low. As the motor accelerates, the firing angles are advanced to gradually increase the voltage.
3. **Bypass Operation:** Once the motor reaches its nominal speed, a bypass contactor engages to short-circuit the thyristors, minimizing semiconductor conduction losses during steady-state operation.

---

## 📈 MATLAB / Simulink Simulation Results

A comparative analysis between direct-on-line starting and thyristor-controlled soft starting yielded the following results:
* **Starting Current:** Direct startup produced an initial peak current of approximately $9.35\text{ A}$, whereas the soft starter successfully reduced the initial starting current to roughly $7.39\text{ A}$.
* **Torque Control:** The maximum transient starting torque dropped significantly from roughly $5.07\text{ Nm}$ (direct starting) down to $2.42\text{ Nm}$ (soft starting), preventing abrupt mechanical shocks.
* **Speed Profile:** The soft starter introduced smooth, controlled acceleration, mitigating violent mechanical stress on shafts, gears, and bearings.

---
