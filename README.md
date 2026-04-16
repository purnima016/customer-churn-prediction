# 📡 Customer Churn Prediction — Telecom Industry

> A production-grade machine learning project for identifying at-risk customers, understanding churn drivers, and enabling proactive retention strategies.

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3+-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-150458?style=flat-square&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat-square&logo=jupyter&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

---

## 📌 Project Overview

Customer churn — when a customer discontinues a service — is one of the most costly and preventable problems in the telecom industry. Studies show that acquiring a new customer costs **5–10× more** than retaining an existing one.

This project builds a complete **end-to-end ML pipeline** that:
- Simulates a realistic telecom customer dataset (7,000 records, 10 features)
- Performs thorough Exploratory Data Analysis (EDA)
- Trains and compares **Logistic Regression** and **Random Forest** classifiers
- Evaluates performance with accuracy, ROC-AUC, confusion matrix, and classification report
- Derives **actionable business insights** about which customers churn and why

---

## 🗂️ Project Structure

```
customer-churn-prediction/
│
├── customer_churn_prediction.ipynb   # Main Jupyter Notebook (full pipeline)
├── README.md                          # Project documentation (this file)
│
└── output/                            # Auto-generated visualizations
    ├── churn_by_segments.png
    ├── feature_distributions.png
    ├── correlation_heatmap.png
    ├── confusion_matrices.png
    ├── roc_curves.png
    ├── feature_importance.png
    └── business_dashboard.png
```

---

## 🧰 Tech Stack

| Tool | Purpose |
|---|---|
| `Python 3.10+` | Core language |
| `pandas` | Data manipulation & analysis |
| `numpy` | Numerical operations |
| `scikit-learn` | ML models, preprocessing, evaluation |
| `matplotlib` | Base plotting |
| `seaborn` | Statistical visualizations |
| `Jupyter Notebook` | Interactive development environment |

---

## 📊 Dataset Features

The dataset simulates a realistic telecom churn scenario with the following features:

| Feature | Type | Description |
|---|---|---|
| `tenure` | Numeric | Months the customer has been with the company |
| `contract_type` | Categorical | Month-to-Month / One Year / Two Year |
| `payment_method` | Categorical | Electronic Check / Bank Transfer / Credit Card / Mailed Check |
| `internet_service` | Categorical | DSL / Fiber Optic / None |
| `tech_support` | Categorical | Yes / No |
| `online_security` | Categorical | Yes / No |
| `num_products` | Numeric | Number of services subscribed (1–5) |
| `num_complaints` | Numeric | Number of support complaints filed |
| `monthly_charges` | Numeric | Monthly billing amount (USD) |
| `total_charges` | Numeric | Cumulative spend with the company |
| `churn` | Binary | **Target** — 1 = Churned, 0 = Retained |

---

## 🤖 Models Trained

### 1. Logistic Regression
- Interpretable baseline model
- Uses `StandardScaler` preprocessing
- Evaluated with 5-fold stratified cross-validation

### 2. Random Forest (🏆 Best)
- Ensemble of 200 decision trees
- `class_weight='balanced'` for class imbalance
- Provides native feature importance scores

---

## 📈 Results

| Model | Test Accuracy | Test ROC-AUC | CV ROC-AUC |
|---|---|---|---|
| Logistic Regression | ~85–87% | ~0.88–0.92 | ~0.88–0.91 |
| **Random Forest** | **~89–91%** | **~0.93–0.96** | **~0.93–0.95** |

> **Random Forest outperforms Logistic Regression** across all metrics by capturing non-linear feature interactions that a linear model cannot represent.

---

## 🔑 Key Business Insights

1. **Contract type is the #1 churn predictor.**  
   Month-to-month customers churn at far higher rates than annual or bi-annual contract holders. → *Offer incentives to switch to longer contracts.*

2. **New customers (< 12 months) are highest risk.**  
   Churn probability drops significantly after the first year. → *Invest in a structured onboarding & early-stage retention program.*

3. **Fiber Optic users churn despite paying premium prices.**  
   Suggests a quality-expectation gap. → *Audit Fiber Optic service quality and satisfaction scores.*

4. **Each support complaint substantially increases churn risk.**  
   Complaints are a leading indicator, not just a symptom. → *Implement proactive outreach after every complaint.*

5. **Electronic check users show higher churn than auto-pay customers.**  
   → *Incentivize migration to automatic payment methods.*

---

## 🚀 How to Run

### Prerequisites
Make sure you have Python 3.10+ installed.

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/customer-churn-prediction.git
cd customer-churn-prediction
```

### 2. Install Dependencies
```bash
pip install pandas numpy scikit-learn matplotlib seaborn notebook
```

Or with a `requirements.txt`:
```bash
pip install -r requirements.txt
```

### 3. Launch the Notebook
```bash
jupyter notebook customer_churn_prediction.ipynb
```

### 4. Run All Cells
Use **Kernel → Restart & Run All** to execute the full pipeline from scratch.

---

## 📦 requirements.txt

```
pandas>=2.0.0
numpy>=1.24.0
scikit-learn>=1.3.0
matplotlib>=3.7.0
seaborn>=0.12.0
notebook>=7.0.0
```

---

## 🗺️ Roadmap / Future Improvements

- [ ] Hyperparameter tuning with `GridSearchCV` / `Optuna`
- [ ] Add `XGBoost` and `LightGBM` for performance benchmarking
- [ ] SHAP values for per-customer explainability
- [ ] Flask/FastAPI deployment for real-time scoring API
- [ ] Customer Lifetime Value (CLV) integration
- [ ] Dashboard with Streamlit or Power BI

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 👤 Author

**Your Name**  
📧 your.email@example.com  
🔗 [LinkedIn](https://linkedin.com/in/yourprofile) · [GitHub](https://github.com/yourusername) · [Portfolio](https://yourportfolio.com)

---

> *Built as part of a data science portfolio. Suitable for internship applications in Data Science, ML Engineering, and Business Analytics roles.*
