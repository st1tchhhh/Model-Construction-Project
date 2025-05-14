# 🧠 Cognitive Performance Modeling Project

This repository contains the final project for STAT 425 (Spring 2025), conducted by Xiangchen Guo, Zijian Shen, and Sean Pang. The project explores how personal behaviors and environmental conditions affect cognitive performance — specifically, **reaction time** and **sleep duration** — using statistical modeling techniques.

---

## 📋 Project Overview

We investigated three central research questions:

1. Do fatigue, stress, and exercise significantly influence **reaction time**, and are the effects nonlinear?
2. Is there a relationship between **video game duration** and **sleep duration**, moderated by caffeine intake?
3. How do device type, network stability, and interface influence **cognitive task performance**?

---

## 📊 Dataset & Variables

- **Observations:** 145 respondents
- **Key variables:**  
  - `First`, `Second`, `Third` – reaction times across 3 trials  
  - `AvgSleepTime`, `LastNightSleep`, `HoursAweak`, `AvgHoursExercise`  
  - `Fatigue`, `Stress`, `CaffeinIntake`, `VideoGamePlay`, `InputDevice`, `DeviceOS`, `WiFi`, `RH` (handedness)

---

## 🧹 Data Preprocessing

- Recoded categorical variables into ordered factors (e.g., `Fatigue` into 3 levels)
- Created binary indicators (e.g., right-handed vs non-right-handed)
- Removed low-variance features
- Standardized structure for exploratory and regression modeling

---

## 📈 Exploratory Data Analysis

We visualized distributions and explored group-level differences:

- **Fatigue vs Reaction Time:** Higher fatigue levels correlate with slower and more inconsistent reaction times  
- **Device OS Distribution:** Majority of participants used Windows/macOS laptops  
- **Exercise vs Reaction Time:** Moderate weekly exercise is linked to better performance  

---

## 🔨 Model Construction

### ✅ Multiple Linear Regression

We modeled `First` (first reaction time) as a function of fatigue, stress, device type, refresh rate, input device, and other variables.

**Significant predictors:**
- Lower fatigue → faster response
- Right-handed participants → faster reaction time
- Mouse/touch screen vs keyboard → different impacts
- Poor WiFi & low screen refresh rate → slower response

📌 *Adjusted R²: 0.371 — model explains ~37% of the variance in reaction time*

---

### ✅ ANOVA: Sleep Duration Model

We examined the interaction between `VideoGamePlay` and `CaffeinIntake` on `AvgSleepTime`.

- **Video game duration** significantly affects sleep duration  
- **Caffeine intake** does **not** have a significant main or interaction effect  
- **Post-hoc (Tukey)**: “Once a week” game players sleep significantly less than daily gamers

---

## 🧪 Model Diagnostics

- Residuals are approximately normally distributed  
- No major violations of homoscedasticity or linearity assumptions  
- Variance inflation factors were within acceptable range

---

## ✅ Key Findings

- **Fatigue**, **stress**, **exercise**, and **right-handedness** are associated with cognitive performance  
- **Device type** and **WiFi stability** affect task execution time  
- **Video game duration** influences sleep, but caffeine’s effect is inconclusive  
- Individual behavior and environment both shape cognitive outcomes

---

## 📁 Files Included

- `FP_Code.Rmd` – full analysis code in R Markdown  
- `FP_Output.pdf` – output with all tables and plots  
- `FP_Report.pdf` – full project report with interpretation  
- `BG.docx` – background and problem statement

---

> 🧑‍🏫 Course: STAT 425 - Statistical Modeling I  
> 📆 Date: May 10, 2025  
> 👥 Team: Xiangchen Guo, Zijian Shen, Sean Pang
