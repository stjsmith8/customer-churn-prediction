# Predicting Customer Credit Card Churn

## 📌 Project Overview
This project predicts **credit card customer churn** for an undisclosed bank using supervised machine learning.  
Three models are developed and compared to identify at-risk customers and uncover the strongest drivers of attrition.

📓 **Main notebook:**  
[Predicting Customer Credit Card Churn.ipynb](Predicting%20Customer%20Credit%20Card%20Churn.ipynb)

---

## 🎯 Objectives
- Compare **Logistic Regression**, **Random Forest**, and **XGBoost** for churn prediction
- Identify the model best suited to a **banking retention context**
- Determine which customer attributes are most strongly associated with churn

---

## 📊 Data
- **Source:** Kaggle – Credit Card Customers Dataset https://www.kaggle.com/datasets/sakshigoyal7/credit-card-customers
- **Observations:** 10,127 customers  
- **Target:** Customer churn (binary)  
- **Features:** Demographics, account activity, transaction behavior

---

## 🧹 Preprocessing
- Train/test split (80/20), stratified by churn
- One-hot encoding for categorical variables
- Log transformation for skewed financial features
- Feature scaling via `StandardScaler`
- Class imbalance addressed using **SMOTE** (Logistic Regression & Random Forest) and  
  `scale_pos_weight` (XGBoost)

---

## 🧠 Models & Performance

| Model | Accuracy | Precision (Churn) | Recall (Churn) | F1-Score |
|-----|---------|------------------|---------------|---------|
| Logistic Regression | 80% | 44% | 77% | 56% |
| Random Forest | 94% | 85% | 80% | 82% |
| **XGBoost** | **96%** | **87%** | **94%** | **90%** |

**XGBoost** achieved the best overall performance, offering the strongest balance between recall and precision for churned customers.

---

## 🔍 Key Insights
- Behavioral and spending variables are stronger churn predictors than demographics
- Higher transaction activity and stronger bank relationships reduce churn risk
- Increased inactivity and frequent bank contact are associated with higher churn
- XGBoost effectively captures non-linear relationships and feature interactions

---

## 💼 Business Implications
- Prioritize retention efforts for customers showing declining engagement
- Monitor transaction behavior as early churn warning signals
- Focus interventions on activity-based risk rather than demographics alone

---

## 🛠 Tools
- Python
- pandas, numpy
- scikit-learn
- imbalanced-learn (SMOTE)
- XGBoost
- matplotlib / seaborn

---

