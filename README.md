# Module 12 Report Template

## Overview of the Analysis

---

* The purpose of this analysis is to evaluate imbalanced data on lending activity using a logistic regression model in order to accurately predict potential fraudulent activity.

* The financial data we analyzed included the loan size and interest rate for each borrower, and along with the borrowers income, debt to income ratio, the total debt the borrower has incurred, the number of accounts the borrower has and if there are any negative marks on their debts. This will help predict likelihood of future fraudulent activity.

* With the above data, we tried to predict the value counts - how many loans were predicted to be fraudulent vs non fraudulent, as well as the accuracy, precision, recall and F1 scores of the models. These will be disucssed more in detail below.  We ran a logistic regression model first with the original data and then with resampled data using a Random OverSampler technique. We are attempting to find the model with shows the best accuracy, precision, recall and F1 score.

* In order to run the two models, first we start with the original data. We divide the data into testing and training data in order to train the model appropriately for future predictions. We do this using train_test_split. Once we have split the data as above, we run the logistic regression model and which then allows us to make predictions on fraudulent vs non fraudulent activity witn new and future data. We can determine the accuracy, precision, recall and F1 score of this data, which is described in more detail below. 

* After analyzing the original data, we then use random oversampling to reduce the imbalance between the fraudulent and non fraudulent transactions. We do this using the RandomOverSampler method which allows us to better balance the data. This is done with hopes to improve the accuracy, precision, recall and F1 scores. We then compare to two models to see which has better statistics.

* Accuracy - Accuracy measures how often the model was correct. If the model predicted a fraudulent transaction that was actually fraudulent, or if the model predicted a non fraudulent transaction that was truly not fraudulent, this leads to higher accuracy.

* Precision - Precision measures our confidence that the model correctly makes positive predictions. So for all transactions that were predicted fraudulent, precision measures how many were truly fraudulent.

* Recall - Similar to precision but slightly different, recall measures the number of true fraudulent transactions the model correctly identified as fraudulent.

* F1 score - Also known as the harmonic mean, the F1 score tells us how well we predicted the fraudulent transactions. A value closer to 1 is desired. We want to know more about how well the model predicts fraudulent transactions as opposed to non fraudulent transactions in this scenario.

* As mentioned above, we use logistic regression to train the model to predict future data. We also use the Random Oversampler method to help balance the data in hopes of more accurate and precise predictions.

---

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1, Original Data:
  * Description of Model 1 Accuracy, Precision, and Recall scores.



* Machine Learning Model 2, Resampled Data:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
