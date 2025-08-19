# 💳 Credit Card Fraud Detection

This project demonstrates **Credit Card Fraud Detection** using a publicly available dataset, showcasing the complete pipeline from **data exploration** to **model deployment**.  

---

## 📌 Project Overview
The goal of this project is to build a model that can accurately **identify fraudulent credit card transactions**.  
We use the **Credit Card Fraud Detection dataset** and employ a **Logistic Regression** model, while addressing the **significant class imbalance** present in the data.

---

## 📂 Dataset
- Dataset: **Credit Card Fraud Detection** (via `fetch_openml`)  
- Features:
  - **V1–V28** → anonymized transaction features (PCA transformed)
  - **Amount** → transaction amount  
  - **Class** → target variable (`0 = non-fraud`, `1 = fraud`)  

---

## 🛠 Steps Taken

### 1️⃣ Data Loading
- Loaded into a **pandas DataFrame** for analysis.  

### 2️⃣ Data Exploration
- Checked data structure, missing values, and **target variable imbalance**.  

### 3️⃣ Data Preprocessing
- Applied **StandardScaler** for feature scaling.  
- Split into **train/test sets** with stratification to preserve class ratios.  
- Applied **SMOTE (Synthetic Minority Over-sampling Technique)** to handle severe class imbalance.  

### 4️⃣ Model Training
- Trained a **Logistic Regression** model on the **SMOTE-resampled training set**.  

### 5️⃣ Model Evaluation
- Evaluated on the **unseen test set** using multiple metrics:  
  - ✅ **Precision**  
  - ✅ **Recall**  
  - ✅ **F1-Score**  
  - ✅ **Confusion Matrix**  
  - ✅ **ROC AUC Score**  

### 6️⃣ Model Deployment
- Saved the trained model for **future predictions on new transactions**.  

---

## 📊 Results

Key findings from model evaluation:

- **Recall (Fraudulent Class):** `0.92` ✅ (captures most fraud cases)  
- **Precision (Fraudulent Class):** `0.06` ⚠️ (high false positives)  
- **ROC AUC Score:** `0.9707` 🚀 (strong discriminative ability)  

> 🔎 **Interpretation:**  
> The model is excellent at **catching frauds (high recall)**, but suffers from **low precision** (too many false alarms). Further optimization (e.g., advanced models, threshold tuning, ensemble methods) is needed.  

---

## 📦 Tech Stack
- **Python** 🐍  
- **Pandas, NumPy** → Data handling  
- **Scikit-learn** → Preprocessing, modeling, evaluation  
- **Imbalanced-learn (SMOTE)** → Handling class imbalance  

---

## 🚀 Future Improvements
- Experiment with **tree-based models** (Random Forest, XGBoost, LightGBM).  
- Apply **threshold tuning** for better precision-recall tradeoff.  
- Use **anomaly detection methods** for fraud detection.  
- Build a **real-time detection system** with streaming data.  

---

## 📑 References
- Dataset: [Credit Card Fraud Detection on OpenML](https://www.openml.org/d/1597)  
- Imbalanced-learn Documentation: [SMOTE](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.SMOTE.html)  

---

## 🏁 Conclusion
This project provides a **solid baseline** for fraud detection with **Logistic Regression** and **SMOTE**.  
It highlights the challenges of **imbalanced data** and the trade-off between **recall vs. precision** in financial fraud detection.  

