# 📌 Predicting Credit Mix Category

## 📝 Project Overview
This project aims to predict the **Credit_Mix** category for a customer based on their financial data. The objective is to develop a robust classification model that provides actionable insights to improve credit health.

## 📂 Dataset Overview
The dataset consists of various financial attributes, including credit utilization, payment history, outstanding debt, and other credit-related metrics. Key features used in model training include:
- **Credit Utilization Ratio**
- **Debt-to-Income Ratio**
- **Number of Open Accounts**
- **Payment History**
- **Loan Types**

## 🎯 Objectives
- Perform **Exploratory Data Analysis (EDA)** to identify trends.
- Engineer meaningful features for model performance enhancement.
- Train multiple classification models and compare their performance.
- Evaluate models using various metrics and derive actionable insights.

---
## 🏗 Classification Models Used
### **1. Random Forest Classifier**
- **Best Parameters:**
  - `max_depth: None`
  - `min_samples_leaf: 1`
  - `min_samples_split: 2`
  - `n_estimators: 50`
- **Evaluation Metrics:**
  - Accuracy: 1.00
  - Precision: 1.00
  - Recall: 1.00
  - F1-Score: 1.00
  - ROC AUC: 0.9612
- **Insights:**
  - The model exhibited the best performance with perfect classification scores and high discriminative power.

### **2. Decision Tree Classifier**
- **Best Parameters:**
  - `max_depth: 10`
  - `min_samples_leaf: 1`
  - `min_samples_split: 2`
- **Evaluation Metrics:**
  - Accuracy: 1.00
  - Precision: 1.00
  - Recall: 1.00
  - F1-Score: 1.00
  - ROC AUC: 0.9479
- **Insights:**
  - Slightly lower ROC AUC compared to Random Forest, indicating a higher tendency to overfit.

### **3. Logistic Regression**
- **Best Parameters:**
  - `C: 10`
  - `penalty: l1`
- **Evaluation Metrics:**
  - Accuracy: 1.00
  - Precision: 1.00
  - Recall: 1.00
  - F1-Score: 1.00
  - ROC AUC: 0.9295
- **Insights:**
  - Performed well with optimized hyperparameters, showing a strong precision-recall balance.

### **4. Support Vector Machine (SVM)**
- **Parameters Used:**
  - `C: 1`, `kernel: rbf`, `gamma: scale`
- **Evaluation Metrics:**
  - Accuracy: 1.00
  - Precision: 1.00
  - Recall: 1.00
  - F1-Score: 1.00
  - ROC AUC: 0.9048
- **Insights:**
  - Lower AUC compared to other models, highlighting potential limitations in multi-class classification.

---
## 📊 Model Performance Comparison
| Model | Accuracy | Precision | Recall | F1-Score | ROC AUC |
|--------|------------|------------|---------|------------|------------|
| **Random Forest** | 1.00 | 1.00 | 1.00 | 1.00 | 0.9612 |
| **Decision Tree** | 1.00 | 1.00 | 1.00 | 1.00 | 0.9479 |
| **Logistic Regression** | 1.00 | 1.00 | 1.00 | 1.00 | 0.9295 |
| **SVM** | 1.00 | 1.00 | 1.00 | 1.00 | 0.9048 |

---
## 🔍 Key Recommendations
### **1. Model Selection**
- **Preferred Model:** Random Forest Classifier (highest ROC AUC and stability).
- **Next Steps:**
  - Increase `n_estimators` to evaluate performance at higher tree counts.
  - Adjust `max_depth` and `min_samples_split` to mitigate overfitting.

### **2. Feature Engineering**
- Utilize **feature importance scores** to remove redundant features.
- Introduce **interaction terms** between financial indicators.

### **3. Handle Class Imbalances**
- Apply **SMOTE** (Synthetic Minority Over-sampling Technique) or **weighted loss functions** to improve class representation.

### **4. Ensemble Approaches**
- Combine models using **stacking or blending** to leverage individual model strengths.
- Use a meta-classifier (e.g., Logistic Regression) to aggregate predictions.

### **5. Deployment & Monitoring**
- Deploy the chosen model in a **production environment**.
- Set up real-time performance monitoring to detect data drift.
- Schedule periodic retraining with updated datasets.

---
## 🚀 How to Run This Project
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/credit-mix-prediction.git
   cd credit-mix-prediction
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Train the model:
   ```bash
   python train_model.py
   ```
4. Evaluate the model:
   ```bash
   python evaluate.py
   ```

---
## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
## 📩 Contact
📧 **Arman Hossain** - armanhossainiueee@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/arman-hossain-1413991a4/)  
🔗 [GitHub](https://github.com/Arman3875)  

---
> **Note:** This project is a learning exercise in classification modeling and credit risk analysis.
