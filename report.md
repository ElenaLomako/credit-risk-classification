# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

The purpose of the analysis is to build a classification model utilizing logistic regression algirothm in order to predict high and low risk lenders. The model was trained on the hostorical data, which contains the information on loan size, interest rate, debt, borrower income, account, deragotory marks on credit. Also, the data contaons "loan_status" with a binary classsifier, where 1 is for hish risk and 0 is for low risk lenders. To check the count of each category of loan status we used "value_counts" function. The data contains 97% of low risk loans and 3% of high risk.

In our analysis we used classification algorithm. Firstly, we split the data into training and testing sets using "train_test_split". Then we created a logistic regression model with unsampled and sampled data. A logistic regression algorithm was trained on sampled (model 1)and not sampled (model 2) datasets. Then each model was validated and assest using the folowing metrics: accuracy, precision, recall, and F1 score.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
Balanced Accuracy Score: 0.9521352751368186
Accuracy: 0.9921975754449317 (the ratio of correctly predicted observations to the total number of observations)
Precision Score: 0.8600746268656716 (he ratio of correctly predicted positive observations to the total predicted positive observations)
Recall Score: 0.9092702169625246 (the ratio of correctly predicted positive observations to all predicted observations for that class)
F1 Score: 0.8839884947267498


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
Balanced Accuracy Score: 0.9941749445500477
Accuracy: 0.9942610265669332
Precision Score: 0.8542372881355932
Recall Score: 0.9940828402366864
F1 Score: 0.9188696444849589

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

Both models provide with high classification power. Random oversampling algorithm has slight improvement in classification prediction yeilding more favorable results based on 99% balanced accuracy score vs 95% with the original data. Futhermore, with random oversampling algorithm we achieved improved recall and f1 indicators of the model overall by improving these metrics for high-risk-loans to 0.99 (vs 0.91 using the original data) and 0.92 (vs 0.88 using original data) respectively. However, there is a slight decrease in the precision for high-risk loans to 0.85 (vs 0.86 using the original data), which likely is aceptable given the increase in the recall, f-1 score, and weighted avr precision. 

The overall assestment of the model definitely depends on the problem we are trying to solve. However, I believe in our case, where a bank is trying to access the creditworthiness of borrowers, missidentifying high-risk borrowes is more risky than identifying low-risk borrowers to mitigate lending risk, and as lower the result default rate on the lons the banks issues. 

While both models present impresive results, I belive the random oversampling algorithm has impoved classification prediction yeilding better results.

If you do not recommend any of the models, please justify your reasoning.
Note: There are some limitations to these models given the unbalanced nature of the data. I think it will be reasonalbe to use other classification model to test how those models will perform vs our models.