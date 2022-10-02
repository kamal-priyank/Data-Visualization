Machine Learning Decision Tree  

The German Credit data is split into train and test sets with a ratio of 0.7 and the optimal tree size is found to be 3 by fitting a decision tree to the training data, which is determined by 5-fold cross validation.   

![](Aspose.Words.10897a61-cebf-49ed-aa94-8c37c135bb74.001.png)

The test error rate of the above model is found to be 0.27 with an AUC of 0.715, which is a decent score.  

2) A random forest is fit to the training data with the parameter of max number of features set to “sqrt” and the number of trees i.e n\_estimators set to 1000.  

![](Aspose.Words.10897a61-cebf-49ed-aa94-8c37c135bb74.002.png)

The test error rate of the random forest model is found to be 0.22 with and AUC of 0.789, which is great than that of the pruned tree model. A decrease in test error rate signals that the model is more accurate now.  

The above variable importance plot shows that Duration, Amount, Age and checkingAccountStatus are the most important features to predict the class.  

2) The plot below shows the ROC curves of both models. From which we can interpret that the area under the curve is more when a random forest model is used rather than a pruned tree model, a random forest model fits better with the training data.  

![](Aspose.Words.10897a61-cebf-49ed-aa94-8c37c135bb74.003.png)
