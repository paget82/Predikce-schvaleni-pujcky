# Loan Approval Prediction Using Machine Learning
*Originally published as: Predikce schválení půjčky*

## Problem
A lending company wanted to automate its loan approval process based on the information applicants provide in their online application. Manual review was slow and inconsistent, making it hard to predict approval outcomes quickly and reliably.

## Solution
I built and compared seven different machine learning classification models to predict whether a loan application will be approved, based on the applicant's demographic and financial data. The workflow included exploratory data analysis (EDA), handling missing values, encoding categorical variables, addressing class imbalance, and evaluating multiple algorithms to identify the best-performing approach.

## Tech Stack
- Python
- Pandas
- Scikit-learn
- Matplotlib / Seaborn
- Jupyter Notebook

**Models compared:**
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)
- Naive Bayes
- Decision Tree
- Random Forest
- Gradient Boosting

## Dataset
- Source: loan.csv
- Size: 614 records
- 13 variables: 8 categorical, 4 continuous, and 1 identifier (Loan_ID)

**Fields:**
- Loan_ID – unique loan reference number
- Gender – applicant's gender (Male or Female)
- Married – applicant's marital status (married or single)
- Dependents – number of dependents
- Education – applicant's education level (graduate or not graduate)
- Self_Employed – employment status (self-employed or not)
- ApplicantIncome – applicant's monthly income
- CoapplicantIncome – co-applicant's monthly income
- LoanAmount – requested loan amount
- Loan_Amount_Term – loan repayment term (in days)
- Credit_History – prior credit history record (0: poor, 1: good)
- Property_Area – property location (rural / semi-urban / urban)
- Loan_Status – loan application outcome (Y: approved, N: rejected)

## Process
1. **Exploratory Data Analysis (EDA)** – examined the distribution of categorical variables (Gender, Married, Education, etc.) and numeric variables (income, loan amount, loan term) individually and by loan approval status.
2. **Bivariate analysis** – explored relationships between variables, such as loan amount vs. applicant income, marital status by gender, and credit history vs. self-employment status.
3. **Missing value handling** – identified missing values across the dataset and visualized their pattern.
4. **Data preprocessing** – removed the non-predictive Loan_ID column, imputed categorical variables using the mode and numeric variables using the mean.
5. **One-hot encoding** – converted categorical variables into a numeric format suitable for machine learning algorithms.
6. **Outlier and skewness handling** – identified positively skewed distributions in applicant income, coapplicant income, and loan amount, and applied a square root transformation to normalize them.
7. **Feature/target split** – separated the independent variables (X) from the target variable (y, Loan_Status).
8. **Class balancing (SMOTE)** – applied oversampling to correct the imbalance between approved and rejected loan applications.
9. **Normalization** – scaled the independent variables to a consistent range.
10. **Train/test split** – divided the dataset into 80% training and 20% testing data.
11. **Model training and comparison** – trained all seven models on the same data and compared their performance.

## Results
All models achieved reasonable accuracy, ranging from 74% to nearly 83%:

| Model | Accuracy |
|---|---|
| Logistic Regression | 82.84% |
| Random Forest | 82.25% |
| Decision Tree | 81.07% |
| SVM | 80.47% |
| Naive Bayes (Categorical) | 79.29% |
| Gradient Boost | 78.70% |
| K Neighbors | 77.51% |
| Naive Bayes (Gaussian) | 73.96% |

- The best-performing model was **Logistic Regression, at 82.84% accuracy**, closely followed by Random Forest at 82.25%.
- Credit history, applicant income, and loan amount emerged as some of the most influential factors in predicting loan approval.

## Screenshots / Demo
See the full exploratory data analysis and model comparison charts in the notebook.

## How to run
```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
jupyter notebook
```
Then open `predikce schvaleni pujcky.ipynb` to follow the full analysis.

## Files
- [Jupyter Notebook](loan_approval_prediction.ipynb) – full loan approval prediction analysis and workflow
- [CSV](loan.csv) – dataset

## Business value
An automated, data-driven loan approval model allows the company to speed up decision-making, reduce inconsistency in manual reviews, and flag high-risk applications earlier. This supports faster turnaround for applicants while helping the business manage credit risk more effectively.
