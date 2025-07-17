# lendingclub-loan-prediction
Machine learning classification project using a Random Forest model to predict whether a borrower will repay their loan in full, based on real LendingClub data (2007–2010). The project explores financial and credit factors that influence loan defaults, using Scikit-learn and Python. Includes EDA, model evaluation, and performance analysis.
# 🔍 LendingClub Loan Default Prediction (Random Forest)

This project explores loan data from [LendingClub.com](https://www.lendingclub.com/), a peer-to-peer lending platform. The objective is to build a machine learning classification model to **predict whether a borrower will pay back their loan in full** or not.

---

## 📁 Dataset Overview

We used a cleaned dataset containing loan information from **2007 to 2010**, before LendingClub became a public company.

Each row represents a borrower with various financial and credit features. The goal is to classify the borrower as either:
- `0` → Fully paid back the loan
- `1` → Did **not** fully pay back the loan

---

## 📊 Features

Here are some of the most important columns in the dataset:

| Feature | Description |
|--------|-------------|
| `credit.policy` | 1 if the customer meets LendingClub's credit criteria, 0 otherwise |
| `purpose` | Purpose of the loan (e.g., debt consolidation, credit card, small business) |
| `int.rate` | Interest rate of the loan (e.g., 0.11 = 11%) |
| `installment` | Monthly payment for the loan |
| `log.annual.inc` | Natural log of annual income |
| `dti` | Debt-to-income ratio |
| `fico` | FICO credit score |
| `days.with.cr.line` | Days the borrower has had a credit line |
| `revol.bal` | Borrower's revolving credit balance |
| `revol.util` | Utilization rate of revolving credit |
| `inq.last.6mths` | Credit inquiries in last 6 months |
| `delinq.2yrs` | Past due payments in last 2 years |
| `pub.rec` | Number of public derogatory records (bankruptcies, liens, etc.) |

---

## ✅ Model Used

We used two classification models:
- **Decision Tree Classifier**
- **Random Forest Classifier**

Our primary focus was the **Random Forest** model due to its superior performance.

---

## 📈 Results

### 🔹 Decision Tree Classifier

- **Accuracy:** ~72%
- **F1-Score (Defaulters):** 0.21
Confusion Matrix:
[[1980 451]
[ 340 103]]

Classification Report:
precision recall f1-score support
0 0.85 0.81 0.83 2431
1 0.19 0.23 0.21 443


---

### 🔹 Random Forest Classifier

- **Accuracy:** ~85%
- **F1-Score (Defaulters):** 0.04

Confusion Matrix:
[[2425 6]
[ 435 8]]

Classification Report:
precision recall f1-score support
0 0.85 1.00 0.92 2431
1 0.57 0.02 0.04 443

## 📌 Observations

- While the **Random Forest** model achieved **85% overall accuracy**, it performed **very poorly in detecting defaulters**.
- The model was **highly biased toward predicting loan repayment** (class `0`), failing to catch most borrowers who defaulted.

---

## 📦 Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- Jupyter Notebook

---

## 📁 File Structure

├── Random Forest Project.ipynb # Jupyter notebook with full analysis
├── loan_data.csv # Cleaned LendingClub loan dataset
└── README.md # Project summary

yaml
Copy
Edit

---

## 📚 Acknowledgements

- Data source: [LendingClub Public Loan Data](https://www.lendingclub.com/)
- Project inspired by data science classification use-cases.

---

## 📌 License

This project is open for educational and non-commercial use.
