# Credit_Risk_Analysis

## Overview of the loan prediction risk analysis:


## The purpose of this analysis is:

The purpose for this analysis is to create the best model for predicting credit risk using multuple features. We are going to test using a few different models. After fine tuning those models we will pick the most accurate model to recommend. 

#### Models tested:

    * RandomOverSampler
    * SMOTE
    * CentroidClustering
    * SMOTEENN
    * BalancedRandomForestClassifier
    * EasyEnsembleClassifier 



## Results:

### Random Oversampling:
![Rand](https://github.com/austink24/Credit_Risk_Analysis/blob/main/Random_overSampling.png)

##### - balanced accuracy score - 66.5% of the time this model correctly predicted the fraudulant transaction however, it still missed 27 times out of 88 to identify a fraudulent transactions. 

##### - precision- when reviewing the results for Precision score we can see that a vary large number of transactions were predicted or flagged as fruadulent when they actaully weren't. 


##### - recall scores - This models sensitivity/recal score shows that it doesn't prededict all the fraudulent transactions very well, improperly predicting almost 1/3 of the fraudulent transactions as not being fraudulent.



### SMOTE:
![SMOTE](https://github.com/austink24/Credit_Risk_Analysis/blob/main/SMOTE.png)

##### - balanced accuracy score - the accuracy score of this model only slightly improves upon the previous model RandomOverSampling with 67% vs 66.5%.


##### - precision - it's precision score still predicted a very large number of non-fraudulent transactions to be fraudulent, actaully predicting ever more FP's than the previous model.

##### - recall scores - only a slight improvement of sensitivity score over the RandomOverSampling model with 63 out of 88 TP, versus 61 out 88 TP with RandomOverSampling.


### CentroidClustering:
![Cluster](https://github.com/austink24/Credit_Risk_Analysis/blob/main/Cluster_centroid.png)

##### - balanced accuracy score - there wasn't any improvement using Undersampling and ClusterCentroids model on accuracy score. 

##### - precision - there also no noticable improvement with the prescision score as it still predicted a large number of FPs.

##### - recall scores - for the sensitivity score it did show an improvement on prediciting TN  but performed worse when it cam to predicting FN with that number increasing.

### SMOTEENN
![Smoteenn](https://github.com/austink24/Credit_Risk_Analysis/blob/main/SMOOTENN.png)

##### - balanced accuracy score - the balanced scoore of SMOTEENN actaully dropped off at 60% when compared to the previous three models.

##### - precision - as with previous models SMOOTEEN still predicts a large number of False Positives the most of any model evaluated up to this point with 7343 FPs.

##### - recall scores - there has been an improvement over previous models as far as recall score with this model where out of 88 fraudualent transactions this model correctly predicted 73 of them and only missed 15. Which still needs to be improved but better than previous.


#### BalancedRandomForestClassifier
![Blanced](https://github.com/austink24/Credit_Risk_Analysis/blob/main/balanced_random.png)

##### - balanced accuracy score - the balanced accuracy score of this model is the highest yet with 79.1%.

##### - precision - we see that this model also does better with correctly predicting FP while only improperly predicting 1706 as fraudulent when they weren't but slips drastically when it comes to corretly identifying fraudulent tranaactions as seen by the increas in FN. 

##### - recall scores - with this model the recall score is actually performing worse as it missed 28 fruadulent transactions by predicting them to be non-fraudulent.


### EasyEnsembleClassifier 
![Easy](https://github.com/austink24/Credit_Risk_Analysis/blob/main/AdAboost.png)

##### - balanced accuracy score - this model performed best out of all the models tested with an accuracy score of 92.6%.

##### - precision -  it also had the lowest FP predictions.

##### - recall scores - for its sensitivty score this model far out performed the rest by only having 8 FN out of 88 fraudulent transactions.



## Summary:
In summary I would not recommend any of these models. I would suggest either adding more data to these models to improve accuracy or continue to search for a model that will minimize the FN even further. With Fraudulent transactions being so costly these days it would be wise to continue refining models to reduce FN.

Out of all the models tested the EasyEnsembleClassifier was by far the best performing model and with no other options it would be the best model to use. Correctly predicting 80 out 88 fraudulent transactions and only predicting 1358 FP out of 17117 non-fraudulent which isn't ideal but a vast improvement on other moedels.

