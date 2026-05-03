# ICU Mortality Prediction (Data Science Project)

A data-driven project for analyzing and predicting ICU mortality risk using clinical data.  
This work combines exploratory data analysis, feature engineering, and machine learning to identify high-risk patients and support clinical decision-making.

---

## Overview

In intensive care units (ICUs), early identification of high-risk patients is critical.  
Traditional scoring systems like APACHE and SOFA provide useful indicators but may not capture complex relationships in patient data.

This project applies a **data science pipeline** to:
- Analyze patient data
- Identify key mortality risk factors
- Build a predictive model for early risk detection

---

## Objectives

- Analyze ICU patient data to uncover mortality patterns  
- Handle class imbalance in real-world healthcare data  
- Identify the most important clinical predictors  
- Develop an interpretable and recall-focused prediction model  
- Support data-driven clinical decision-making  

---

## Dataset

- **15,000 ICU patient records**
- **24 clinical features → reduced to 7 key predictors**
- Target:  
  - `0 = Survived`  
  - `1 = Died`

### Key Features:
- Ventilation required  
- Vasopressor use  
- Sepsis flag  
- APACHE score  
- SOFA score  
- Comorbidity score  
- Age  

The dataset is **imbalanced**:
- Survived: 11,582  
- Died: 3,418  

---

## Methodology

The project follows a structured data science workflow:

1. **Data Preparation**
   - Cleaning, preprocessing, removing irrelevant features  

2. **Exploratory Data Analysis (EDA)**
   - Class distribution  
   - Feature relationships  
   - Clinical pattern discovery  

3. **Feature Engineering**
   - Reduced features from 24 → 7  
   - Selected based on statistical and clinical relevance  

4. **Data Splitting & Balancing**
   - Train/test split (80/20)  
   - Random undersampling (training set only)  

5. **Model Development**
   - Logistic Regression  
   - Decision Tree  
   - Random Forest  
   - SVM  
   - KNN  
   - Naive Bayes  
   - Gradient Boosting  
   - XGBoost  

6. **Optimization**
   - Threshold tuning (0.35)  
   - Focus on improving recall  

7. **Evaluation**
   - Accuracy, Precision, Recall, F1-score, ROC-AUC  
   - Confusion Matrix  

---

## Key Results

- **Best Model:** Tuned XGBoost  
- **Recall:** 88.45% ✅  
- **F1-score:** 67.83%  
- **ROC-AUC:** 0.64  

The model prioritizes **recall**, ensuring high-risk patients are correctly identified.

---

## Key Insights

- Mortality strongly correlates with:
  - Ventilation requirement  
  - Vasopressor use  
  - Sepsis  
  - Severity scores (APACHE, SOFA)  

- Mortality risk increases with age  
- Severe class imbalance impacts model behavior  
- Clinical features are more influential than demographic ones  

---

## Visualizations

### Class Distribution
![Class Distribution](images/Class_Distribution.png)

### Feature Importance
![Feature Importance](images/feature_importance.png)

### Confusion Matrix
![Confusion Matrix](images/confusion_matrix.png)

---

## Prototype Demo

[Watch Demo Video](https://drive.google.com/your-link)

---

## Project Files

- Notebook: `notebook/ICU_Mortality_Model.ipynb`  
- Paper: `paper/report.pdf`  
- Poster: `poster/poster.png`  
- Dataset: `data/ICU_Patient_Monitoring_Mortality.csv`  

---

## Limitations

- Moderate ROC-AUC performance (~0.64)  
- Sensitive to noisy clinical data  
- Based on a single dataset  
- No time-series patient data included  

---

## Future Work

- Incorporate time-series ICU data  
- Use larger and more diverse datasets  
- Explore advanced imbalance handling techniques  
- Improve model robustness and generalization  

---

## Authors

- Mashael Saeed  
- Sarah Elshiathy  
- Seifeldin Elshiathy  

---

## Acknowledgements

This project is based on publicly available ICU datasets and builds upon prior research in healthcare analytics and machine learning.

---

## License

This project is for academic and educational purposes.
