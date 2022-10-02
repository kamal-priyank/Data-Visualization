## Decision Tree & Random Forest on GermanCredit Dataset

The German Credit data is split into train and test sets with a ratio of 0.7 and the optimal tree size is found to be 3 by fitting a decision tree to the training data, which is determined by 5-fold cross validation.   

<p align="center">
<img width="523" alt="Screenshot 2022-10-02 at 21 41 14" src="https://user-images.githubusercontent.com/66077662/193475352-2679a832-4bc0-466d-a33d-2492214cf5e8.png">

</p>
<h5 align="center">Pruned Decision tree</h5>

The test error rate of the above model is found to be 0.27 with an AUC of 0.715, which is a decent score.  

A random forest is fit to the training data with the parameter of max number of features set to “sqrt” and the number of trees i.e n\_estimators set to 1000.  

<p align="center">
<img width="753" alt="Screenshot 2022-10-02 at 21 41 42" src="https://user-images.githubusercontent.com/66077662/193475363-c61e5047-03ba-4b8e-b1f5-319c74430898.png">

</p>
<h5 align="center">Random Forest</h5>

The test error rate of the random forest model is found to be 0.22 with and AUC of 0.789, which is great than that of the pruned tree model. A decrease in test error rate signals that the model is more accurate now.  

The above variable importance plot shows that Duration, Amount, Age and checkingAccountStatus are the most important features to predict the class.  

The plot below shows the ROC curves of both models. From which we can interpret that the area under the curve is more when a random forest model is used rather than a pruned tree model, a random forest model fits better with the training data.  

<p align="center">
<img width="798" alt="Screenshot 2022-10-02 at 21 42 00" src="https://user-images.githubusercontent.com/66077662/193475382-62ecc211-6405-4370-9805-19447304eb0c.png">

</p>
<h5 align="center">ROC Curve Comparision</h5>
