## Customer Churn Prediction Using Machine Learning

## Table Contents

1.Business Overview  
2.Business Understanding  
3.Stakeholders  
4.Success criteria  
5.Data Understanding  
6.EDA  
7.Modeling 🚀  
8.Model Performance  
9.model choice  
10.Recommendations
11.Conclusion

## 1️⃣ Business Overview

The telecommunications industry is highly competitive, and companies often struggle to retain customers. One major challenge faced by telecom providers is customer churn, which occurs when customers stop using the company’s services and move to a competitor.

Customer churn can significantly impact a company's revenue because acquiring new customers is often more expensive than retaining existing ones. Therefore, companies need effective strategies to identify customers who are likely to leave and take proactive steps to retain them.

In this project, I analyze customer data from a telecommunications company (Syriatel) to build a machine learning model that predicts whether a customer is likely to churn. The dataset contains information such as customer account length, call usage, international plans, voice mail plans, and customer service calls.

By identifying patterns that lead to customer churn, the company can take preventive actions such as offering promotions, improving customer service, or providing personalized retention strategies.

## 2️⃣ Business Understanding

The objective of this project is to predict whether a telecom customer will churn using customer usage and account information. The dataset includes features such as account length, call usage (day, evening, and night minutes), international plan, voicemail plan, and customer service calls.

The target variable is churn, where TRUE indicates the customer left the company and FALSE indicates the customer stayed. By predicting churn early, the company can take actions such as improving customer service or offering incentives to retain customers.

## 3️⃣ Stakeholders

The main stakeholders for this project include:  
Company management, who use insights to improve business strategies and reduce churn.  
Customer retention teams, who can target customers likely to leave with special offers or improved services.  
Customer service teams, who can improve support if frequent service calls are linked to churn.

## 4️⃣ Success Criteria

The success of this project will be determined by how well the machine learning model can correctly predict customer churn. I will evaluate the model using classification metrics such as accuracy, precision, recall, and F1-score.

A successful model should correctly identify customers who are likely to churn while minimizing incorrect predictions. This will help demonstrate that the model can be useful for identifying at-risk customers and supporting customer retention strategies

## 5️⃣ Data Understanding

The dataset used in this project contains customer information from a telecommunications company. It includes data related to customer accounts, service usage, and interactions with customer support. The goal of the dataset is to help identify patterns that may lead to customer churn.

During the initial inspection of the dataset, I checked for issues such as missing values, duplicates, and data types. Understanding the structure and quality of the data helps prepare it for further analysis, including exploratory data analysis and machine learning modeling.

## 6️⃣ Exploratory Data Analysis (EDA)

Exploratory Data Analysis (EDA) was conducted to understand patterns, relationships, and trends within the dataset.

Several visualizations were used to analyze how different features relate to customer churn.

Key Findings:
Customers with frequent customer service calls are more likely to churn, suggesting dissatisfaction.
Customers with an international plan show a higher churn rate.
Customers with higher usage (especially day minutes) tend to churn more.

These insights highlight important behavioral patterns that influence customer churn and help guide the modeling process.

## 7️⃣ Modeling 🚀

To solve the classification problem, multiple machine learning models were built and evaluated.

Models Used:
Logistic Regression (Baseline Model)
Logistic Regression with SMOTE
Decision Tree (Without SMOTE)
Decision Tree (With SMOTE)
Data Preparation for Modeling:
Train-test split was applied
Categorical variables were encoded
Numerical features were scaled
Class imbalance was handled using SMOTE (for selected models)

## 8️⃣ Model Performance

The models were evaluated using classification metrics:

Accuracy → Overall correctness
Precision → Correctness of positive predictions
Recall → Ability to detect churn
F1-score → Balance between precision and recall
ROC-AUC → Overall model performance
Summary of Results:
Logistic Regression (Original):
High accuracy
Very low recall for churn (poor detection)
Logistic Regression (SMOTE):
Improved recall
Slight decrease in accuracy
Decision Tree (Without SMOTE):
High accuracy (~94%)
Strong AUC (~0.91)
Balanced performance
Decision Tree (With SMOTE):
Higher recall
Lower accuracy (~80%)
More false positives

## 9️⃣ Model Choice

The selected model for this project is:

👉 Decision Tree (Without SMOTE)

Reason for Selection:
Provides the best balance between accuracy and recall
Achieves high overall performance
Maintains strong ROC-AUC score
Produces fewer false positives compared to SMOTE models

This model is suitable for business use because it can effectively identify customers at risk of churn while maintaining reliable predictions.

## 🔟 Recommendations

Based on the model results, the following recommendations are proposed:

Focus on At-Risk Customers
→ Target customers predicted as churn for retention efforts
Improve Customer Retention Strategies
→ Offer personalized promotions and better customer support
Monitor Model Performance
→ Regularly update the model with new data
Balance Business Trade-offs
→ Adjust model depending on whether recall or accuracy is more important
Analyze Key Features
→ Focus on factors like service calls and usage patterns
Explore Advanced Models
→ Consider Random Forest or Gradient Boosting for improvement

## 1️⃣1️⃣ Conclusion

This project demonstrates that machine learning can effectively predict customer churn using customer behavior data.

The analysis shows that:

Customer service interactions and usage patterns strongly influence churn
Handling class imbalance impacts model performance
Decision Tree provides the best balance of performance

👉 Using this model, the company can move from reactive decisions to proactive customer retention strategies, improving both revenue and customer satisfaction.
