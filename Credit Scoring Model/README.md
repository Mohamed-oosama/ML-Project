
# 🏦 Credit Scoring Model

## 📌 Overview
This project builds a **Credit Scoring Model** to predict an individual's creditworthiness using past financial and demographic data.  
The model helps financial institutions decide whether to approve or reject loan/credit applications.  
It also demonstrates practical applications of Machine Learning for real-world financial decision-making.

---

## 🎯 Objectives
- Predict loan/credit approval based on applicant's financial and demographic history.  
- Train and evaluate multiple classification models:
  - Logistic Regression  
  - Decision Tree  
  - Random Forest  
  - K-Nearest Neighbors (KNN)  
  - XGBoost  
  - Support Vector Classifier (SVC)  
- Evaluate model performance using:
  - **Accuracy**
  - **Precision, Recall, F1-Score**
  - **ROC-AUC**
- Compare model performances and identify the most reliable predictor.

---

## 📊 Dataset
The dataset includes applicant information such as:
- Income  
- Existing debts  
- Payment history  
- Marital status, gender, and other demographic details  
- Credit history features such as late payments or defaults  

*(Dataset is included in this repository / provided separately.)*  
> Note: The dataset is preprocessed for missing values and categorical features encoding.

---

## ⚙️ Requirements
Install the following Python libraries before running the project:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
