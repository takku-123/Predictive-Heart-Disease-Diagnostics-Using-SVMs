# 🫀 Predictive Heart Disease Diagnostics Using SVMs

Welcome to **HeartCareAI**, a project leveraging **Support Vector Machine (SVM)** models to predict cardiovascular risks. This repository provides an innovative approach to diagnosing heart disease using statistical optimization and predictive modeling.

---

## 🚀 Overview

This project addresses the growing demand for accurate diagnostics in healthcare systems. Using patient data like **Age**, **Blood Pressure**, **Cholesterol Levels**, and **Maximum Heart Rate**, we developed three SVM models to classify patients as either at risk or not at risk of heart disease.

![Heart Diagnosis Process](images/heart_diagnosis_process.png)

### Implemented Models:
1. **Hard Margin Supervised SVM (SVM1)**: Assumes linearly separable data (failed in this case).
2. **Soft Margin Supervised SVM (SVM2)**: Allows misclassifications for better generalization.
3. **Soft Margin Semi-Supervised SVM (SVM3)**: Predicts unlabelled data while optimizing parameters for labeled data.

---

## 🔑 Key Features

- **Data-Driven Decision Support**: Predicts heart disease likelihood based on patient metrics.
- **Customizable Regularization**: Fine-tuned parameter (\( \lambda \)) to balance precision and generalization.
- **Scalability**: Extendable to include additional risk factors and handle larger datasets.

---

## 📊 Results & Insights

![Model Accuracy Chart](images/model_accuracy_chart.png)

- **Accuracy**:
  - SVM2: 84% on training data, 68% on test data.
  - SVM3: Slightly higher complexity but comparable accuracy.
- **Optimal Regularization Parameter (\( \lambda \))**:
  - SVM2: \( \lambda = 1000 \)
  - SVM3: \( \lambda = 50 \)

**Conclusion**: SVM2 was selected for its simplicity, robustness, and reliable optimization.

---

## ⚙️ Technical Details

### Input Data:
- **Features**: Age, Resting Blood Pressure, Cholesterol, Maximum Heart Rate.
- **Labels**: +1 (Heart Disease), -1 (No Heart Disease).

### Model Formulation:
The decision boundary is modeled as:
\[
    f(x) = w_1 \cdot \text{Age} + w_2 \cdot \text{BP} + w_3 \cdot \text{Cholesterol} + w_4 \cdot \text{MaxHR} + b
\]
Where:
- \( w_1, w_2, w_3, w_4 \): Coefficients (weights).
- \( b \): Intercept.

- \( f(x) > 0 \): No Heart Disease.
- \( f(x) < 0 \): Heart Disease.

### Implementation Tools:
- **Microsoft Excel Spreadsheets**: For data preprocessing and modeling.
- **Solver Add-In**: Optimized mathematical equations for each model.

---

## 💻 Getting Started

### Prerequisites:
- **Microsoft Excel** (with Solver Add-In installed).
- Basic knowledge of machine learning concepts.

### Steps:
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/takku-123/Predictive-Heart-Disease-Diagnostics-Using-SVMs.git
   ```
2. **Open the Excel File**:
   Use the provided sample dataset and Solver configuration to explore the models.
3. **Test Your Data**:
   Replace the sample data with your own dataset to validate predictions.

---
