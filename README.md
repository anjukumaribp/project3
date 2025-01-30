# project3
Upgrad project file

Telecom Customer Churn Prediction
This project aims to predict customer churn in a telecom company using machine learning techniques. The focus is on high-value customers to help the company reduce revenue loss by identifying potential churners early.

Project Overview
In the telecom industry, customer churn (i.e., customers leaving the service provider) is a major problem. Retaining existing customers is 5-10 times cheaper than acquiring new ones. The goal of this project is to:

Predict which high-value customers are at risk of churn.
Identify the key factors contributing to customer churn.
Provide business recommendations to reduce churn.
Dataset Details
The dataset contains customer usage and recharge details for four months:

June (6) & July (7) → Good phase (Customer is satisfied)
August (8) → Action phase (Customer might be considering switching)
September (9) → Churn phase (Used to define churn but removed from training)
Churn Definition: A customer is considered to have churned if they:

Made zero outgoing calls (total_og_mou_9 == 0).
Made zero incoming calls (total_ic_mou_9 == 0).
Used zero mobile data (vol_2g_mb_9 == 0 & vol_3g_mb_9 == 0).
Project Workflow
Step 1: Data Preprocessing
Handle missing values (replace NaNs with 0 for numeric features).
Remove irrelevant columns (e.g., mobile_number).
Select high-value customers (top 30% based on recharge amount in June & July).
Step 2: Feature Engineering
Create trend-based features (e.g., change in ARPU from June to August).
Replace infinite values and clip extreme outliers.
Normalize numeric features before feeding into models.
Step 3: Exploratory Data Analysis (EDA)
Visualize churn vs. non-churn customers.
Check feature correlation with churn.
Identify important variables affecting churn.
🔹 Step 4: Model Building
Logistic Regression (for interpretability and feature importance).
Random Forest Classifier (for better predictive performance).
SMOTE (Synthetic Minority Over-sampling Technique) to handle class imbalance.
🔹 Step 5: Model Evaluation
Classification Report (Precision, Recall, F1-score).
Confusion Matrix (to check misclassification rates).
Feature Importance Analysis (identify key churn predictors).
📈 Key Insights
High decline in ARPU (Average Revenue Per User) → High churn risk.
Customers with reduced recharge amounts are more likely to churn.
Customers who stop using mobile data are potential churners.
Call volume decrease over months is a key indicator of churn.
📌 Business Recommendations
✅ Identify early churn indicators and offer special retention plans.
✅ Target customers showing a sharp decline in recharge amount.
✅ Engage customers reducing outgoing/incoming call volume with incentives.
✅ Improve mobile data offerings for users reducing 2G/3G usage.
✅ Use AI-driven customer segmentation to personalize retention strategies.

⚙️ How to Run the Code
Prerequisites
Install the required dependencies:

bash
Copy
Edit
pip install pandas numpy scikit-learn imbalanced-learn matplotlib seaborn
Run the Python script
bash
Copy
Edit
python telecom_churn_prediction.py
📌 File Structure
bash
Copy
Edit
📁 Telecom_Churn_Prediction/
│── 📄 telecom_churn_prediction.py  # Main script for model training & evaluation
│── 📄 README.md                     # Project documentation
│── 📊 telecom_churn_data.csv        # Dataset file
│── 📄 Data Dictionary.xlsx          # Column descriptions
│── 📁 models/                        # Saved trained models
│── 📊 results/                       # Analysis reports & visualizations
📌 Future Enhancements
🔹 Use Deep Learning models (e.g., Neural Networks) for better prediction accuracy.
🔹 Incorporate more behavioral data (e.g., customer complaints, customer service interactions).
🔹 Develop a real-time churn prediction API for telecom companies.

👨‍💻 Contributors
Your Name - Data Scientist 📊
Company/Institution (if applicable)
🚀 Feel free to contribute! Fork this project and add your own improvements.

📜 License
This project is open-source and free to use under the MIT License.
