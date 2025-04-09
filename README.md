💳 Credit Card Fraud Detection

🧠 Project Overview
This project aims to improve the detection of fraudulent credit card transactions using various machine learning techniques. Credit card fraud is a significant issue in the financial sector, and its prevention is critical to minimizing financial loss and maintaining trust.

📂 Contents
Credit_card_fraud_detection_Final.ipynb – Main notebook for EDA, model training, evaluation, and results.

CCFraudDetection.pdf – Data storytelling presentation summarizing methodology, findings, and recommendations.

Root Cause Analysis.pdf – In-depth analysis of class imbalance and model performance challenges.

🧩 Problem Statement
Credit card fraud detection datasets are highly imbalanced, with fraudulent transactions representing a tiny portion of the total data. Traditional models often exhibit high accuracy but fail to detect fraudulent cases effectively, which is the primary concern.

⚙️ Project Pipeline
Data Exploration: Loaded and analyzed features relevant for model building.

Preprocessing & EDA: Detected imbalances and trends in transaction data.

Data Splitting: Stratified k-fold cross-validation used to retain class distribution.

Modeling:
Logistic Regression
Decision Tree
Random Forest
XGBoost

Imbalance Handling:
SMOTE (Synthetic Minority Oversampling)
ADASYN (Adaptive Synthetic Sampling)

Evaluation Metrics:
Accuracy, Precision, Recall, F1-Score, ROC-AUC

📊 Findings
Without balancing, models achieved high accuracy but low sensitivity.

SMOTE and ADASYN significantly improved recall and F1-score.

XGBoost with SMOTE outperformed others in detecting fraudulent transactions.

Model	Accuracy	Recall	F1-Score	ROC AUC
Logistic Regression (Raw)	0.99	0.68	0.70	0.94
XGBoost (SMOTE)	0.99	0.82	0.80	0.96
Decision Tree (ADASYN)	0.97	0.81	0.11	0.91

💡 Recommendations
Use XGBoost with SMOTE for the best balance between sensitivity and precision.
Avoid relying on accuracy as the primary metric for imbalanced datasets.
Incorporate human verification or threshold tuning for deployment scenarios.

💰 Cost-Benefit Consideration
Small banks should prioritize precision to avoid excessive false positives.
Large banks should focus on recall to prevent high-value fraud losses.

✅ Conclusion
Combining oversampling techniques with robust models like XGBoost improves fraud detection substantially. This project highlights the importance of proper metric evaluation and data balancing in solving real-world imbalanced classification problems.
