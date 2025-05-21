# Customer-Churn-Prediction
This project uses machine learning to predict customer churn based on demographic, service usage, and billing data. By building and tuning a Random Forest classifier, the model achieves around 80% accuracy and provides insights into the key factors that influence customer retention, helping businesses take proactive steps to reduce churn.

# 🔄 Customer Churn Prediction

This project aims to build a classification model that predicts whether a customer will churn based on demographic, service usage, and account-related data. Predicting churn allows businesses to take proactive measures in customer retention, minimizing revenue loss and enhancing customer satisfaction.

---

## 🎯 Problem Statement

Customer churn refers to when a customer ends their relationship with a service provider. In today’s competitive environment, retaining customers is crucial. The goal of this project is to develop a machine learning model that accurately predicts whether a customer is likely to churn.

The dataset contains demographic information (like gender and senior citizen status), account details (tenure, payment method), and service usage data (internet, phone, security services). The model will help identify high-risk customers and guide the company’s retention strategies.

---

## 📦 Dataset Information

- **Dataset Name**: `customer_data.csv`
- **Total Entries**: 7,043
- **Features**: 21
- **Source**: [Customer Dataset (Google Sheets)](https://docs.google.com/spreadsheets/d/1rnBO9F9xdSUY-WpeOJilMxMRZT-hwwWq6O98OHreY0k/edit?gid=1602415961#gid=1602415961)

Features include:

- **Demographics**: Gender, SeniorCitizen, Partner, Dependents
- **Service Details**: InternetService, PhoneService, OnlineSecurity, etc.
- **Account Info**: Tenure, Contract, PaymentMethod, MonthlyCharges, TotalCharges
- **Target**: `Churn` (Yes/No)

---

## 📈 Project Deliverables

1. **Data Exploration & Preprocessing**:
   - Handled missing values (e.g., `TotalCharges`)
   - Encoded categorical and binary variables
   - Scaled numeric features using `StandardScaler`
   - Created dummy variables for multiclass features

2. **Model Development**:
   - Built an initial **RandomForestClassifier** model
   - Performed **Train/Test Split**: 
     - 80% Training 
     - 20% Testing
     - Used **stratified sampling** to preserve class balance

3. **Model Evaluation**:
   - **Initial Model Accuracy**: 79.2%
   - **Tuned Model Accuracy**: 80.2% (after GridSearchCV)
   - Evaluation Metrics:
     - **Precision (Churn Class)**: 66%
     - **Recall (Churn Class)**: 52%
     - **F1-Score (Churn Class)**: 58%
   - Confusion matrix and classification report included

4. **Feature Importance**:
   - Top predictive features:
     1. `TotalCharges`
     2. `MonthlyCharges`
     3. `tenure`
     4. `PaymentMethod_Electronic check`
     5. `InternetService_Fiber optic`

---

## ✅ Success Criteria

- Developed a reliable and interpretable churn prediction model
- Achieved strong accuracy and F1-score on test data
- Generated insights for customer retention strategies
- Made predictions for new/unseen data with reasonable accuracy

---

## 📊 Key Insights

- **TotalCharges**: Higher total charges are associated with customer retention (long-term users).
- **MonthlyCharges**: Higher monthly bills increase the likelihood of churn.
- **tenure**: Longer tenure reduces churn risk — loyal customers are more stable.
- **PaymentMethod**: Customers using electronic check are more likely to churn.
- **InternetService**: Fiber optic users show different churn behavior than DSL users.

---

## ⚙️ Tools & Libraries Used

- **Language**: Python
- **Libraries**:
  - `pandas`, `numpy` – data manipulation
  - `scikit-learn` – model building and evaluation
  - `seaborn`, `matplotlib` – visualizations

---

## 📎 Guidelines Followed

- Data was split into training/testing sets to avoid overfitting
- Hyperparameter tuning using `GridSearchCV`
- Used visualizations for interpretability (feature importance, confusion matrix)
- Reported all preprocessing, modeling, and evaluation steps

---


