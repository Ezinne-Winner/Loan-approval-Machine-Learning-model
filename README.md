# Loan Approval Prediction

## Overview
This project focuses on building a machine learning system that predicts whether a loan application will be **approved** or **rejected** based on applicant information such as income, education, credit history, employment status, and property details.

The goal is to analyze the dataset, understand the factors influencing loan approval, and develop a reliable predictive model that can support financial institutions in decision-making.

---

## Aim
To develop and evaluate machine learning models capable of accurately predicting loan approval status.

---

## Objectives
- Clean and preprocess the raw dataset  
- Perform detailed Exploratory Data Analysis (EDA)  
- Handle missing values and outliers  
- Encode categorical variables and scale numerical features  
- Train multiple machine learning models  
- Compare model performance  
- Conduct hyperparameter tuning  
- Draw insights and conclusions from the analysis  

---

## Dataset
The dataset includes:
- Demographic information  
- Income details  
- Loan amount and term  
- Credit history  
- Property area  
- Employment and education status  

Missing values were filled using:
- Mode (categorical)
- Median/Mode (numerical)

Categorical data was encoded using **Label Encoding**, and numerical data was scaled using **StandardScaler**.

---

## Exploratory Data Analysis (EDA)
EDA was performed to understand patterns, relationships, and trends in the data, including:

- Distribution of loan status  
- Applicant and co-applicant income distributions  
- Loan amount distribution  
- Relationship between:
  - Credit history and loan approval  
  - Education and applicant income  
  - Property area and approval rates  

### Key Insights
- Applicants with **good credit history** have a much higher approval rate.  
- Applicant income influences loan amount but is not the sole determinant of approval.  
- Graduates generally apply for more loans and show slightly higher approval rates.  
- Income-related columns contained significant outliers that required cleaning.

---

## Outlier Treatment
Outliers were detected using the **Interquartile Range (IQR)** method and removed from:
- Applicant Income  
- Coapplicant Income  

This helped improve model stability and performance.

---

## Data Preparation
- Encoded categorical variables using `LabelEncoder`
- Scaled numerical data using `StandardScaler`
- Split dataset into training and test sets (70/30 ratio)

---

## Models Used
The following machine learning algorithms were trained and evaluated:

- **Logistic Regression**  
- **Random Forest Classifier**  
- **Support Vector Classifier (SVC)**  
- **XGBoost Classifier**

### Model Accuracy Comparison

| Model | Accuracy |
|--------|----------|
| Logistic Regression | ~84% |
| Random Forest | ~85% |
| SVC | ~74% |
| **XGBoost** | **~87%** |

---

## Results & Findings
- **XGBoost achieved the highest accuracy** and performed best overall.  
- Logistic Regression and Random Forest also performed well and were more interpretable.  
- SVC struggled due to dataset imbalance.  
- Credit history emerged as the most influential predictor of loan approval.

---

## Conclusion
Machine learning models can effectively predict loan approval outcomes with high accuracy.  
The project demonstrates how credit history, income patterns, and proper data cleaning strongly influence predictive performance.

XGBoost is recommended for deployment due to its robustness and consistency.

---

## Technologies Used
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn, Plotly  
- Scikit-Learn  
- XGBoost  
- Jupyter Notebook  

---

## Future Enhancements
- Apply SMOTE or other balancing techniques  
- Add SHAP explainability for model insights  
- Deploy the model using Flask or FastAPI  
- Build an interactive dashboard using Streamlit  
- Explore more advanced feature engineering techniques  

---

