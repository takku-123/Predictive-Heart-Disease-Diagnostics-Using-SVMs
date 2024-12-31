# Predictive-Heart-Disease-Diagnostics-Using-SVMs
# 🫀 Predictive Heart Disease Diagnostics Using SVMs

Welcome to **HeartCare**, a project designed to leverage **Support Vector Machine (SVM)** models for predicting cardiovascular risks. This repository showcases an innovative approach to diagnosing heart disease using statistical optimization and predictive modelling.

---

## 📋 Overview

The project was born from a need to address the increasing burden on healthcare systems, particularly in detecting cardiovascular diseases. Using patient data like **Age**, **Blood Pressure**, **Cholesterol Levels**, and **Maximum Heart Rate**, we have constructed three SVM models to classify patients as either at risk or not at risk of heart disease.

![Heart Diagnosis Process](images/heart_diagnosis_process.png)

### Models Implemented:
1. **Hard Margin Supervised SVM** (SVM1): Assumes data is linearly separable, failed in this case.
2. **Soft Margin Supervised SVM** (SVM2): Allows some misclassification to achieve better generalization.
3. **Soft Margin Semi-Supervised SVM** (SVM3): Predicts unlabelled data while optimizing parameters for labelled data.

---

## 🔍 Key Features
- **Data-Driven Decision Support**: Predicts heart disease likelihood based on patient metrics.
- **Customizable Thresholds**: Fine-tuned regularization parameters (λ) to balance precision and generalization.
- **Scalability**: Easily extendable to include additional risk factors or adapt to larger datasets with advanced tools.

---

## 🛠️ Technical Description

### Model Architecture
- **Hard Margin SVM (SVM1)**: Tried to separate the data linearly but was infeasible due to overlapping classes.
- **Soft Margin SVM (SVM2)**: Introduced a regularization parameter `λ` to handle misclassifications and improve robustness.
- **Semi-Supervised SVM (SVM3)**: Utilized binary variables for unlabelled data to predict missing diagnoses.

![SVM Model Flowchart](images/svm_model_flowchart.png)

### Data Input:
- Patient Risk Factors: **Age**, **Resting Blood Pressure**, **Cholesterol**, **Maximum Heart Rate**.
- Labels: **+1** (Heart Disease) or **-1** (No Heart Disease).

### Mathematical Model:
The decision boundary is modeled as:
\[
f(x) = w_1 \cdot \text{Age} + w_2 \cdot \text{BP} + w_3 \cdot \text{Cholesterol} + w_4 \cdot \text{Max HR} + b
\]
Where:
- \( w_1, w_2, w_3, w_4 \): Coefficients (calculated weights).
- \( b \): Intercept.
- \( f(x) > 0 \): No Heart Disease.
- \( f(x) < 0 \): Heart Disease.

### Results:
- **SVM2** was chosen due to its simplicity, robustness, and global optimization.
- Achieved **84% accuracy** on training data and **68% accuracy** on test data.

### Implementation Tools:
- **Microsoft Excel**: Used for data preprocessing and model implementation.
- **Solver Add-In**: Optimized the mathematical equations for each model.

---

## 📊 Results & Insights
![Results Chart](images/results_chart.png)

- **Accuracy**: SVM2 provided reliable predictions with minimal overfitting.
- **Regularization Parameter (λ)**: Fine-tuned for balance between model complexity and classification accuracy.
   ```bash
   git clone https://github.com/your-username/HeartCareAI.git
