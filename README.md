# 📡 Telecom Customer Churn Prediction

An end-to-end Machine Learning classification project focused on predicting customer churn in the telecom industry using Python, data analysis, visualization, feature engineering, and predictive modeling.

---

# 📌 Project Overview

Customer churn is one of the biggest challenges faced by telecom companies. Losing existing customers directly affects revenue and customer acquisition costs.

This project builds multiple machine learning models to predict whether a customer is likely to leave the telecom service.

The notebook covers:

* Data cleaning
* Exploratory Data Analysis (EDA)
* Feature engineering
* Data preprocessing
* Model building
* Model evaluation
* Feature importance analysis
* Business insights & recommendations

---

# 🎯 Problem Statement

The goal of this project is to:

* Analyze customer behavior patterns
* Identify factors contributing to churn
* Build predictive models for churn detection
* Improve customer retention strategies

---

# 📂 Dataset Information

The dataset contains telecom customer information including:

* Customer demographics
* Account information
* Service subscriptions
* Billing details
* Contract type
* Tenure information
* Customer support interactions
* Churn status

### Target Variable

* `Churn Value`

  * `1` → Customer churned
  * `0` → Customer retained

---

# 🛠️ Technologies Used

## Programming Language

* Python

## Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

# 📊 Project Workflow

## 1. Data Loading

* Loaded telecom customer churn dataset
* Inspected rows, columns, and dataset structure

## 2. Data Exploration

Performed:

* Shape analysis
* Data type inspection
* Missing value detection
* Statistical summaries
* Unique value analysis

## 3. Data Cleaning

Tasks completed:

* Removed unnecessary columns
* Fixed incorrect data types
* Converted `Total Charges` to numeric format
* Handled missing values
* Removed blank string values

## 4. Exploratory Data Analysis (EDA)

Visualizations created:

* Churn distribution
* Churn vs Contract Type
* Monthly Charges vs Churn
* Tenure vs Churn
* Correlation heatmap

### Key Insights

* Customers with month-to-month contracts churn more frequently
* Higher monthly charges are associated with increased churn
* Customers with shorter tenure are more likely to churn

---

# ⚙️ Feature Engineering

* Encoded categorical variables
* Applied feature scaling using `StandardScaler`
* Split dataset into training and testing sets

---

# 🤖 Machine Learning Models

The following models were trained and evaluated:

## 1. Logistic Regression

* Baseline classification model
* Good balance between interpretability and performance

## 2. Decision Tree Classifier

* Achieved high training accuracy
* Showed signs of overfitting

## 3. Random Forest Classifier

* Improved generalization
* Strong feature importance analysis

## 4. Balanced Logistic Regression (Final Model)

* Applied class balancing using `class_weight='balanced'`
* Improved recall for churn prediction

---

# 📈 Model Evaluation Metrics

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC Score
* Confusion Matrix

### Best Performing Models

| Model                        | Approx Accuracy | ROC-AUC                   |
| ---------------------------- | --------------- | ------------------------- |
| Logistic Regression          | ~80.7%          | ~0.862                    |
| Balanced Logistic Regression | ~80%+           | ~0.862                    |
| Random Forest                | Competitive     | Strong Feature Importance |

---

# 🔍 Feature Importance Analysis

Top features influencing churn included:

* Contract Type
* Monthly Charges
* Tenure Months
* Internet Service
* Payment Method
* Total Charges

Feature importance was analyzed using:

* Logistic Regression coefficients
* Random Forest feature importance

---

# 📌 Business Insights

## Customers more likely to churn:

* Month-to-month contract users
* Customers with high monthly charges
* New customers with low tenure
* Customers without long-term commitments

## Recommended Business Actions

* Encourage long-term contracts
* Offer retention discounts for high-risk customers
* Improve onboarding experience
* Provide personalized customer support
* Create loyalty programs for newer customers

---

# ⚠️ Limitations

* Dataset may not represent all telecom markets
* Model performance depends on dataset quality
* External economic or competitor factors were not included
* Further hyperparameter tuning could improve performance

---

# 🚀 Future Improvements

Possible enhancements:

* Hyperparameter optimization
* Cross-validation
* Advanced ensemble models
* XGBoost / LightGBM implementation
* Deployment using Flask or Streamlit
* Real-time churn prediction dashboard

---

# 📷 Visualizations Included

* Count plots
* Box plots
* Correlation heatmaps
* ROC curves
* Feature importance charts
* Confusion matrices

---

# ▶️ How to Run the Project

## 1. Clone Repository

```bash
git clone https://github.com/your-username/telecom-customer-churn-prediction.git
cd telecom-customer-churn-prediction
```

## 2. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl
```

## 3. Run Jupyter Notebook

```bash
jupyter notebook
```

Open:

```bash
telecom_customer_churn_prediction.ipynb
```

---
```text
# 📁 Project Structure

📦 customer-churn-prediction
 ┣ 📂 data
 ┃ ┣ 📄 Telco_customer_churn.xlsx
 ┃ ┗ 📄 readme.txt
 ┣ 📂 graphs
 ┃ ┣ 📊 eda_01_churn_distribution.png
 ┃ ┣ 📊 eda_02_churn_vs_contract.png
 ┃ ┣ 📊 eda_03_monthly_charges_vs_churn.png
 ┃ ┣ 📊 eda_04_tenure_vs_churn.png
 ┃ ┣ 📊 eda_05_correlation_heatmap.png
 ┃ ┣ 📊 eval_01_confusion_matrix_before_after.png
 ┃ ┣ 📊 eval_02_feature_importance_lr_rf.png
 ┃ ┣ 📊 eval_03_roc_curve_all_models.png
 ┃ ┣ 📊 eval_04_model_performance_comparison.png
 ┃ ┗ 📄 readme.txt
 ┣ 📄 README.md
 ┣ 📄 requirements.txt
 ┣ 📄 .gitignore
 ┗ 📓 telecom_customer_churn_prediction.ipynb
```
---

# 🧠 Skills Demonstrated

* Data Cleaning
* Exploratory Data Analysis
* Data Visualization
* Feature Engineering
* Machine Learning
* Classification Algorithms
* Model Evaluation
* Business Insight Generation

---

# 📚 Conclusion

This project demonstrates a complete machine learning workflow for telecom customer churn prediction.

Among all tested models, Logistic Regression and Balanced Logistic Regression delivered the best overall performance with strong ROC-AUC scores and reliable churn detection capability.

The project highlights how machine learning can help telecom companies proactively identify at-risk customers and improve retention strategies.

---

# 👨‍💻 Author

Your Name

* GitHub: [https://github.com/Sanjay-raj-k-s](https://github.com/Sanjay-raj-k-s)
* LinkedIn: [https://www.linkedin.com/in/sanjayrajks/](https://www.linkedin.com/in/sanjayrajks/)

---

# ⭐ If You Like This Project

Give this repository a ⭐ on GitHub and feel free to fork or contribute.
