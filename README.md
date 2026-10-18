 
Customer Churn Prediction using Logistic Regression
📋 Overview

Customer churn is a critical metric for subscription-based businesses and telecommunications companies. This project uses Logistic Regression to predict whether a customer is likely to churn (leave the service) based on demographic information, account features, and service subscriptions.

Using the Telco Churn dataset, this repository provides a full workflow covering data preprocessing, feature engineering, model training, and performance evaluation.
🗂️ Dataset Description

The model is trained on the Telco Customer Churn dataset (Telco_Churn_Dataset.csv).

    Target Variable:

        Churn: Binary outcome indicating whether the customer left within the last month (Yes / No).

    Key Features:

        Demographics: gender, SeniorCitizen, Partner, Dependents

        Services: PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies

        Account: tenure, Contract, PaperlessBilling, PaymentMethod, MonthlyCharges, TotalCharges

⚙️ Project Workflow

    Data Loading & Cleaning:

        Load data using pandas.

        Handle missing values and adjust data types (e.g., TotalCharges).

    Preprocessing & Feature Engineering:

        Encoding: One-Hot Encoding / Label Encoding for categorical variables.

        Scaling: Standardization of continuous variables (tenure, MonthlyCharges, TotalCharges).

    Model Training:

        Train-test split (80% train / 20% test).

        Fit Logistic Regression model using scikit-learn.

    Evaluation:

        Evaluate model performance using Accuracy, Precision, Recall, F1-Score, and ROC-AUC.

🚀 Getting Started
Prerequisites

Install the required libraries:

pip install pandas numpy scikit-learn matplotlib seaborn

Quickstart

import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression

# 1. Load data
df = pd.read_csv('Telco_Churn_Dataset.csv')

# 2. Preview data
print(df.head())

📊 Key Insights

    Contract Type: Month-to-month contract holders have a significantly higher churn rate compared to long-term contracts.

    Tenure: Higher tenure strongly correlates with lower customer churn.

    Model Interpretability: Logistic Regression coefficients help identify top drivers behind customer churn.

Report unsafe content Opens in a new window
