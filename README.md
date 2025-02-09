**Titanic Survival Prediction**
===============================

**Overview**
------------

This project applies machine learning techniques to predict passenger survival on the Titanic. The dataset, sourced from **Kaggle** (provided by *Khashayar Baghizadeh Hosseini*), consists of **891 rows** and **12 columns**, containing information on **passenger demographics, ticket details, and survival status**. The analysis involves data cleaning, visualization, and model training to evaluate classification performance.

**Data Cleaning**
-----------------

-   **Handling Missing Values**:
    -   **Age**: Mean imputation
    -   **Embarked**: Mode imputation
    -   **Cabin**: Missing values explicitly marked
-   **Feature Encoding**:
    -   Converted categorical features (*Sex*, *Embarked*) into numeric values using **label encoding**.
-   **Feature Engineering**:
    -   Created a **FamilySize** feature by combining *SibSp* and *Parch*.
-   **Data Normalization**:
    -   Scaled *Fare* using **StandardScaler** to improve model performance.

**Data Visualization**
----------------------

### **1\. Survival Rate by Passenger Class**

A bar plot illustrating survival rates across different ticket classes.

🔹 *First-class passengers had the highest survival rate, followed by second-class, with third-class having the lowest survival rate.*

### **2\. Age Distribution of Survived vs. Not Survived**

A histogram comparing age distributions of passengers who survived versus those who did not.

🔹 *Younger passengers had a higher likelihood of survival compared to older passengers.*

**Machine Learning Models**
---------------------------

The following classifiers were used:

1.  **Logistic Regression** -- A linear model for binary classification. *(max_iter=200 for convergence)*
2.  **K-Nearest Neighbors (KNN)** -- Classifies based on the k-nearest neighbors.
3.  **Decision Tree** -- Splits data based on feature values to form a predictive tree.

### **Model Performance (5-Fold Cross-Validation)**

| Model | Mean Accuracy | Standard Deviation |
| --- | --- | --- |
| Logistic Regression | 0.833 | 0.012 |
| K-Nearest Neighbors | 0.844 | 0.014 |
| Decision Tree | 0.833 | 0.017 |

🔹 *KNN achieved the highest accuracy and lowest standard deviation, making it the most consistent model in this setup.*

**Analysis & Future Improvements**
----------------------------------

-   **KNN outperformed Logistic Regression & Decision Tree** in accuracy and consistency.
-   Further improvements could include:
    -   **Outlier detection & removal**
    -   **Hyperparameter tuning (e.g., adjusting k for KNN)**
    -   **Feature selection and dimensionality reduction**

**Conclusion**
--------------

This project demonstrates the importance of **feature engineering, data preprocessing, and model selection** in real-world datasets. By applying machine learning techniques, we successfully predicted survival probabilities and analyzed key survival factors. Future work could explore ensemble methods or deep learning models for enhanced predictions.
