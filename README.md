# 🏦 Loan Approval Prediction - EDA & Machine Learning

This project performs **Exploratory Data Analysis (EDA)** and builds a **Random Forest Classifier** to predict loan approval status using a real-world dataset.

---

## 📁 Dataset Overview

The dataset includes the following features:

- Applicant demographics: Age, Gender, Education, Income, Employment
- Financial behavior: Home Ownership, Loan Amount, Loan Intent, Interest Rate, Credit Score
- Target Variable: `loan_status` (1 = Approved, 0 = Not Approved)

---

## 🧹 Data Cleaning

- No missing values detected.
- All categorical columns encoded using `LabelEncoder`.
- Numerical and categorical features handled appropriately for model training.

---

## 📊 Exploratory Data Analysis (EDA)

### 🔹 Target Distribution
- Slight imbalance in loan approvals:
  - **Passed**: 80%
  - **Not Passed**: 20%

### 🔹 Key Insights

| Feature             | Passed (Avg)     | Not Passed (Avg) |
|---------------------|------------------|------------------|
| Income              | \$59,886         | \$86,157         |
| Loan Amount         | \$10,856         | \$9,220          |
| Interest Rate       | 12.86%           | 10.48%           |
| Credit Score        | 631.89           | 632.81           |

- **Higher-income applicants are more likely to be rejected**, possibly due to larger or riskier loan requests.
- **Loan purpose (intent), education, and home ownership** also show visible patterns in approval trends.

---

## 🤖 Predictive Modeling

### Model: `RandomForestClassifier`

- Categorical features encoded
- Data split: 80% Train / 20% Test

### ✅ Performance Summary

**Accuracy:** `92.87%`

**Classification Report:**

| Class       | Precision | Recall | F1-Score | Support |
|-------------|-----------|--------|----------|---------|
| Not Passed  | 0.94      | 0.97   | 0.95     | 6990    |
| Passed      | 0.89      | 0.78   | 0.83     | 2010    |

- **Macro Avg F1-Score:** 0.89
- **Weighted Avg F1-Score:** 0.93

### 🔍 Observations:
- The model performs **very well on identifying rejected applications**, but has slightly lower recall for approved ones.
- Overall, the model is **well-balanced and reliable** for deployment or business use cases.

---

## 📈 Future Improvements

- Address class imbalance with **SMOTE or class weighting**
- Try **XGBoost** or **Logistic Regression** for comparison
- Perform **hyperparameter tuning** with `GridSearchCV`
- Improve recall for the "Passed" class

---

## 🧠 Tools & Libraries Used

- Python, Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn (RandomForestClassifier, LabelEncoder, train_test_split)

---

## ✅ Conclusion

This project demonstrates the full data science workflow — from data cleaning and exploration to model training and evaluation — for predicting loan approvals using a structured dataset.
