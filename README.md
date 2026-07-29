# Energy Generation & Transmission Planning (Gümüşhane Region)

This repository contains the analysis, load planning, and evaluation of energy generation strategies for the **Gümüşhane region**. Using an energy system simulator, this project establishes a mix of renewable energy sources (Solar, Wind, and Hydroelectric) to meet hourly peak loads across different seasons (specifically comparing winter and summer profiles).

> **Course:** EEM0311 - Energy Generation and Transmission  
> **Institution:** Bursa Technical University – Electrical & Electronics Engineering  
> **Author:** Jess Edmond Razafimanovolily  
> **Academic Advisor:** Asst. Prof. Dr. İbrahim Gürsü TEKDEMİR  

---

## 📋 Overview

Energy demand fluctuates across hours of the day and months of the year. This study models a total installed capacity of **2,626.85 MW** across 6 power plants to satisfy hourly demand profiles for two representative days:
* **Winter Peak:** January 10, 2025
* **Summer Peak:** July 11, 2025

---

## ⚡ Installed Capacity Breakdown

The generation fleet consists of 6 power plants integrated with weather data files (JSON format) matching specific regional conditions:

| No | Power Plant Name | Plant Type | Capacity (MW) | Weather Dataset |
|---|---|---|---|---|
| 1 | Solar Power Plant (GES) | Solar | 80.00 | `Hava_durumu_bingöl_10-01-2025.json` |
| 2 | Kangal Wind Power Plant (Hybrid Solar) | Solar/Hybrid | 40.00 | `Hava_durumu_sivas_10-01-2025.json` |
| 3 | Soğanlı Wind Power Plant | Wind | 30.00 | `Hava_durumu_bayburt_10-01-2025.json` |
| 4 | Yukarı Kaleköy Hydroelectric Power Plant | Hydroelectric | 626.85 | `Hava_durumu_bingöl_10-01-2025.json` |
| 5 | Karakaya Hydroelectric Power Plant | Hydroelectric | 1,800.00 | `Hava_durumu_elazığ_10-01-2025.json` |
| 6 | Solar Power Plant (GES 2) | Solar | 50.00 | `Hava_durumu_bursa_10-01-2025.json` |
| **Total** | | | **2,626.85 MW** | |

---

## 📊 Key Results & Key Findings

### 1. Load Demand vs. Installed Capacity
The installed total power (**2,626.85 MW**) successfully covers the monthly peak power demand for all 12 months, with the maximum peak occurring in July (**2,241.8 MW**).

### 2. Capacity Factor Analysis
Comparative capacity factor percentages show clear seasonal shifts:

| Power Plant | Jan 10 (%) | Jul 11 (%) |
|---|---|---|
| Solar Power Plant (80 MW) | 12.53% | 31.80% |
| Kangal Hybrid GES (40 MW) | 12.50% | 36.15% |
| Soğanlı Wind Power Plant (30 MW) | 2.07% | 6.81% |
| Yukarı Kaleköy Hydroelectric (626.85 MW) | 100.00% | 100.00% |
| Karakaya Hydroelectric (1800 MW) | 53.01% | 54.74% |
| GES (50 MW) | 11.48% | 33.63% |

### 3. Base Load Power Plant
* **Karakaya Hydroelectric Power Plant** acts as the primary **base load provider**, supplying over **50% to 67%** of the total energy demand every single hour of the day in both summer and winter seasons.

---

## 📈 Summary Visualizations

- **Winter Simulation (Jan 10):** Generation accurately tracks the morning and evening peaks (hovering around 1,500 – 1,800 MWh).
- **Summer Simulation (Jul 11):** High solar irradiance boosts capacity factors above 30-36%, supporting higher summer cooling load demands (peaking above 2,000 MWh).

---

## 🛠️ Requirements & Setup

To run or replicate the planning simulations:
1. Ensure you have access to the energy planning/carbon simulation tool used in the course.
2. Load the corresponding hourly load data for January 10 and July 11.
3. Import the weather JSON datasets:
   * `Hava_durumu_bingöl_10-01-2025.json`
   * `Hava_durumu_sivas_10-01-2025.json`
   * `Hava_durumu_bayburt_10-01-2025.json`
   * `Hava_durumu_elazığ_10-01-2025.json`
   * `Hava_durumu_bursa_10-01-2025.json`
