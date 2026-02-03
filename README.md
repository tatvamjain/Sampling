# Sampling Techniques on Imbalanced Credit Card Fraud Dataset

## 📌 Objective
The objective of this assignment is to analyze the effect of different **sampling techniques** on a **highly imbalanced credit card fraud dataset** and to study how these techniques influence the **accuracy of multiple machine learning models**.

---

## 📊 Dataset Description
- **Dataset Name:** Creditcard_data.csv  
- **Problem Type:** Binary Classification  
- **Target Variable:** `Class`  
  - `0` → Non-Fraud  
  - `1` → Fraud  
- **Issue:** Highly imbalanced class distribution  
- **Dataset Link:**  
  https://github.com/AnjulaMehto/Sampling_Assignment/blob/main/Creditcard_data.csv  

---

## ⚖️ Class Balancing Strategy
The original dataset was highly imbalanced, which could lead to biased model predictions.  
To address this issue, **Random Over Sampling (ROS)** was applied to balance the dataset.

Random Over Sampling duplicates minority class samples to ensure:
- Equal representation of both classes  
- Reduced bias during model training  
- Improved learning for minority (fraud) cases  

---

## 🧪 Sampling Techniques Used
After balancing the dataset, the following sampling techniques were applied to generate **five different dataset samples**:

1. **Simple Random Sampling**  
   Random selection of samples from the balanced dataset.

2. **Stratified Sampling**  
   Maintains class distribution while creating samples.

3. **Systematic Sampling**  
   Selects every *k-th* data point from the dataset.

4. **Cluster Sampling**  
   Groups data into clusters and samples selected clusters.

5. **Bootstrap Sampling**  
   Sampling with replacement, allowing duplicate samples to enhance robustness.

> **Note:** These techniques were applied *after class balancing* and were used to generate multiple evaluation samples, not for handling class imbalance.

---

## 🤖 Machine Learning Models Used

| Model Code | Algorithm |
|-----------|-----------|
| M1 | Logistic Regression |
| M2 | Decision Tree |
| M3 | Naive Bayes |
| M4 | Random Forest |
| M5 | Support Vector Machine (SVM) |

All models were trained using standard preprocessing steps and evaluated using **accuracy score**.

---

## 📈 Accuracy Results Table (%)

| Model / Sampling | Sampling1<br>(Simple Random) | Sampling2<br>(Stratified) | Sampling3<br>(Systematic) | Sampling4<br>(Cluster) | Sampling5<br>(Bootstrap) |
|------------------|-----------------------------|---------------------------|---------------------------|------------------------|--------------------------|
| **M1_LogisticRegression** | 90.22 | 86.96 | 89.22 | 94.57 | 95.65 |
| **M2_DecisionTree** | 94.57 | 97.83 | 95.10 | 100.00 | 98.91 |
| **M3_NaiveBayes** | 76.09 | 61.96 | 80.39 | 64.13 | 71.74 |
| **M4_RandomForest** | 100.00 | 98.91 | 100.00 | 100.00 | 100.00 |
| **M5_SVM** | 95.65 | 94.57 | 96.08 | 97.83 | 97.83 |

- **Highest Accuracy:** 100.00%  
- **Lowest Accuracy:** 61.96%

---

## 🏆 Best Sampling Technique for Each Model

| Model | Best Sampling Technique | Best Accuracy |
|------|------------------------|--------------|
| M1 – Logistic Regression | Bootstrap Sampling | 95.65% |
| M2 – Decision Tree | Cluster Sampling | 100.00% |
| M3 – Naive Bayes | Systematic Sampling | 80.39% |
| M4 – Random Forest | Multiple (Tie) | 100.00% |
| M5 – SVM | Cluster / Bootstrap (Tie) | 97.83% |

---

## 🌟 Overall Best Combination
- **Model:** Decision Tree (M2)  
- **Sampling Technique:** Cluster Sampling  
- **Accuracy:** 100.00%

---

## 🔍 Discussion

### Model Performance Analysis
- **Random Forest (M4)** showed the most stable behavior, achieving **100% accuracy** across most sampling techniques.
- **Decision Tree (M2)** performed exceptionally well and achieved perfect accuracy with **Cluster Sampling**.
- **SVM (M5)** showed consistently strong performance with accuracies ranging from **94.57% to 97.83%**.
- **Logistic Regression (M1)** showed higher variability and performed best with **Bootstrap Sampling**.
- **Naive Bayes (M3)** achieved comparatively lower accuracy, indicating weaker suitability for this dataset.

### Sampling Technique Analysis
- **Cluster Sampling** provided the best overall results and delivered top performance across multiple models.
- **Bootstrap Sampling** significantly improved Logistic Regression and SVM performance.
- **Systematic Sampling** worked best for Naive Bayes and achieved perfect accuracy for Random Forest.
- **Stratified Sampling** did not outperform other techniques significantly since the dataset was already balanced.

---

## ✅ Conclusion
This experiment demonstrates that:
- Balancing the dataset using **Random Over Sampling (ROS)** significantly improves model performance.
- Sampling techniques influence each machine learning model differently.
- **Cluster Sampling** emerged as the most effective sampling strategy overall.
- **Random Forest** proved to be the most stable and reliable model for this dataset.

### 🔑 Final Insights
- **Best Overall Combination:** Decision Tree with Cluster Sampling (100% accuracy)  
- **Most Stable Model:** Random Forest  

---
