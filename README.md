# 🫀 Predictive Heart Disease Diagnostics Using SVMs

Welcome to **HeartCare Project**, a project leveraging **Support Vector Machine (SVM)** models to predict cardiovascular risks. This repository provides an innovative approach to diagnosing heart disease using statistical optimization and predictive modeling.

---

## 🚀 Overview

This project addresses the growing demand for accurate diagnostics in healthcare systems. Using historical patient data like **Age**, **Blood Pressure**, **Cholesterol Levels**, and **Maximum Heart Rate**, we developed three SVM models to classify patients as either at risk or not at risk of heart disease.

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

## 📊 Dataset Details

This project leverages historical patient data for analysis and modelling. The dataset includes key features recorded from past medical diagnoses and clinical observations. The project uses this historical data to establish patterns and predictive capabilities for identifying cardiovascular risks.

The dataset used for this project includes the following features:

- **Age**: Patient's age in years.
- **Resting Blood Pressure (BP)**: Systolic blood pressure measured at rest (mmHg).
- **Cholesterol**: Serum cholesterol level (mg/dL).
- **Maximum Heart Rate (MaxHR)**: Maximum heart rate achieved during exercise.
- **Diagnosis (Label)**:
  - `+1`: Indicates the presence of heart disease.
  - `-1`: Indicates no heart disease.

### Dataset Splits:
- **Training Data**:
  - Used to train the SVM models.
  - Contains labelled data for supervised learning.
- **Test Data**:
  - Used to validate the models' performance on unseen data.
- **Semi-Supervised Data**:
  - Includes a mix of labelled and unlabeled data to simulate real-world scenarios where some diagnoses are unknown.

---

## 📊 Results & Insights

![Model Accuracy Chart](images/model_accuracy_chart.png)

- **Accuracy**:
  - SVM2: 84% on training data, 68% on test data.
  - SVM3: Slightly higher complexity but comparable accuracy.
- **Optimal Regularization Parameter (\( \lambda \))**:
  - SVM2: \( \lambda = 1000 \) - This value balances a wide margin with minimal misclassifications.
  - SVM3: \( \lambda = 50 \) - A smaller value suitable for mixed labeled and unlabeled datasets.

**Conclusion**: SVM2 was selected for its simplicity, robustness, and reliable optimization, making it the most practical choice for this diagnostic task.

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

### Additional Insights:
From the "\( \lambda \) vs Accuracy" analysis sheet in the dataset, the classification rates consistently peaked at optimal \( \lambda \) values (SVM2: 1000, SVM3: 50), showing a balance between overfitting and underfitting.

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
2. **Open the Excel File**: Navigate to the repository folder, locate the Excel file, and open it. The file contains the dataset and pre-configured Solver settings necessary for running the SVM models.
3. **Test Your Data**:
   Replace the sample data with your own dataset to validate predictions.
4. **Enable Solver Add-In**:
   - Navigate to Excel options.
   - Under Add-Ins, activate Solver.
   - Ensure Solver settings match those provided in the project documentation.

### Example Input & Output:
Input sample:
```
Age: 55
BP: 140
Cholesterol: 220
MaxHR: 150
```
Output:
```
Prediction: +1 (Heart Disease)
```

---

## 🔮 Future Scope

- Transition to advanced tools like **Python** and **scikit-learn**.
- Include additional risk factors for more robust diagnostics.
- Build a web-based application for real-time usage.
- Utilize larger datasets for extended testing and validation.
- Integrate a grid search approach for hyperparameter tuning.

---
