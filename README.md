# CreditWise — Loan Approval Prediction

A Machine Learning project that explores applicant financial and demographic data to predict loan approval outcomes using classification algorithms.

## Project Overview

CreditWise analyzes applicant information such as income, credit score, existing loans, savings, loan amount, and other relevant attributes to study loan approval patterns.

The project focuses on data preprocessing, exploratory data analysis, categorical encoding, feature scaling, feature engineering, model training, and performance evaluation.

## Dataset

- **Dataset file:** `loan_approval_data.csv`
- **Number of records:** 1,000
- **Original features:** 20 columns, including the target variable
- **Target variable:** `Loan_Approved`

The dataset contains applicant income, co-applicant income, age, credit score, debt-to-income ratio, savings, collateral value, loan details, and other attributes.

## Tech Stack

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook

## Workflow

1. Load and inspect the dataset.
2. Handle missing numerical and categorical values.
3. Perform exploratory data analysis (EDA).
4. Visualize distributions, class balance, outliers, and feature correlations.
5. Encode categorical features using Label Encoding and One-Hot Encoding.
6. Split the dataset into training and testing sets.
7. Scale features using StandardScaler.
8. Train and evaluate multiple classification models.
9. Apply feature engineering and compare model performance.

## Machine Learning Models

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Gaussian Naive Bayes

## Results

The notebook uses an 80/20 train-test split with `random_state=42`.

### Initial Model Comparison

| Model                | Accuracy | Precision | Recall | F1-score |
| -------------------- | -------: | --------: | -----: | -------: |
| Logistic Regression  |   86.50% |    78.33% | 77.05% |   77.69% |
| KNN                  |   76.00% |    62.75% | 52.46% |   57.14% |
| Gaussian Naive Bayes |   86.50% |    80.36% | 73.77% |   76.92% |

### After Feature Engineering

| Model                | Accuracy | Precision | Recall | F1-score |
| -------------------- | -------: | --------: | -----: | -------: |
| Logistic Regression  |   88.00% |    78.46% | 83.61% |   80.95% |
| KNN                  |   78.50% |    67.31% | 57.38% |   61.95% |
| Gaussian Naive Bayes |   86.00% |    81.13% | 70.49% |   75.44% |

_These are the results recorded in the current notebook, not a guarantee of real-world performance._

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/akshatjaiswal575/CreditWise-Loan-Approval-Prediction.git
cd CreditWise-Loan-Approval-Prediction
```

### 2. Install dependencies

```bash
python -m pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open `credit_wise.ipynb` and run the cells in order. Keep `loan_approval_data.csv` in the same directory as the notebook.

## Current Limitations and Future Improvements

- Move preprocessing into a scikit-learn Pipeline or ColumnTransformer to help prevent data leakage.
- Fit imputers and encoders using training data only.
- Add cross-validation and hyperparameter tuning.
- Compare additional classification models.
- Evaluate the model for fairness, reliability, and suitability before any real lending use.

## Disclaimer

This project is for educational and portfolio purposes. Its predictions should not be used as the sole basis for real-world lending decisions.
