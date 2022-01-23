<p align="center">
  <img width="1000" src="https://user-images.githubusercontent.com/88597956/150657232-960eef57-7c25-4131-8fef-9444367f63d3.png">
</p>

# Overview
Assist LendingClub utilize machine learning to help predict credit risk. Build several machine learning models, oversampling, undersampling and a combined sampling approach, and evaluate the models to determine which of the models performs the best. 

## Results
Before creating the models, the dataset was clean by dropping null columns and row, removing the loan status of issued, converting the interest rates to a numerical value, and we converted the loan status column (target column) to low_risk and high_risk. From there we split the data in to training and testing, evaluated the balance of the target values. As you can see in the image the below it is unbalanced as the number of good loans outnumbers the risky loans, thus creating the need to employ different techniques to train and evaluate models with unbalanced classes. Below are the output results for each of the six models completed on the cleaned credit risk dataset.

![Loan_Status](https://user-images.githubusercontent.com/88597956/150690750-ce317db5-e156-4335-9fa2-b909d4a6c4f5.png)

**Native Random Oversampling**
- A balanced accuracy score of 64.6%, meaning 35.4% of classes are incorrectly classified.
- The high_risk loans had a precision score of 1% and a recall score of 71%
- the low_risk loans had a precision score of 100%, and a recall score of 58%

![Native_Random_Oversampling](https://user-images.githubusercontent.com/88597956/150690067-13de9d74-7a4b-404c-9685-349f8e35057b.png)

**SMOTE Oversampling**
- A balanced accuracy score of 65.9%, meaning 34.1% of classes are incorrectly classified.
- The high_risk loans had a precision score of 1% and a recall score of 63%
- the low_risk loans had a precision score of 100%, and a recall score of 68%

![SMOTE_Oversampling](https://user-images.githubusercontent.com/88597956/150690074-a49d7767-ca8b-4746-b3e8-19fae9739483.png)


**ClusterCentroids (undersampling)**
- A balanced accuracy score of 66.6%, meaning, meaning 33.4% of classes are incorrectly classified.
- The high_risk loans had a precision score of 1% and a recall score of 73%
- the low_risk loans had a precision score of 100%, and a recall score of 60%



![Undersampling](https://user-images.githubusercontent.com/88597956/150690076-d2619a74-a221-48cc-8a93-de60b41ba01c.png)


**SMOTEENN Sampling (combination)**
- A balanced accuracy score of 60.2%, meaning 39.8% of classes are incorrectly classified.
- The high_risk loans had a precision score of 1% and a recall score of 68%
- the low_risk loans had a precision score of 100%, and a recall score of 52%

![Combination](https://user-images.githubusercontent.com/88597956/150690086-e1cda843-57d9-4e92-b25e-fc1e83ceb55a.png)

**Balanced Random Forest Classifier**
- A balanced accuracy score of 78.9%, meaning 21.1% of classes are incorrectly classified.
- The high_risk loans had a precision score of 3% and a recall score of 70%
- the low_risk loans had a precision score of 100% and a recall score of 87%

![Balanced_Random_Forest_Classifer](https://user-images.githubusercontent.com/88597956/150690090-279c524f-078f-4e2c-b6db-c7d04a9f5bb6.png)

**Easy Ensemble AdaBoost Classifier**
- A balanced accuracy score of 93.2%, meaning 6.8% of classes are incorrectly classified.
- The high_risk loans had a precision score of 9% and a recall score of 92%
- the low_risk loans had a precision score of 100%, and a recall score of 94%

![Easy_Ensemble](https://user-images.githubusercontent.com/88597956/150690093-a7171207-0d2b-4987-9168-2af594c8d689.png)


## Summary

In looking at the above results, it is easy to see that the Easy Ensemble AdaBoost Classifier was the best performing model of the 6 with the best accuracy score of the six models tested at 93.2%. Not only did it have a high accuracy score but it also had high precision, recall and specificity scores. The high specificity score means that it accurately determined 94% of the high_risk loans, which is exactly what we would prefer in this situation. The oversampling, undersampling and combination sampling models results were all nearly identical, predicting a minimum of 33% of classed incorrectly.  The Balanced Random Forest Classifier accuracy was higher than the previous models but still inaccurately classified 21.1% of classes. 
