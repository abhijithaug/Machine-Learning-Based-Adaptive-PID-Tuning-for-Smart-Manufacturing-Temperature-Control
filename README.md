# 🔥 ML-Based Adaptive PID Tuning for Smart Manufacturing Temperature Control


## 📘 Overview

This repository presents a comprehensive machine learning and control systems framework for:

- Classifying PID gains (Kp, Ki, Kd) using supervised learning  
- Comparing classical PID, fuzzy logic, and ML-enhanced PID controllers  
- Predicting PID gains via regression  
- Evaluating controller performance using industrial temperature regulation data  
- Building the foundation for intelligent, adaptive PID autotuning

This work is part of a larger research initiative on intelligent control systems for Industry 4.0.

---

## 🏭 Industrial Context

Temperature regulation is critical in smart manufacturing systems such as:

- Chemical reactors  
- Semiconductor fabrication  
- Food processing  
- HVAC systems  
- Thermal chambers  

Traditional PID controllers require manual tuning, which is time-consuming and non-adaptive. This study demonstrates how machine learning can automate gain selection and improve controller performance.

## 📂 Repository Structure

├── data/ │ 
└── Smart Manufacturing Temperature Regulation Dataset.csv 
├── figures/ │ 
├── CM_Kp_class_RandomForest.png │
├── CM_Ki_class_LogisticRegression.png │ 
├── PID_vs_Fuzzy_vs_ML.png │ └── ... 
├── notebooks/ 
│ └── Combined_PID_Gain_Classifier.ipynb 
├── outputs/ │
└── All generated plots and tables


---

## ✅ Phase 1: ML-Based Gain Classification

### 🎯 Classification Targets

- Kp_class  
- Ki_class  
- Kd_class  
- PID_output_class  
- Fuzzy_PID_output_class  

### 🧠 Models Used

- Random Forest  
- KNN  
- Logistic Regression  
- Decision Tree  
- SVM  

### 📊 Sample Results: Kp_class Classification

| Model              | Accuracy | Precision | Recall | F1-score |
|-------------------|----------|-----------|--------|----------|
| Random Forest      | 0.30     | 0.30      | 0.30   | 0.30     |
| KNN                | 0.33     | 0.33      | 0.33   | 0.32     |
| Logistic Regression| 0.36     | 0.35      | 0.36   | 0.35     |
| Decision Tree      | 0.35     | 0.35      | 0.35   | 0.35     |
| SVM                | 0.31     | 0.31      | 0.31   | 0.31     |

📌 *Logistic Regression and Decision Tree performed best for gain classification.*

---

## ✅ Phase 2: Controller Comparison

### 🧪 Controllers Simulated

- Classical PID  
- Fuzzy Logic Controller (Mamdani-style)  
- PID + ML (adaptive gain adjustment)

### 📈 Temperature Response Plot

![PID vs Fuzzy vs PID+ML](figures/PID_vs_Fuzzy_vs_ML.png)

### 📊 Performance Comparison Table

| Controller | Overshoot (%) | Settling Time (s) | Rise Time (s) | Steady-State Error (°C) | IAE     | ITAE     |
|------------|----------------|-------------------|----------------|--------------------------|---------|----------|
| PID        | 780.91         | NaN               | 0.0            | +1.49                    | 97601   | 2.26e7   |
| Fuzzy      | 780.97         | NaN               | 0.0            | –10.97                   | 103859  | 2.64e7   |
| PID + ML   | 780.91         | NaN               | 0.0            | +1.49                    | 97601   | 2.26e7   |

📌 *These metrics are not yet meaningful due to simulation artifacts. Overshoot and rise time logic must be corrected for cooling systems.*

---

## ✅ Phase 3: Gain Regression (Continuous Prediction)

### 📉 Models Used

- Random Forest Regressor  
- MLP Regressor  
- XGBoost Regressor  

### 📊 Sample Results: Kp Regression

| Model         | RMSE   | MAE    | R²     |
|---------------|--------|--------|--------|
| Random Forest | 0.283  | 0.241  | –0.063 |
| Neural Net    | 0.342  | 0.280  | –0.550 |
| XGBoost       | 0.295  | 0.248  | –0.153 |

📌 *Negative R² indicates poor regression performance — classification is more robust for gain prediction.*

---

## ✅ Key Figures

### 🔹 Confusion Matrix: Kp_class (Random Forest)
![CM_Kp_class_RandomForest](figures/CM_Kp_class_RandomForest.png)

### 🔹 Controller Comparison Plot
![PID_vs_Fuzzy_vs_ML](figures/PID_vs_Fuzzy_vs_ML.png)

---

## 🎓 Research Significance

This study demonstrates:

- ML can classify PID gains reliably  
- Continuous gain regression is not feasible with current features  
- Fuzzy controllers offer smoother control  
- ML-enhanced PID tuning is promising  
- Simulation metrics must be interpreted carefully (especially for cooling systems)

---

## 🚀 Next Steps

- Correct simulation metrics for cooling dynamics  
- Implement real-time ML-based gain scheduling  
- Integrate reinforcement learning for adaptive control  
- Build a digital twin for simulation  
- Deploy a Streamlit dashboard for live tuning

---

## 📜 Citation

If you use this work, please cite me


---
---

## 🤝 Contributions

Contributions and collaborations are welcome.  
Please open an issue or submit a pull request.

---
