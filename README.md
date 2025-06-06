

# Comprehensive Analysis of Bank Customer Churn Prediction Using Machine Learning Models

## Project Description

This project aims to predict whether a bank customer will churn (leave the bank) using multiple machine learning classification models. Customer churn directly impacts a bank’s revenue and customer retention strategy. Accurately identifying customers at risk allows institutions to take proactive measures and improve satisfaction.

## Who Will Benefit and Why?

* **Banks and Financial Institutions**: Can use churn prediction to design personalized retention strategies, reduce attrition, and improve long-term profitability.
* **Data Scientists and Analysts**: Provides a practical example of preprocessing, feature engineering, and model evaluation for real-world classification tasks in finance.
* **Business Strategists**: Gain insights into what factors contribute most to customer churn and which segments need more attention.

---

## Objective

To evaluate and compare different machine learning models to identify which performs best at predicting customer churn and to extract actionable insights from the results.

---

## Dataset

* **Source**: [Kaggle - Predicting Churn for Bank Customers](https://www.kaggle.com/datasets/adammaus/predicting-churn-for-bank-customers)
* The dataset contains customer-level information such as age, balance, tenure, credit score, geography, and gender, along with the target variable `Exited`, which indicates churn (1 = yes, 0 = no).

---

## Approach

### Data Preprocessing

* **Missing Values**: Checked and handled any missing data to ensure completeness.
* **Categorical Encoding**: Used one-hot encoding to convert categorical variables (`Geography`, `Gender`) into numerical format.
* **Feature Engineering**: Created aggregated features such as mean values grouped by `Geography` and `Gender` to enhance model inputs.

### Data Visualization

* A counter plot was used to display the distribution of the `Exited` variable.

  * **Churn Rate**: \~20% of customers exited, revealing moderate class imbalance.

### Correlation Analysis

* Evaluated feature correlation with `Exited` to identify the most influential factors driving customer churn.

---

## Machine Learning Models

The following models were developed, evaluated, and compared:

1. **Logistic Regression**
2. **Random Forest Classifier**
3. **XGBoost Classifier**
4. **Final XGBoost Model** (with hyperparameter tuning using Randomized Search)

---

## Evaluation Metrics

Each model was assessed using four core metrics:

* **Accuracy**
* **Precision**
* **Recall**
* **F1 Score**

These metrics help capture the trade-off between correctly identifying churn cases and minimizing false positives/negatives.

---

## Model Performance

### Logistic Regression

* **Accuracy**: 81.10%
* **Precision**: 58.18%
* **Recall**: 23.70%
* **F1 Score**: 33.68%

➡️ Performs reasonably well but has low recall, meaning it misses many actual churn cases.

### Random Forest

* **Accuracy**: 86.70%
* **Precision**: 74.56%
* **Recall**: 52.10%
* **F1 Score**: 61.34%

➡️ Strong overall performance, especially in capturing churned customers with high precision and recall.

### XGBoost

* **Accuracy**: 85.25%
* **Precision**: 67.08%
* **Recall**: 53.33%
* **F1 Score**: 59.42%

➡️ Balanced model, close in performance to Random Forest.

### Final XGBoost (Tuned)

* **Accuracy**: 85.05%
* **Precision**: 66.99%
* **Recall**: 51.60%
* **F1 Score**: 58.30%

➡️ Slightly lower performance than Random Forest but offers higher precision than both Logistic Regression and Random Forest.

---

## Single Observation Prediction

* A single customer profile was processed and passed into the Final XGBoost model.
* **Result**: Predicted as a churn case (`Exited = 1`), demonstrating how the model can be used for individual-level predictions.

---

## Key Findings

* **Random Forest** emerged as the top-performing model based on a combination of accuracy, recall, and F1 score.
* **XGBoost** showed comparable performance, offering a good balance between false positives and false negatives.
* **Logistic Regression**, although simpler, lacked the capability to capture true churn cases effectively due to low recall.
* **Feature importance analysis** (not shown in detail) would further help in understanding key drivers of churn such as credit score, balance, or tenure.

---

## Conclusion

The **Random Forest model** is the most effective for predicting customer churn among those tested. It provides a solid balance across all key evaluation metrics and can serve as a reliable model for deployment in real banking systems.

---

## Recommendations

* **Deploy Random Forest** as the primary churn prediction model.
* **Use churn predictions** to create targeted outreach strategies for at-risk customers.
* **Monitor model performance** regularly and update with new data for continuous improvement.

### Future Steps

* Integrate external datasets (e.g., customer service history, complaints) for richer features.
* Explore advanced ensemble methods or deep learning models.
* Run A/B testing with retention campaigns guided by model predictions.

---

## Data Source

[Kaggle Dataset: Predicting Churn for Bank Customers](https://www.kaggle.com/datasets/adammaus/predicting-churn-for-bank-customers)

---

## Course Acknowledgment

This project was developed as part of the Udemy course:
**"Machine Learning Projects for Beginners in Python" by Vijay Gadhave**
[Course Link](https://www.udemy.com/course/machine-learning-projects-for-beginners-in-python/learn/lecture/25170744#questions)

---
