# **Drug Prediction using Machine Learning**

## **Overview**
This project implements a **Decision Tree classifier** for predicting drug effectiveness based on sparse matrix data. The dataset consists of **binary target labels** with features representing non-zero values. **Principal Component Analysis (PCA), SMOTE, and Z-score normalization** were applied for data preprocessing and feature selection. The final **F1-score achieved was 0.84686**.

---

## **Approach**
### **1. Data Preprocessing**
- 🛠️ **Null value handling** – Replaced missing values with the **mean**.
- 📊 **Z-score normalization** – Standardized feature values.
- 🏷️ **Feature Reduction** – **PCA** was applied to remove redundant data.

### **2. Handling Data Imbalance**
- 🔄 **SMOTE (Synthetic Minority Oversampling Technique)** was used to balance the dataset.

### **3. Model Training & Hyperparameter Tuning**
- 🏆 **Cross-validation using GridSearchCV**:
  - Optimized hyperparameters to select the best model.
  - **Best Model**: `DecisionTreeClassifier(criterion='entropy', max_depth=20)`
  - **F1-score: 0.84686**
  
- ✅ **Alternative Model Evaluated**:
  - **Naive Bayes (GaussianNB)** achieved a higher **F1-score of 0.98**, but Decision Tree provided more accurate predictions.

---

## **Final Model Selection**
| Max Depth | Criterion | F1-Score |
|-----------|-----------|----------|
| 20        | Gini      | 0.82     |
| 20        | Entropy   | 0.84     |

📌 **Decision Tree (Entropy) was selected as the final model** due to its superior accuracy.

---

## **Execution Steps**
1. 📥 **Load dataset** into `train_df` and `test_df`.
2. 🔍 **Perform data preprocessing** (null handling, normalization, PCA).
3. 🎯 **Train the Decision Tree model** using the best parameters.
4. 📊 **Generate predictions** and save output in `predictions.txt`.
5. ⏳ **Runtime:** ~120-180 minutes.

---

## **Results & Insights**
- ✅ **Best Model**: Decision Tree (`criterion='entropy', max_depth=20`)
- 🏆 **Final F1-score**: `0.84686`
- ⚡ **Naive Bayes performed well (F1-score = 0.98)** but Decision Tree was chosen for better real-world performance.

---

## **Future Work**
- 🏗 **Test additional feature selection techniques** for better generalization.
- 🚀 **Explore deep learning models** (Neural Networks) for improved classification.
- 📈 **Optimize hyperparameters further** to enhance prediction accuracy.

---

## **Author**
👤 **Preethi Ranganathan**  
📧 [prangana@gmu.edu](mailto:prangana@gmu.edu)  

---

