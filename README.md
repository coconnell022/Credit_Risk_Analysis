# Credit_Risk_Analysis

## Overview of the Analysis

The purpose of this project was to apply machine learning to solve credit card risk using a dataset from LendingClub, a peer-to-peer lending services company. The main objective is to use different machine learning techniques to train and evaluate models with unbalanced classes using imbalanced-learn and scikit-learn libraries and resampling. The data was first oversampled using the RandomOverSampler and SMOTE algorithms, then undersampled using the CLusterCentroids algorithm and a combination approach of oversampling and undersampling using the SMOTEENN algorithm. Then two additional models, BalancedRandomForestClassifier and EasyEnsembleClassifier were used to predict credit risk. After all six models were created, they were all evaluated on performance to decide if they should be used to classify credit risk for individuals as "high risk" or "low risk".

    Resources
        - Data Sources: LoanStats_2019Q1.csv
        - Software: Python (imbalanced-learn & scikit-learn), Jupyter Notebook

## Results

Below are the results of the six different machine learning models used in this project. For each machine learning model evaluated, the balanced accuracy score, precision score, and recall score are listed. The balanced accuracy score of each model represents how often the classifier is correct with the model. The precision score is a measure of how reliable a positive classification is. The recall score is the ability of the classifier to find all the positive samples.

**1. Naive Random Oversampling**

   - Balanced accuracy score: 0.65
    
   ![alt text](https://github.com/coconnell022/Credit_Risk_Analysis/blob/main/Images/Naive%20Random%20Oversampling_BAS.png?raw=true)

   - Precision and recall scores: 0.99 and 0.55 averages respectively
    
   ![alt text](https://github.com/coconnell022/Credit_Risk_Analysis/blob/main/Images/Naive%20Random%20Oversampling_ICR.png?raw=true)
    
**2. SMOTE Oversampling**

   - Balanced accuracy score: 0.66
    
   ![alt text](https://github.com/coconnell022/Credit_Risk_Analysis/blob/main/Images/SMOTE%20Oversampling_BAS.png?raw=true)

   - Precision and recall scores: 0.99 and 0.69 averages respectively
    
   ![alt text](https://github.com/coconnell022/Credit_Risk_Analysis/blob/main/Images/SMOTE%20Oversampling_ICR.png?raw=true)

**3. ClusterCentroids Undersampling**

   - Balanced accuracy score: 0.55
    
   ![alt text](https://github.com/coconnell022/Credit_Risk_Analysis/blob/main/Images/ClusterCentroids%20Undersampling_BAS.png?raw=true)

   - Precision and recall scores: 0.99 and 0.41 averages respectively
    
   ![alt text](https://github.com/coconnell022/Credit_Risk_Analysis/blob/main/Images/ClusterCentroids%20Undersampling_ICR.png?raw=true)

**4. SMOTEENN Combination**

   - Balanced accuracy score: 0.66 
    
   ![alt text](https://github.com/coconnell022/Credit_Risk_Analysis/blob/main/Images/SMOTEENN%20Combination_BAS.png?raw=true)

   - Precision and recall scores: 0.99 and 0.61 averages respectively
    
   ![alt text](https://github.com/coconnell022/Credit_Risk_Analysis/blob/main/Images/SMOTEENN%20Combination_ICR.png?raw=true)

**5. Balanced Random Forest Classifier**

   - Balanced accuracy score: 0.79
    
   ![alt text](https://github.com/coconnell022/Credit_Risk_Analysis/blob/main/Images/Balanced%20Random%20Forest%20Classifier_BAS.png?raw=true)

   - Precision and recall scores: 0.99 and 0.87 averages respectively
    
   ![alt text](https://github.com/coconnell022/Credit_Risk_Analysis/blob/main/Images/Balanced%20Random%20Forest%20Classifier_ICR.png?raw=true)

**6. Easy Ensemble AdaBoost Classifier**

   - Balanced accuracy score: 0.93
    
   ![alt text](https://github.com/coconnell022/Credit_Risk_Analysis/blob/main/Images/Easy%20Ensemble%20AdaBoost%20Classifier_BAS.png?raw=true)

   - Precision and recall scores: 0.99 and 0.94 averages respectively
    
   ![alt text](https://github.com/coconnell022/Credit_Risk_Analysis/blob/main/Images/Easy%20Ensemble%20AdaBoost%20Classifier_ICR.png?raw=true)

## Summary

In summary, out of the six machine learning models evaluated the **recommended machine learning model is the Easy Ensemble AdaBoost Classifier**. An ideal machine learning model would have a high balanced accuracy score, a high precision score, and a high recall score. **The Easy Ensemble AdaBoost Classifier had the highest balanced accuracy score at 0.93, the highest average precision score at 0.99, and the highest average recall score at 0.94**. One of the main reasons that the Easy Ensemble Classifier has the highest overall performance is due to the fact that this model combines multiple models and the final prediction is based on the accumulated predictions from each algorithm while also reducing the variance of the model. The AdaBoost component of this model also provides additional accuracy by weighing the errors of previous models to minimize similar errors in subsequent models. The one negative drawback of using these models is that although the averages for precision and recall are high, the high_risk prediction precision scores are significantly lower than the low_risk prediction precision scores which could potentially cause errors in the overall accuracy in the assessment of credit card risk.


        Caroline O'Connell
        February 7th, 2021

