# 📦 Invoice Intelligence System

An AI-powered internal analytics portal for vendor invoice management — built with Machine Learning and Streamlit.

🔗 **Live App:** [https://vsy2xnjc6k56cajlysqdpn.streamlit.app/](https://vsy2xnjc6k56cajlysqdpn.streamlit.app/)

---

## 🧠 Overview

The **Invoice Intelligence System** is a machine learning pipeline that helps finance and procurement teams:

- **Predict freight costs** accurately for vendor invoices
- **Flag risky invoices** that require manual approval
- **Reduce financial leakage** caused by invoice anomalies
- **Speed up finance operations** with automated risk assessment

---

## 🚀 Features

### 🚚 Freight Cost Prediction
- Predicts freight cost based on **Quantity** and **Invoice Dollars**
- Trained using Linear Regression, Decision Tree, and Random Forest
- Best model selected automatically based on lowest MAE

### 🚨 Invoice Manual Approval Flag
- Classifies invoices as **Safe** or **Requires Manual Approval**
- Uses a Random Forest Classifier with GridSearchCV tuning
- Flags invoices with abnormal cost discrepancies or delivery delays

---

## 🗂️ Project Structure

```
Invoice Intelligence System/
│
├── app.py                        # Streamlit web application
├── requirements.txt              # Python dependencies
│
├── frieght_cost_prediction/      # Freight cost ML pipeline
│   ├── data_preprocessing.py
│   ├── modeling_evaluation.py
│   └── train.py
│
├── invoice_flagging/             # Invoice risk ML pipeline
│   ├── data_preprocessing.py
│   ├── modeling_evaluation.py
│   └── train.py
│
├── inference/                    # Prediction scripts
│   ├── predict_freight.py
│   └── predict_invoice_flag.py
│
├── notebooks/                    # Exploratory analysis
│   ├── Predicting_Freight_Cost.ipynb
│   └── Invoice Flagging.ipynb
│
└── models/                       # Saved trained models (not pushed to GitHub)
    ├── predict_freight_model.pkl
    ├── predict_flag_invoice.pkl
    └── scaler.pkl
```

---

## ⚙️ Setup & Installation

### 1. Clone the repository
```bash
git clone https://github.com/crazyshubham/-Invoice-Intelligence-System.git
cd -Invoice-Intelligence-System
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Set up the database
Place your `inventory.db` SQLite database inside a `Data/` folder:
```
Invoice Intelligence System/
└── Data/
    └── inventory.db
```

### 4. Train the models
```bash
# Train freight cost model
python frieght_cost_prediction/train.py

# Train invoice flagging model
cd invoice_flagging
python train.py
```

### 5. Run the app
```bash
streamlit run app.py
```

---

## 🤖 ML Models

| Module | Model | Metric |
|--------|-------|--------|
| Freight Cost Prediction | Linear Regression | R² = 97% |
| Invoice Risk Flagging | Random Forest Classifier | F1-Score optimized |

---

## 🛠️ Tech Stack

- **Python 3.13**
- **Scikit-learn** — ML models
- **Pandas / NumPy** — Data processing
- **Streamlit** — Web app
- **Plotly** — Visualizations
- **SQLite** — Database
- **Joblib** — Model persistence

---

## 👤 Author

**Shubham Upadhyay**  
[GitHub](https://github.com/crazyshubham)
