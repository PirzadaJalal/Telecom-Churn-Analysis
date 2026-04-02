# Telecom Customer Churn Analysis & Prediction
Customer churn is a critical challenge in the telecom industry impacting revenue and growth. This project develops a machine learning solution to predict churn and provides actionable insights through a Power BI dashboard to improve customer retention.

<img width="1208" height="759" alt="dashboard-overview" src="https://github.com/user-attachments/assets/e96e990a-72af-4540-9508-7e2f86b2d2a7" />
<img width="1211" height="761" alt="dashboard-churn drivers" src="https://github.com/user-attachments/assets/2ea184ad-deae-406e-a2d4-8b90f9f1b9e2" />

## Objective
Analyze customer churn and predict at-risk customers using machine learning and visualize insights using Power BI.

## Machine Learning Approach

### Model Selection
Multiple machine learning algorithms were applied to evaluate performance and identify the best model for churn prediction:

Logistic Regression  
Random Forest Classifier  
XGBoost Classifier  
K-Nearest Neighbors (KNN)  
Support Vector Machine (SVM)  
Gradient Boosting Classifier  
AdaBoost Classifier  
Extra Trees Classifier  
LightGBM Classifier  
<img width="742" height="573" alt="Screenshot (197)" src="https://github.com/user-attachments/assets/c89e02b6-da0f-4716-8ee3-c419c3b4f54e" />


### Data Preparation

Categorical variables were encoded using Label Encoding  
Target variable (`Churn`) was converted into binary format (0 = No, 1 = Yes)  
Irrelevant features such as `customerID` were removed  
Dataset was split into training and testing sets (80/20 split with stratification)  

### Handling Class Imbalance

Applied **SMOTE (Synthetic Minority Oversampling Technique)** on training data  
Ensured balanced representation of churn and non-churn classes  

### Model Evaluation
Each model was evaluated using:

Accuracy  
Recall (Primary focus)  
Confusion Matrix  
Classification Report (Precision, Recall, F1-score)  

The evaluation emphasized **Recall**, as correctly identifying churn customers is critical for business retention strategies.

### Model Optimization

Performed **Hyperparameter Tuning** using GridSearchCV  
Optimized **AdaBoost Classifier** based on recall score  
Selected the best-performing model based on ability to detect churn cases

### Final Model

Tuned AdaBoost model used as final model  
Achieved significant improvement in recall (~0.88)  
Prioritized identifying high-risk customers over minimizing false positives  

### Feature Importance Analysis

Applied Random Forest to extract feature importance  
Identified key drivers of churn:
1. Monthly Charges  
2. Contract Type  
3. Tenure  
4. Total Charges  
5. Online Security  
6. Tech Support

<img width="1039" height="553" alt="important_features" src="https://github.com/user-attachments/assets/f92b91a3-5697-4f90-8037-ff0212ec20e4" />

### Conclusion

The machine learning pipeline successfully identified high-risk churn customers and key behavioral drivers. The approach demonstrates a balance between predictive performance and business applicability, enabling data-driven retention strategies.

## Key Insights
 Customers with **high monthly charges** are more likely to churn  
 **Short tenure customers** show higher churn rate  
 **Month-to-month contracts** have the highest churn  
 Lack of **Tech Support & Online Security** increases churn  

## Tools & Technologies

### Programming & Libraries
Python (Pandas, NumPy)  
Scikit-learn (Modeling, Evaluation, Preprocessing)  
XGBoost & LightGBM (Advanced Boosting Models)  
Imbalanced-learn (SMOTE for class imbalance)  

### Data Visualization
Matplotlib  
Seaborn  

### Business Intelligence
Microsoft Power BI (Dashboard & Data Visualization)
