# 🔥 ML-Based Adaptive PID Tuning for Smart Manufacturing Temperature Control

## 📌 Overview
This repository presents a **machine learning–driven framework for adaptive PID tuning** in a smart manufacturing temperature regulation system.  
The study compares **Classical PID**, **Fuzzy PID**, and **ML-assisted PID** approaches using real industrial-style production data.

Unlike idealized simulations, this dataset reflects **real operating conditions**, including noise, non-stationarity, and the absence of controlled step inputs.

---

## 🎯 Objectives
- Classify PID gains (`Kp`, `Ki`, `Kd`) into **Low / Medium / High**
- Compare multiple ML classifiers for PID gain selection
- Compare **PID vs Fuzzy PID vs ML-PID** control outputs
- Explore feasibility of **continuous PID gain regression**
- Evaluate controller performance using **control-theoretic metrics**
- Identify limitations of production data for classical control analysis

---

## 📊 Dataset Description
**Smart Manufacturing Temperature Regulation Dataset**

| Category | Variables |
|--------|----------|
| Process | Current Temperature, Ambient Temperature, Humidity |
| Control | PID Control Output, Fuzzy PID Output |
| PID Gains | Kp, Ki, Kd |
| Engineered | Error lag, rolling means, temperature deltas |

> ⚠️ Data represents **production logs**, not controlled experiments.

---

## 🛠 Feature Engineering
The following dynamic features were created:
- Temperature error lag
- Temperature rate of change
- Rolling mean of PID output
- Ambient temperature variation

These features improved classification robustness and temporal awareness.

---

## 🤖 Machine Learning Models

### Classification
- Random Forest
- K-Nearest Neighbors
- Logistic Regression
- Decision Tree
- Support Vector Machine (RBF)

### Regression (Exploratory)
- Random Forest Regressor
- Neural Network (MLP)
- XGBoost Regressor

---

## 📈 PID Gain Classification Results

### Example: `Kp_class`

| Model | Accuracy | Precision | Recall | F1 |
|-----|----------|----------|-------|----|
| Random Forest | ⭐ Best | High | High | High |
| SVM | Moderate | Moderate | Moderate | Moderate |
| KNN | Lower | Lower | Lower | Lower |
| Logistic Regression | Low | Low | Low | Low |

📌 **Observation:**  
Tree-based models outperform linear models due to nonlinear process behavior.

---

## 📊 Multi-Target Model Comparison

Targets evaluated:
- `Kp_class`
- `Ki_class`
- `Kd_class`
- `PID_output_class`
- `Fuzzy_PID_output_class`

### Best Model per Target

| Target | Best Model |
|------|-----------|
| Kp_class | Random Forest |
| Ki_class | Random Forest |
| Kd_class | Random Forest |
| PID Output | Random Forest |
| Fuzzy PID Output | Random Forest |

### 📉 Model Comparison Figure
```text
outputs/Model_Comparison_All_Targets.png
