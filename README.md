# 🏦 Loan Approval Prediction

## 📌 Project Overview
This project aims to build a machine learning model to automate the loan approval process. Traditional loan approval is time-consuming, prone to human error, and can lead to inconsistent decision-making. By using data-driven predictions, banks and financial institutions can improve efficiency, accuracy, and fairness.

---

## 📁 Dataset
The dataset includes information about applicants such as:
- Demographic data (education, self-employed status, etc.)
- Financial metrics (income, loan amount, loan term)
- Credit behavior (previous defaults, existing loans)

**Target column:** `loan_status`  
- `1`: Loan Approved  
- `0`: Loan Rejected

---

## 🔧 Technologies Used
- Python
- Pandas & NumPy (Data preprocessing)
- Scikit-learn (Modeling & Evaluation)
- Jupyter Notebook / Python script

---

## ⚙️ Project Steps

### 1. **Data Cleaning**
- Removed leading/trailing whitespaces from column names
- Converted target labels (`approved`/`rejected`) to numerical format
- Dropped missing target values

### 2. **Feature Encoding**
- Categorical columns like `education` and `self_employed` were label encoded.

### 3. **Missing Value Imputation**
- Numerical columns filled with median values.

### 4. **Feature Scaling**
```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
X[numerical_features] = scaler.fit_transform(X[numerical_features])
