# 📡 Customer Churn Prediction — Telecom Industry

> **End-to-End Machine Learning Classification Project**  
> Predicting customer churn using the IBM Telco dataset with Logistic Regression, Decision Tree, and Random Forest.

---

## 📋 Project Summary

| Item | Details |
|---|---|
| **Dataset** | IBM Telco Customer Churn — 7,043 customers, 20 features (after cleaning) |
| **Problem Type** | Binary Classification |
| **Models Used** | Logistic Regression, Decision Tree, Random Forest |
| **Best Model** | Logistic Regression with `class_weight='balanced'` |
| **Churn Recall** | 0.57 → **0.80** (40% improvement) |
| **ROC-AUC** | **0.862** |
| **Key Drivers** | Tenure Months, Total Charges, Monthly Charges, Contract Type |

---

## 🎯 Business Goal

Customer churn is one of the most critical challenges in the telecom industry. Acquiring a new customer costs **5–7x more** than retaining an existing one. This project builds a machine learning model to identify at-risk customers early, enabling targeted retention strategies before revenue is lost.

---

## 📁 Project Structure

```
customer-churn-prediction/
│
├── README.md                          # Project documentation
├── requirements.txt                   # Python dependencies
├── customer_churn_prediction.ipynb    # Main Jupyter Notebook
│
├── data/
│   └── telecom_customer_churn.csv     # IBM Telco dataset (place here)
│
└── graphs/
    ├── roc_curve.png                  # ROC Curve — all models comparison
    ├── confusion_matrix.png           # Confusion Matrix — before vs after balancing
    └── feature_importance.png         # Feature Importance — LR & Random Forest
```

---

## 📊 Dataset

- **Source:** [IBM Cognos Analytics Sample Data](https://community.ibm.com/community/user/businessanalytics/blogs/steven-macko/2019/07/11/telco-customer-churn-1113)
- **Observations:** 7,043 customers
- **Original Features:** 33 variables
- **Target Variable:** `Churn Value` — 1 (churned), 0 (retained)

### Feature Categories

| Category | Features |
|---|---|
| **Demographics** | Gender, Senior Citizen, Partner, Dependents |
| **Location** | City, State, Zip Code, Latitude/Longitude |
| **Services** | Phone, Internet, Online Security, Tech Support, Streaming |
| **Billing** | Contract type, Payment Method, Monthly & Total Charges |
| **Churn Info** | Churn Label, Churn Value, Churn Score, Churn Reason, CLTV |

---

## ⚙️ Setup & Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/customer-churn-prediction.git
cd customer-churn-prediction
```

### 2. Create a Virtual Environment (Recommended)

```bash
python -m venv venv
source venv/bin/activate        # macOS/Linux
venv\Scripts\activate           # Windows
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Add the Dataset

Download the IBM Telco Customer Churn dataset and place it inside the `data/` folder:

```
data/telecom_customer_churn.csv
```

### 5. Launch Jupyter Notebook

```bash
jupyter notebook customer_churn_prediction.ipynb
```

---

## 🔄 Project Workflow

```
Data Loading → EDA → Data Cleaning → Feature Engineering
     → Model Training → Evaluation → Class Balancing → Final Model
```

| Step | Description |
|---|---|
| **1. Problem Statement** | Define business goal and churn impact |
| **2. Data Loading** | Load IBM Telco dataset from Excel |
| **3. Data Exploration** | Shape, dtypes, missing values, unique values |
| **4. Target Analysis** | Class distribution and imbalance check |
| **5. Data Cleaning** | Drop leakage columns, fix data types, handle nulls |
| **6. EDA** | Visualize churn vs contract, charges, tenure |
| **7. Feature Engineering** | Label encoding, scaling |
| **8. Model Training** | Logistic Regression, Decision Tree, Random Forest |
| **9. Evaluation** | Accuracy, Precision, Recall, F1, ROC-AUC |
| **10. Feature Importance** | Coefficient & impurity-based analysis |
| **11. Class Balancing** | `class_weight='balanced'` to improve Recall |
| **12. Final Model** | Balanced Logistic Regression selected |

---

## 📈 Model Results

| Model | Accuracy | Precision (Churn) | F1 (Churn) | ROC-AUC | Recall (Churn) |
|---|---|---|---|---|---|
| Logistic Regression | 80.7% | 0.69 | 0.62 | 0.862 | 0.57 |
| Decision Tree | 74.1% | 0.54 | 0.53 | 0.673 | 0.51 |
| Random Forest | 79.5% | 0.68 | 0.59 | 0.839 | 0.52 |
| **LR Balanced (Final)** | **75.1%** | **0.54** | **0.64** | **0.862** | **0.80** |

### Why Balanced Logistic Regression?

The standard model had a churn Recall of only **0.57**, meaning it missed nearly half of all actual churners. By using `class_weight='balanced'`, churn Recall improved to **0.80** — a **40% increase** — while maintaining the same ROC-AUC of **0.862**. In a business context, missing a churner leads to direct revenue loss, making Recall the priority metric.

---

## 🔍 Key Findings & Feature Insights

| Feature | Impact | Business Meaning |
|---|---|---|
| **Tenure Months** | High → Low Churn | Long-term customers are loyal and less likely to leave |
| **Total Charges** | High → Low Churn | Higher total spend indicates a longer customer relationship |
| **Monthly Charges** | High → High Churn | Price-sensitive customers leave when bills are high |
| **Contract Type** | Long-term → Low Churn | Annual/two-year contract customers rarely churn |
| **Dependents** | Yes → Low Churn | Customers with dependents have more reason to stay |
| **Payment Method** | Electronic Check → High Churn | Correlates with month-to-month contracts |
| **Online Security** | No → High Churn | Customers without security feel less value |
| **Tech Support** | No → High Churn | Lack of support increases frustration and churn risk |

---

## 💡 Business Recommendations

- **Promote long-term contracts** — Incentivize month-to-month customers to upgrade to annual plans
- **Address price sensitivity** — Offer loyalty discounts to high monthly charge customers
- **Focus on early retention** — New customers churn more; invest in onboarding and first-90-day experience
- **Bundle value-added services** — Promote Tech Support and Online Security to reduce churn risk

---

## ⚠️ Limitations

- Model is trained on a simulated dataset and may not generalize to all segments
- No hyperparameter tuning was performed
- Limited feature availability may affect prediction accuracy in production

---

## 🚀 Future Improvements

1. **SMOTE** — Oversample the minority class for better training balance
2. **GridSearchCV** — Systematic hyperparameter tuning
3. **XGBoost / LightGBM** — Advanced ensemble models for tabular data
4. **Threshold tuning** — Adjust the 0.5 classification threshold to further optimize Recall vs Precision

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-1.5+-green?logo=pandas)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.2+-orange?logo=scikit-learn)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.6+-blue)
![Seaborn](https://img.shields.io/badge/Seaborn-0.12+-teal)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

## 🙋‍♂️ Author

Made with ❤️ as an end-to-end ML classification project.  
Feel free to ⭐ the repo if you found it useful!
