# Fraudulent Detection Project Summary

This project involves building and tuning a Random Forest model to detect fraudulent transactions. The steps include data preparation, model building, tuning, and interpretability analysis.

## Steps of Analysis

### **1. Reading Data**
- **Task:** Load and preprocess the dataset for analysis.

### **2. Class Separability Analysis**

### **3. Building a Random Forest Model**
- **Initial Model Performance:**
  - **Training Set Accuracy:** `1.0`
  - **Test Set Accuracy:** `0.7857142857142857`
  - **Confusion Matrices:**
    - **Training:** `[[9632, 0], [0, 16]]`
    - **Test:** `[[4121, 0], [6, 8]]`
  - **Implication:** High training accuracy suggests overfitting; lower test accuracy indicates need for model tuning.

### **4. Model Tuning**
- **Round 1: Tuning 'n_estimators' and 'max_depth'**
  - **Best Parameters:** `{'max_depth': 20, 'n_estimators': 150}`
  - **Score:** `0.9020957672003872`
- **Round 2: Tuning 'min_samples_split' and 'min_samples_leaf'**
  - **Best Parameters:** `{'min_samples_leaf': 4, 'min_samples_split': 2}`
  - **Score:** `0.9469309133248367`
  - **Implication:** Successive tuning rounds improved model performance and robustness.

### **5. Permutation Importance for Model Interpretability**
- **Top 5 Features:**
  - **V17:** `0.001693`
  - **V14:** `0.000701`
  - **V12:** `0.000459`
  - **V16:** `0.000242`
  - **V4:**  `0.000242`
- **Implication:** These features are most influential in the model's predictions, highlighting key factors in detecting fraudulent transactions.
