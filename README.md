# Comprehensive Analysis of Bank Customer Churn Prediction Using Machine Learning Models

## Overview
This project focuses on predicting customer churn for a bank using machine learning models. Customer churn, the rate at which customers stop doing business with a company, is a critical metric for businesses as it directly impacts revenue and profitability. By accurately predicting churn, banks can proactively implement retention strategies to retain customers and improve customer satisfaction.

## Objective
The objective of this analysis is to identify the best machine learning model for predicting customer churn and provide actionable insights to reduce churn rates and enhance customer retention strategies.

## Who Will Benefit
Banks and Financial Institutions: Can use the insights to implement targeted retention strategies and reduce customer churn, thereby improving profitability.
Data Scientists and Analysts: Can learn about the methodologies and models used in this analysis for their own projects or research.

## Methodology

### Data Preprocessing:
Missing Value Handling: Checked for and handled missing values to ensure the quality of the data.
Encoding Categorical Data: Encoded categorical variables into numerical format using one-hot encoding for model compatibility.
Feature Engineering: Derived new features from existing data, such as mean values for numeric columns grouped by 'Geography' and 'Gender', to enhance model performance.

### Data Visualization:
Used a counter plot to visualize the distribution of the target variable 'Exited', indicating a churn rate of approximately 20%.

### Correlation Analysis:
Analyzed the correlation between features and the target variable 'Exited' to identify factors influencing customer churn.

### Modeling:

Developed and evaluated the following machine learning models:

Logistic Regression

Random Forest

XGBoost

Final XGBoost (with optimized hyperparameters)

Conducted hyperparameter tuning using Randomized Search to improve model performance.

### Evaluation Metrics:
Evaluated models based on accuracy, precision, recall, and F1 score to determine their effectiveness in predicting customer churn.

### Single Observation Prediction:

Predicted churn for a single observation using the Final XGBoost model.

## Results and Analysis

### Logistic Regression:
Accuracy: 81.10%
Precision: 58.18%
Recall: 23.70%
F1 Score: 33.68%

### Random Forest:
Accuracy: 86.70%
Precision: 74.56%
Recall: 52.10%
F1 Score: 61.34%

### XGBoost:
Accuracy: 85.25%
Precision: 67.08%
Recall: 53.33%
F1 Score: 59.42%

### Final XGBoost:
Accuracy: 85.05%
Precision: 66.99%
Recall: 51.60%
F1 Score: 58.30%

#### Model Comparison and Interpretation:

Logistic Regression: Decent accuracy but struggles with recall, indicating it may miss identifying actual churn cases.

Random Forest: Offers high accuracy, precision, and recall, making it a strong performer in predicting churn.

XGBoost: Strikes a balance between accuracy, precision, and recall, performing competitively with the Random Forest model.

Final XGBoost: Demonstrates competitive performance, slightly trailing behind the Random Forest model in accuracy but offering higher precision than both Logistic Regression and Random Forest models.

## Conclusion
The Random Forest model emerges as the best performer among the models evaluated, offering high accuracy, precision, recall, and F1 score. Its ability to handle complex relationships in the data makes it a suitable choice for predicting customer churn.

## Recommendations
Implement the Random Forest model for predicting customer churn.
Focus on strategies to retain customers identified as likely to churn based on the model predictions.
Future Steps
Explore additional features or data sources to further improve model performance.
Implement the model in a real-world scenario to monitor and reduce customer churn.

## Data Source
Kaggle Dataset: Predicting Churn for Bank Customers
https://www.kaggle.com/datasets/adammaus/predicting-churn-for-bank-customers

## Course Acknowledgement
This analysis is part of the course "Machine Learning Projects for Beginners in Python" on Udemy by Udemy Instructor, Vijay Gadhave.
https://www.udemy.com/course/machine-learning-projects-for-beginners-in-python/learn/lecture/25170744#questions
