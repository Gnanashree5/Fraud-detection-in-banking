# 🔒 Fraud Detection in Banking

## 📄 Project Overview
This project aims to detect fraudulent credit card transactions using a **Random Forest Classifier**. The dataset used is from Kaggle, containing **284,807 transactions**, with only **0.17% fraud cases**, making it highly imbalanced.

## 📚 Dataset Details
- **Source**: [Kaggle Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- **Total Transactions**: 284,807
- **Fraudulent Cases**: 492 (~0.17% of the data)
- **Features**:
  - **Time**: Seconds elapsed since the first transaction.
  - **V1-V28**: PCA-transformed anonymized features.
  - **Amount**: Transaction amount.
  - **Class**: 0 = Non-Fraud, 1 = Fraud.

## ⚙️ Data Preprocessing
🔄 **Handling Class Imbalance**:
- **Undersampling**: Equal samples of fraud and non-fraud transactions.
- **Feature Scaling**: StandardScaler applied to normalize the **Amount** column.
- **Feature Selection**: Dropped the "Time" column as it was not useful.

## 🧑‍💻 Model Training
- **Algorithm Used**: RandomForestClassifier (100 estimators, random_state=42)
- **Train-Test Split**: 80% training, 20% testing (stratified sampling)
- **Hyperparameters**:
  - `n_estimators=100`
  - `random_state=42`

## 📊 Model Performance
| Metric        | Class 0 (Non-Fraud) | Class 1 (Fraud) |
|--------------|-------------------|-----------------|
| **Precision** | 94%                 | 96%             |
| **Recall**    | 96%                 | 94%             |
| **F1-score**  | 95%                 | 95%             |
| **Accuracy**  | **95% Overall**      |                 |

🔍 **Key Insights**:
✅ High precision (96%) for fraud detection → Fewer false fraud alerts.
✅ High recall (94%) for fraud → Model correctly identifies most frauds.
✅ Balanced F1-score (95%) → Effective fraud detection with minimal false alarms.

## ✨ Feature Importance
- **Most Important Features:** V12, V14, V10, and **Transaction Amount**.
- **Visualization of feature importance included in the notebook**.

## 🚀 Future Improvements
- 🌟 **Enhance Recall**: Use **SMOTE** for better class balance.
- 👨‍💻 **Hyperparameter Tuning**: Optimize tree depth, feature selection.
- 🛠️ **Deploy Model**: Implement real-time fraud detection.

```

## 🎨 Visualizations
- **Confusion Matrix Heatmap** ✅
- **ROC-AUC Curve** ✅
- **Feature Importance Plot** ✅


## ✨ Acknowledgment
This project is inspired by the Kaggle **Credit Card Fraud Detection Dataset** and aims to improve fraud detection methods.

---
🚀 **Let's make online transactions safer!**

