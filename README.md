# 🧠 Employee Attrition Prediction

This project enables **Salifort Motors** to detect employees at high risk of attrition by analyzing structured HR data and deploying an interpretable machine learning model. The objective is to equip HR with actionable intelligence to **reduce turnover**, improve retention, and optimize workforce planning.

---

## 🔍 Project Overview

### 🎯 Objective
Develop a predictive analytics pipeline to identify patterns in employee behavior and forecast attrition using logistic regression for high interpretability.

### 🧰 Tools & Technologies
- **Python:** Pandas, NumPy, Seaborn, Scikit-learn  
- **Modeling:** Logistic Regression  
- **Data Processing:** One-Hot Encoding, SMOTE (Synthetic Minority Over-sampling Technique)  
- **Evaluation Metrics:** ROC-AUC, Confusion Matrix, Classification Report  

---

## 🔎 Insights from Correlation Analysis

<img width="1622" height="690" alt="Screenshot (456)" src="https://github.com/user-attachments/assets/008c557c-9401-4e0b-8b7f-199c45776190" />

- **Top Negative Correlations** (indicate reduced risk of attrition):
  - `satisfaction_level`: -0.36 — strong inverse relation with attrition
  - `work_accident`: -0.1 — employees with accidents are more likely to stay
- **Top Positive Correlations** (indicate increased attrition risk):
  - `time_spend_company`: +0.2 — risk increases with tenure length
  - `salary_low`: +0.15 — low salary is positively associated with attrition
  - `average_monthly_hours`: +0.12 — high workloads contribute to resignations

**Thresholds**: Variables with correlation magnitude > 0.1 were considered significant for modeling.

---

## 🧪 Model Evaluation

### 🟠 ROC-AUC Curve

<img width="1120" height="691" alt="Screenshot (457)" src="https://github.com/user-attachments/assets/cf3e0e00-1e54-468e-b8f9-f2d1e29a6c8e" />

- **AUC = 0.82**  
  Demonstrates strong discriminative power of the logistic regression model in separating at-risk employees from retained ones.

### 📉 Confusion Matrix & Classification Report

<img width="736" height="708" alt="Screenshot (458)" src="https://github.com/user-attachments/assets/f15c7b5c-d124-4d14-ae8c-8c28f71cb790" />

| Metric         | Value  |
|----------------|--------|
| **Accuracy**   | 0.79   |
| **Recall (Left)** | 0.80   |
| **Precision (Left)** | 0.42   |
| **F1-Score (Left)** | 0.55   |

- High **recall** for class 1 (left) ensures most at-risk employees are detected.
- Moderate **precision** indicates room for improving false positive reduction (e.g., model tuning or thresholding).

---

## 📈 Key Findings

- **Satisfaction level** is the most predictive feature; low satisfaction strongly correlates with attrition.
- Employees with **low salary**, **long tenure**, and **high workload** are significantly more likely to leave.
- Departments such as **RandD** and **support** show slight variations but no major standalone impact.

---

## 💼 Business Implications

- **Retention Strategy Design**: Prioritize interventions for employees with low satisfaction and high project load.
- **Compensation Restructuring**: Focus on employees in the lowest salary band.
- **Workload Management**: Reduce excessive working hours to mitigate burnout and disengagement.

---

## 🧠 Skills Demonstrated

- Translating HR problems into predictive ML solutions
- Correlation-driven feature selection and interpretation
- Handling imbalanced classification tasks with SMOTE
- Communicating technical results to non-technical stakeholders

---

## 📌 Next Steps

- Deploy threshold-tuned version of the model in HR dashboards
- Integrate model into employee management systems for real-time alerts
- Explore ensemble models (e.g., Random Forest, XGBoost) to improve precision

---

