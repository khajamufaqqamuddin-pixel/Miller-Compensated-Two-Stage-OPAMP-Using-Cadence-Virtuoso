
# Two-Stage Miller-Compensated CMOS Op-Amp (Cadence Virtuoso)

This repository presents the **design, analysis, and simulation** of a
**two-stage CMOS operational amplifier** with **Miller compensation**,
implemented in **Cadence Virtuoso (90 nm technology)**.

---

## 🎯 Design Targets

| Parameter | Symbol | Value |
|---------|--------|-------|
| DC Gain | A₀ | ≥ 60 dB |
| Gain Bandwidth | GBW | 30 MHz |
| Phase Margin | PM | ≥ 60° |
| Slew Rate | SR | 20 V/µs |
| Load Capacitance | Cᴸ | 2 pF |
| Supply Voltage | VDD | 1.8 V |
| Power Dissipation | P | ≤ 300 µW |

---

## 🧠 Op-Amp Architecture

- Differential input stage (M₁, M₂)
- PMOS current-mirror load (M₃, M₄)
- Tail current source (M₅)
- Second gain stage (M₆)
- Miller compensation capacitor (Cᶜ)

---
# Circuit Diagram
The circuit of an OPAMP includes a Differential Stage which contains a differential pair and current mirror. It also includes an Amplification stage to increase the gain.

<p align="center">
  <img src="https://github.com/chennakeshavadasa/Miller-Compensated-Two-stage-OPAMP-using-SKY130PDK/assets/123294639/9c016285-e9c8-4366-aa3d-c95bb129947a" alt="Image" />
</p>

---

# Design and Analysis
-  Design Overview 
   - (W/L) ratio of M3,M4 is found using ICMR(+) <br> 
   - (W/L) ratio of M1,M2 is found using GBW <br>
   - I5 is found using Slew Rate <br>
   - (W/L) ratio of M5 is found using ICMR(-) <br>
   - (W/L) ratio of M6 is found from Gain and design of M3, M4 <br>

# Schematic

![2_SOPAMP_Sch](https://github.com/khajamufaqqamuddin-pixel/Miller-Compensated-Two-Stage-OPAMP-Using-Cadence-Virtuoso/blob/main/Schmetics/2_SOPAMP_Sch.png)

![AC_DC_Analysis](https://github.com/khajamufaqqamuddin-pixel/Miller-Compensated-Two-Stage-OPAMP-Using-Cadence-Virtuoso/blob/main/Schmetics/AC_DC_Analysis.png) 

# Gain and Phase Margin
- Achieved specifications:
  - DC gain: 64 dB, GBW : 34 MHz, Phase Margin: 59°,  Slew Rate: 38.72u V/sec
<p align="center">
  <img src="https://github.com/khajamufaqqamuddin-pixel/Miller-Compensated-Two-Stage-OPAMP-Using-Cadence-Virtuoso/blob/main/Plots/VCM_0.5_plot.png" />
</p>

# SlewRate

<p align="center">
  <img src="https://github.com/khajamufaqqamuddin-pixel/Miller-Compensated-Two-Stage-OPAMP-Using-Cadence-Virtuoso/blob/main/Plots/Slewate_plot.png" />
</p>

<p align="center">
  <img src="https://github.com/khajamufaqqamuddin-pixel/Miller-Compensated-Two-Stage-OPAMP-Using-Cadence-Virtuoso/blob/main/Plots/SlewRate_Cacl.png" />
</p>




## 👤 Author

**Khaja Mufaqqam Uddin**  
Analog CMOS Design

