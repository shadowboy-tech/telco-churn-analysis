# 📡 Telco Customer Churn Analysis & Prediction

> A complete end-to-end machine learning pipeline for analysing and predicting customer churn in the telecommunications industry — from raw data to actionable retention insights.

---

## 🗂️ Project Overview

Customer churn is one of the most costly problems in the telecom sector. This project builds a full ML pipeline on the **IBM Telco Customer Churn Dataset (7,043 customers · 21 features)** to:

- Understand *why* customers leave through exploratory data analysis
- Identify the most influential churn drivers via feature selection
- Train and compare four binary classification models
- Surface actionable business recommendations to reduce churn

---

## 📁 Repository Structure

```
telco-churn-analysis/
│
├── customer_churn_analysis.ipynb           # Main Jupyter Notebook (source)
├── customer-churn-analysis-and-prediction.ipynb  # Pre-executed notebook with outputs
├── Telco_Customer_Churn_Dataset___1_.csv   # Dataset (place here before running)
├── README.md                               # You are here
│
└── figures/                           # Auto-generated plots (after running notebook)
    ├── fig_churn_distribution.png
    ├── fig_numeric_distributions.png
    ├── fig_categorical_churnrate.png
    ├── fig_correlation_heatmap.png
    ├── fig_feature_importance.png
    ├── fig_cv_comparison.png
    ├── fig_model_comparison.png
    ├── fig_roc_curves.png
    └── fig_confusion_matrices.png
```

---

## 🧪 Project Workflow

The notebook is structured into **6 sequential tasks**:

| Task | Description |
|------|-------------|
| **Task 1** | Data loading, cleaning, EDA, and encoding |
| **Task 2** | Stratified 80/20 train-test split + feature scaling |
| **Task 3** | Feature selection via Mutual Information & Random Forest importance |
| **Task 4** | Model selection — Logistic Regression, Decision Tree, Random Forest, Gradient Boosting |
| **Task 5** | Model training with 5-fold cross-validation |
| **Task 6** | Evaluation — Accuracy, Precision, Recall, F1, ROC-AUC + business interpretation |

---

## 📊 Key Results

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---|---|---|---|---|
| Logistic Regression | ~80% | ~66% | ~76% | ~71% | ~0.84 |
| Decision Tree | ~78% | ~63% | ~74% | ~68% | ~0.81 |
| Random Forest | ~82% | ~69% | ~76% | ~72% | ~0.85 |
| **Gradient Boosting** | **~83%** | **~70%** | **~78%** | **~74%** | **~0.86** |

> 🏆 **Gradient Boosting** achieved the best ROC-AUC and F1-Score on the held-out test set.

---

## 🔑 Top Churn Drivers

1. **Contract type (Month-to-month)** — the single strongest predictor; these customers churn 3× more
2. **Tenure** — longer-tenured customers are significantly more loyal
3. **Monthly Charges** — higher bills correlate strongly with churn risk
4. **Internet Service (Fiber Optic)** — unexpectedly high churn; may indicate service quality gaps
5. **Tech Support & Online Security** — customers without these add-ons churn far more often

---

## 💡 Business Recommendations

- 🎯 **Incentivise long-term contracts** for month-to-month customers (discounts, loyalty perks)
- 💰 **Trigger retention calls** for customers with monthly charges > $70 and tenure < 12 months
- 🛠️ **Bundle Tech Support & Online Security** to improve stickiness
- 🔎 **Audit Fiber Optic service quality** — churn rate is disproportionately high
- 📈 **Deploy model in a monthly scoring pipeline** to flag high-risk accounts proactively

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3.10+ | Core language |
| Pandas / NumPy | Data manipulation |
| Matplotlib / Seaborn | Visualisation |
| Scikit-learn | Preprocessing, modelling, evaluation |
| Jupyter Notebook | Interactive development environment |

---

## ⚙️ Setup & Usage

### 1. Clone the repository
```bash
git clone https://github.com/shadowboy-tech/telco-churn-analysis.git
cd telco-churn-analysis
```

### 2. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 3. Add the dataset
Place `Telco_Customer_Churn_Dataset___1_.csv` in the root directory, then update the path in **Task 1** of the notebook:
```python
DATA_PATH = "Telco_Customer_Churn_Dataset___1_.csv"
```

### 4. Launch the notebook
```bash
jupyter notebook customer_churn_analysis.ipynb
```

---

## 📌 Dataset

- **Source:** [IBM Sample Datasets / Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Size:** 7,043 rows × 21 columns
- **Target:** `Churn` (Yes / No) — ~26.5% positive rate

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

---

## 👤 Author

**Muhammad Inuwa Muhammad**  
*AI/ML Engineer*
🔗 [LinkedIn](https://linkedin.com/in/muhammad-inuwa-muhammad)
