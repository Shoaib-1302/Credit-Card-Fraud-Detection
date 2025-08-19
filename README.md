Credit Card Fraud Detection
This project demonstrates credit card fraud detection using an in-built dataset, including data exploration, preprocessing, model training, evaluation, and deployment.

Project Overview
The goal of this project is to build a model that can accurately identify fraudulent credit card transactions. We use a publicly available dataset and employ a Logistic Regression model, addressing the significant class imbalance present in the data.

Dataset
The dataset used in this project is the Credit Card Fraud Detection dataset available through fetch_openml. It contains anonymized transaction data with features V1 through V28, the transaction Amount, and the target variable Class (0 for non-fraudulent, 1 for fraudulent).

Steps Taken
Data Loading: The dataset was loaded into a pandas DataFrame.
Data Exploration: Initial analysis was performed to understand the data structure, check for missing values, and examine the distribution of the target variable.
Data Preprocessing:
Features were scaled using StandardScaler.
The dataset was split into training and testing sets using train_test_split with stratification to maintain the original class distribution in both sets.
SMOTE (Synthetic Minority Over-sampling Technique) was applied to the training data to handle the class imbalance.
Model Training: A Logistic Regression model was trained on the SMOTE-resampled training data.
Model Evaluation: The model's performance was evaluated on the original, unseen test set using metrics such as precision, recall, F1-score, confusion matrix, and ROC AUC score.
Model Deployment: The trained model was saved and can be loaded for making predictions on new data.
Results
The model achieved a high recall for the fraudulent class, indicating its ability to identify a large percentage of fraudulent transactions. However, the precision was low, suggesting a need for further optimization to reduce false positives. The ROC AUC score indicates good overall discriminative ability.

Key findings from the evaluation:

Recall (Fraudulent Class): 0.92
Precision (Fraudulent Class): 0.06
ROC AUC Score: 0.9707
