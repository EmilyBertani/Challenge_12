# Module 12 Report

## Overview of the Analysis

---

* The purpose of this analysis is to evaluate imbalanced data on lending activity using a logistic regression model in order to accurately predict potential fraudulent activity.

* The financial data we analyzed included the loan size and interest rate for each borrower, and along with the borrowers income, debt to income ratio, the total debt the borrower has incurred, the number of accounts the borrower has and if there are any negative marks on their debts. This will help predict likelihood of future fraudulent activity.

* With the above data, we tried to predict the value counts - how many loans were predicted to be fraudulent vs non fraudulent, as well as the accuracy, precision, recall and F1 scores of the models. These will be disucssed more in detail below.  We ran a logistic regression model first with the original data and then with resampled data using a Random OverSampler technique. We are attempting to find the model with shows the best accuracy, precision, recall and F1 score.

* In order to run the two models, first we start with the original data. We divide the data into testing and training data in order to train the model appropriately for future predictions. We do this using train_test_split. Once we have split the data as above, we run the logistic regression model and which then allows us to make predictions on fraudulent vs non fraudulent activity witn new and future data. We can determine the accuracy, precision, recall and F1 score of this data, which is described in more detail below. 

* After analyzing the original data, we then use random oversampling to reduce the imbalance between the fraudulent and non fraudulent transactions. We do this using the RandomOverSampler method which allows us to better balance the data. This is done with hopes to improve the accuracy, precision, recall and F1 scores. We then compare to two models to see which has better statistics.

* Accuracy - Accuracy measures how often the model was correct. If the model predicted a fraudulent transaction that was actually fraudulent, or if the model predicted a non fraudulent transaction that was truly not fraudulent, this leads to higher accuracy.

* Precision - Precision measures our confidence that the model correctly makes positive predictions. So for all transactions that were predicted fraudulent or non fraudulent, precision measures how many were truly fraudulent or truly non fraudulent.

* Recall - Similar to precision but slightly different, recall measures the number of true fraudulent transactions the model correctly identified as fraudulent.

* F1 score - Also known as the harmonic mean, the F1 score tells us how well we predicted the fraudulent transactions. A value closer to 1 is desired. We want to know more about how well the model predicts fraudulent transactions as opposed to non fraudulent transactions in this scenario.

* As mentioned above, we use logistic regression to train the model to predict future data. We also use the Random Oversampler method to help balance the data in hopes of more accurate and precise predictions.

---

## Results

* Machine Learning Model 1, Original Data:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
  
  ![Original Data Class Report](https://github.com/EmilyBertani/Challenge_12/blob/main/Original_data_class_report.png)
  
  * With the model run on the original data, we can see that the accuracy is excellent at 0.99. This means that 99% of the time the model accurately predicted true fraudulent and true non fraudulent transactions.
  
  * The precision for the original data was 1.00 for the non fraudulent transactions and 0.85 for the fraudulent transactions. This means that we are 100% confident that our model will truly predict a non fraudulent transaction and 85% confident the model will truly predict a fraudulent transaction.
  
  * The recall for the original data shows the recall of 0.99 for the non fraudulent transactions and 0.91 for the fraudulent transactions. This means that for all non fraudulent transactions, our model correctly identified 99% of them, and for all fraudulent transactions, our model correctly identified 91%.

* Machine Learning Model 2, Resampled Data:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  
  ![Resampled Data Class Report](https://github.com/EmilyBertani/Challenge_12/blob/main/Resampled_data_class_report.png)
  
  * With the model run on the resampled data, we can see that the accuracy is also at 0.99. So with the resampled data, 99% of the time the model accurately predicted true fraudulent and true non fraudulent transactions.
  
  * The precision for the resampled data was again 1.00 for the non fraudulent transactions and 0.84 for the fraudulent transactions. This means that we are 100% confident that our model will truly predict a non fraudulent transaction and 84% confident the model will truly predict a fraudulent transaction.
  
  * The recall for the resampled data shows again a recall of 0.99 for the non fraudulent transactions and 0.99 for the fraudulent transactions. This means that for all non fraudulent transactions, our model correctly identified 99% of them, and for all fraudulent transactions, our model correctly identified 99%.

---

## Summary


* From this analysis, we can see that there is minimal difference between the original and resampled data. However, our goal is to most accurately and precisely predict fraudulent data. Therefore I would opt for the resampled data model as the recall for the fraudulent data is almost perfect at 99% compared to 91% with the original data. Even with a precision of 84% with resampled data compared to 85% with the original data, this .01% difference is still worth using the resampled data.

* As mentioned above, it is more important to correctly predict fraudulent data compared to non fraudulent data. Therefore as above, I stand by using the resampled data as the model for fraud detection.

