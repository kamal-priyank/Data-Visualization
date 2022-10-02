Machine Learning Individual Coursework  

Question 1:  

1) The German Credit data is split into train and test sets with a ratio of 0.7 and the optimal tree size is found to be 3 by fitting a decision tree to the training data, which is determined by 5-fold cross validation.   

![](Aspose.Words.10897a61-cebf-49ed-aa94-8c37c135bb74.001.png)

The test error rate of the above model is found to be 0.27 with an AUC of 0.715, which is a decent score.  

2) A random forest is fit to the training data with the parameter of max number of features set to “sqrt” and the number of trees i.e n\_estimators set to 1000.  

![](Aspose.Words.10897a61-cebf-49ed-aa94-8c37c135bb74.002.png)

The test error rate of the random forest model is found to be 0.22 with and AUC of 0.789, which is great than that of the pruned tree model. A decrease in test error rate signals that the model is more accurate now.  

The above variable importance plot shows that Duration, Amount, Age and checkingAccountStatus are the most important features to predict the class.  

2) The plot below shows the ROC curves of both models. From which we can interpret that the area under the curve is more when a random forest model is used rather than a pruned tree model, a random forest model fits better with the training data.  

![](Aspose.Words.10897a61-cebf-49ed-aa94-8c37c135bb74.003.png)

Question 2:  (1)  

![](Aspose.Words.10897a61-cebf-49ed-aa94-8c37c135bb74.004.jpeg)

3) The data set is split into a training set of 50% and a test set of 50% and the support vector machine is trained with a linear kernel, a polynomial kernel and an RBF or a Radial kernel on the training data with all the parameters tuned by 5-fold cross validation.  

![](Aspose.Words.10897a61-cebf-49ed-aa94-8c37c135bb74.005.jpeg)

The above svm classification plot with linear kernel shows that there is highly inaccurate i.e the accuracy is found to be 42.66, which means more than half of the datapoints were incorrectly classified.  

![](Aspose.Words.10897a61-cebf-49ed-aa94-8c37c135bb74.006.jpeg)

The above svm classification plot with a polynomial kernel also shows high error rate but better than the linear model.  

![](Aspose.Words.10897a61-cebf-49ed-aa94-8c37c135bb74.007.jpeg)

The above svm classification plot with a Radial kernel also a high error rate with an accuracy of 46.66.  

The Radial or RBF kernel model is found to be a better fit and gives best results for the above simulated 3-class dataset.  

Question 3:  

1) The recorded 10 test values of KNN and LDA in two vectors are:  

![](Aspose.Words.10897a61-cebf-49ed-aa94-8c37c135bb74.008.png)

![](Aspose.Words.10897a61-cebf-49ed-aa94-8c37c135bb74.009.png)

The k value of 3 is found to be the best estimator while tuning the parameters of the KNN model by 5-fold cross validation.  

2) The plot below shows two boxplots of AUC values of LDA and KNN respectively.  

![](Aspose.Words.10897a61-cebf-49ed-aa94-8c37c135bb74.010.png)

From the boxplots shown above we can conclude that the KNN model is a better fit for the newthyroid.txt data because it has higher median AUC values when compared to the linear discriminant analysis (LDA)model  

Question 4:  

A user defined function for the generation of training indexes is defined with inputs as a vector y, K as the value for K-fold cross validation and a seed as an integer, the output obtained are the training sets and the function is applied to the German credit dataset with 10fold cross validation to generate corresponding training indexes.  

We get a list of indexes for the input list of y vector and  randomly shuffle it using the shuffle() function, the list of y is split into K number chunks as we need a K-fold cross validation and then one by one selecting one chunk to test set and join other nine chunks to the train set.  
6  
