# Machine Learning for Student Performance Prediction

## 📌 Project Overview
This repository contains the data science pipeline and research findings from my Master's Thesis in **Data Science and Engineering** at **Politecnico di Torino**

The project addresses the challenge of early performance prediction in engineering education by combining educational technology with advanced machine learning.It utilizes a custom **Moodle-based check-in/checkout system** to collect behavioral data and support self-regulated learning.

---

## 🎓 Thesis Details
* **Title:** Machine Learning for Student Performance Prediction.
* **Author:** Hamed Goldoust.
* **Supervisors:** Prof. Paolo Giaccone and Prof. Paolo Manfredi.
* **Institution:** Politecnico di Torino, Electronics and Telecommunications Department (DET).
* **Academic Year:** 2025-2026.

---

## 🚀 Key Research Findings
* **Predictive Power:** For students initially scoring below the performance threshold (80% or 70%), the models achieved $R^{2}$ values exceeding **0.98**, allowing for highly accurate early intervention.
* **The "Improvement Efficiency" Metric:** This derived feature, measuring how well students close their personal knowledge gaps, was identified as the **strongest predictor** of final success for at-risk students across all datasets.
* **Universal Behavioral Indicators:** Assessment timing metrics—such as the percentage of available time used (`duration_norm_checkin`) and time management efficiency—consistently emerged as top predictors for the entire student cohort.
* **Generalization vs. Complexity:** Resubstitution analysis demonstrated that **Linear Models** (Lasso, Ridge, Logistic Regression) generalize better to new student groups, while complex tree-based models (Random Forest) are prone to significant overfitting in educational contexts.

---

## 🛠️ Machine Learning Pipeline
The framework implements a modular pipeline designed for educational data mining:

1.  **Data Extraction:** Automated logging of Moodle events, including quiz interactions, video engagement, and navigation patterns.
2.  **Feature Engineering:** Conversion of raw logs into pedagogically meaningful metrics like `improvement_efficiency` and `timing_strategy_change`.
3.  **Preprocessing:** * **Outlier Treatment:** Applied via **Winsorization** to mitigate the impact of unconventional study habits.
    * **Scaling:** Utilization of the **Yeo-Johnson** Power Transformer to normalize skewed temporal distributions.
4.  **Modeling & Optimization:** * **Regression:** Lasso, Ridge, Random Forest, Gradient Boosting, and SVR.
    * **Classification:** Logistic Regression, Random Forest, and Gradient Boosting to categorize students into grade ranges.
    * **Tuning:** Systematic grid search with 5-fold cross-validation.

---

## 📊 Experimental Setup
The models were rigorously tested across four different course implementation datasets:
* **Module 1 & 2:** Targeted students scoring initially under 80.
* **Module 3 & 4:** Targeted students scoring initially under 70.
* **Evaluation Metrics:** RMSE, MAE, $R^{2}$, and Relative Mean Squared Error (RelMSE).

---



## ⚖️ Ethical Considerations
To ensure fair and responsible AI in education, this project incorporates:
* **Anonymization:** Student identifiers are secured using SHA-256 hashing.
* **Bias Mitigation:** Use of balanced datasets and fair feature selection to treat all students equitably.
* **Interpretability:** Preference for models that provide clear, actionable insights for pedagogical intervention.

---
*This work contributes to the field of learning analytics by enabling evidence-based practices to foster learning success in higher education.*
