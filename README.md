# 🩺 Diabetes Prediction Using Machine Learning

Accurate and early prediction of diabetes is critical in preventing long-term complications and improving patient outcomes. This project leverages machine learning to develop an interpretable and accurate model for diabetes diagnosis using the **Pima Indians Diabetes Dataset**.

---

## 📊 Project Overview

This repository presents a complete machine learning pipeline for binary classification of diabetes presence (diabetic vs non-diabetic). It follows a structured data science approach:

- Exploratory Data Analysis (EDA)
- Data Preprocessing and Imputation
- Model Training (Logistic Regression, SVM, KNN)
- Addressing Class Imbalance with **SMOTE**
- Model Evaluation (Accuracy, Precision, Recall, Specificity, F1, AUC)
- Feature Significance and Interpretability

---

## 🧠 Tools & Libraries Used

- Python (NumPy, Pandas, Matplotlib, Seaborn)
- Scikit-learn
- imbalanced-learn (SMOTE)
- Jupyter Notebooks

---

## 🔬 Dataset Summary

- 📁 Records: 768
- 👩‍⚕️ Female patients aged 21+
- 🧬 Features: 8 health metrics (e.g., Glucose, BMI, Age)
- 🎯 Target: `Outcome` (0 = Non-Diabetic, 1 = Diabetic)
- ⚠️ Class Imbalance: 268 diabetic vs 500 non-diabetic

---

## 🔍 Exploratory Data Analysis Highlights

- Glucose and BMI are the strongest predictors of diabetes.
- Several features contain zeros that are not physiologically plausible (e.g., BMI = 0), flagged for imputation.
- A correlation heatmap and boxplots help visualize patterns and potential outliers.
- Feature significance tested using p-values and correlation metrics.

---

## 🤖 Model Performance

| Model               | Accuracy | Precision | Recall | F1 Score | AUC  |
|--------------------|----------|-----------|--------|----------|------|
| Logistic Regression | 75.7%    | 68%       | 62%    | 65%      | 0.73 |
| Logistic (SMOTE)    | 69%      | 56%       | 71%    | 63%      | ↑ Improved |
| SVM                 | 76.6%    | Similar   | Slightly Higher | Slightly Higher | ↓ Lower |

- **SMOTE** increased recall but reduced precision—more diabetic cases correctly identified at the cost of more false positives.
- Logistic regression performed well and is interpretable, while SVM gave slightly better accuracy but poorer AUC.
- Feature importance showed "Glucose", "BMI", and "Age" as top predictors (p < 0.05).

---

