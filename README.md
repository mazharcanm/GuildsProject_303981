# GuildsProject_303981
AI &amp; ML Project - Guilds
# **Guild Membership Prediction Project**

## **Team Members**
- **Captain**: Berke Tayfun Akseki (Student ID: 303981)
- **Member 1**: Mazhar Can Muradoglu (Student ID: 306951)
- **Member 2**: Efe Aydin (Student ID: 305041)

---

## **Introduction**
The **Guild Membership Prediction Project** uses machine learning to predict the guild assignment of individuals in a fictional world based on features such as stamina, mystical indices and wizardry skill. The project evaluates three models : Logistic Regression, Random Forest and Linear SVM to determine the most effective approach for this classification task.

By analyzing the performance of these models, the project aims to explore the trade offs between speed, interpretability and accuracy in machine learning.

---

## **Methods**

### **Dataset**
- The dataset includes 30+ features related to physical, mental, and mystical characteristics.
- **Target Variable**: `Guild_Membership` (categorical).
- Features include:
  - **Numerical**: `Mystical_Index`, `Rune_Power`, `Gold_Pouches_Per_Year`, etc.
  - **Categorical**: `Presence`/`Absence` indicators like `Dragon_status_Presence`.

### **Preprocessing**
1. Missing values were handled:
   - **Numerical**: Replaced with column means.
   - **Categorical**: Replaced with column modes.
2. Binary categorical features (e.g., `Present`/`Absent`) were mapped to `1`/`0`.
3. All features were standardized using `StandardScaler`.

### **Models**
1. **Logistic Regression**:
   - Chosen for its simplicity and efficiency.
   - Solver: `liblinear`.
2. **Random Forest**:
   - Ensemble method leveraging decision trees.
   - Number of trees: 50 (optimized for speed).
3. **Linear SVM**:
   - Kernel: Linear, providing faster training compared to non-linear kernels.

### **Environment Setup**
To recreate the environment:
```
bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib

```
# Experimental Design

## Main Purpose
The goal is to evaluate and compare the performance of three models—**Logistic Regression**, **Random Forest**, and **Linear SVM**—on predicting guild memberships.

## Baselines
Each model was tested and compared using:

- **Accuracy**: Overall correctness of predictions.
- **F1 Score**: Balances precision and recall to account for class imbalance.

## Evaluation Metrics

1. **Accuracy**  
   Measures the proportion of correct predictions.

2. **F1 Score (Weighted)**  
   Evaluates performance across imbalanced classes by taking into account both precision and recall.

# Results

## Model Performance
The results for each model are as follows:

- **Logistic Regression**: Accuracy 85.89%, F1 Score 0.8173  
- **Random Forest**: Accuracy 85.90%, F1 Score 0.8100  
- **Linear SVM**: Accuracy 85.89%, F1 Score 0.8032

# Classification Reports

## Logistic Regression

| Class | Precision | Recall | F1-score | Support |
|:-----:|:---------:|:------:|:--------:|:-------:|
| **0** | 0.00      | 0.00   | 0.00     | 202     |
| **1** | 0.49      | 0.12   | 0.20     | 1593    |
| **2** | 0.87      | 0.98   | 0.92     | 10889   |
| **Accuracy**     | -        | -      | 0.86     | 12684   |
| **Macro Avg**    | 0.45     | 0.37   | 0.37     | 12684   |
| **Weighted Avg** | 0.81     | 0.86   | 0.82     | 12684   |

---

## Random Forest

| Class | Precision | Recall | F1-score | Support |
|:-----:|:---------:|:------:|:--------:|:-------:|
| **0** | 0.00      | 0.00   | 0.00     | 202     |
| **1** | 0.49      | 0.08   | 0.14     | 1593    |
| **2** | 0.87      | 0.99   | 0.92     | 10889   |
| **Accuracy**     | -        | -      | 0.86     | 12684   |
| **Macro Avg**    | 0.45     | 0.36   | 0.35     | 12684   |
| **Weighted Avg** | 0.81     | 0.86   | 0.81     | 12684   |

---

## Linear SVM

| Class | Precision | Recall | F1-score | Support |
|:-----:|:---------:|:------:|:--------:|:-------:|
| **0** | 0.00      | 0.00   | 0.00     | 202     |
| **1** | 0.51      | 0.04   | 0.08     | 1593    |
| **2** | 0.86      | 0.99   | 0.92     | 10889   |
| **Accuracy**     | -        | -      | 0.86     | 12684   |
| **Macro Avg**    | 0.46     | 0.35   | 0.33     | 12684   |
| **Weighted Avg** | 0.80     | 0.86   | 0.80     | 12684   |

# Conclusions

## Summary
- **Random Forest** achieved the highest accuracy (85.90%) and F1 Score (0.8100), indicating its robustness in classification.  
- **Logistic Regression** and **Linear SVM** had similar performance, with Logistic Regression being slightly better on F1 Score.

## Future Directions
- Perform hyperparameter tuning for all models to further improve performance.  
- Experiment with additional models, such as Gradient Boosting or deep learning approaches.  
- Address class imbalance by oversampling or undersampling techniques.

# Model Comparison Table

| **Model**             | **Accuracy** | **F1 Score** |
|:---------------------:|:------------:|:------------:|
| Logistic Regression   | 85.89%       | 0.8173       |
| Random Forest         | 85.90%       | 0.8100       |
| Linear SVM            | 85.89%       | 0.8032       |
