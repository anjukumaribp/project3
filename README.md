Telecom Churn Prediction

Project Overview

In the telecom industry, customer churn is a significant challenge as customers frequently switch between service providers. This project aims to predict customer churn using customer-level data from a leading telecom firm and identify key factors that influence churn. By proactively identifying high-risk customers, telecom companies can take preventive measures to retain them, reducing revenue loss.

Business Problem

The annual churn rate in telecom ranges from 15-25%.
Acquiring a new customer is 5-10 times more expensive than retaining an existing one.
The project focuses on high-value prepaid customers in the Indian and Southeast Asian market, where prepaid models dominate.

Objective

Predict churn for high-value customers using the last three months of data.
Identify key factors leading to churn.
Recommend strategies for customer retention.

Dataset Information

The dataset contains customer data for four consecutive months (June-September). The months are encoded as 6, 7, 8, and 9.
Data Dictionary
loc: Local
IC: Incoming
OG: Outgoing
T2T: Telecom-to-Telecom
T2O: Telecom-to-Other operator
RECH: Recharge
Columns suffixed with 6, 7, 8, 9 correspond to the respective months.


Methodology

Step 1: Data Preprocessing
Load and explore the dataset.
Handle missing values and outliers.

Step 2: High-Value Customer Filtering
Define high-value customers as those with recharge amounts above the 70th percentile in the first two months.
This should result in around 30,000 rows.

Step 3: Churn Tagging
A customer is tagged as churned (1) if:
No incoming or outgoing calls.
No mobile internet usage.
Based on the 9th month’s data.
Columns used:
total_ic_mou_9
total_og_mou_9
vol_2g_mb_9
vol_3g_mb_9
After tagging, drop all month 9 attributes.

Step 4: Feature Engineering
Create new features based on call duration, recharge patterns, and data usage.
Convert categorical variables to numerical.
Normalize or standardize features if needed.

Step 5: Handle Class Imbalance
Churn rate is typically 5-10%.
Use techniques like SMOTE (oversampling) or undersampling.

Step 6: Model Building
Split the data into train and test sets.
Train various models:
Logistic Regression (for feature importance)
Random Forest
XGBoost
SVM
Optimize hyperparameters using GridSearchCV.

Step 7: Model Evaluation
Use performance metrics like:
Accuracy
Precision & Recall
F1-score
ROC-AUC score

Step 8: Feature Importance Analysis
Identify key churn predictors using:
Logistic Regression coefficients
Random Forest/XGBoost feature importance
Visualize results with bar plots.

Step 9: Business Recommendations
Based on insights, recommend strategies such as:
Special discounts & offers for high-risk customers.
Improving network quality to retain users.
Personalized retention campaigns based on customer usage patterns.

Technologies Used
Python (pandas, numpy, seaborn, scikit-learn, imbalanced-learn)
Machine Learning Models (Logistic Regression, Random Forest, XGBoost, SVM)
Data Visualization (Matplotlib, Seaborn, SHAP)

How to Run the Project
Install required packages:
pip install pandas numpy seaborn scikit-learn imbalanced-learn xgboost matplotlib
Run the Jupyter Notebook:
jupyter notebook
Follow the notebook's steps to preprocess data, train models, and analyze results.

Conclusion

This project helps telecom companies proactively identify high-risk customers and take corrective actions to reduce churn and revenue loss. By leveraging machine learning, we provide valuable insights into customer behavior, helping businesses make data-driven decisions.
