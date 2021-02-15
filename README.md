# Credit_Risk_Analysis

## Overview of the loan prediction risk analysis:


## The purpose of this analysis is:

The purpose for this analysis is to create the best model for predicting credit risk using multuple features. We are going to test using a few different models. After fine tuning those models we will pick the most accurate model to recommend. 

#### Models tested:

    * RandomOverSampler
    * SMOTE
    * ClusterCentroids
    * SMOTEENN
    * BalancedRandomForestClassifier
    * EasyEnsembleClassifier 



## Results:

### Random Oversampling:
![Rand](https://github.com/austink24/Credit_Risk_Analysis/blob/main/Random_overSampling.png)

##### - balanced accuracy score

##### - precision

##### - recall scores 


### SMOTE:
![SMOTE](https://github.com/austink24/Credit_Risk_Analysis/blob/main/SMOTE.png)

##### - balanced accuracy score

##### - precision

##### - recall scores 


### ClusterCentroids:
![Cluster](https://github.com/austink24/Credit_Risk_Analysis/blob/main/Cluster_centroid.png)

##### - balanced accuracy score

##### - precision

##### - recall scores 


### SMOTEENN
![Smoteenn](https://github.com/austink24/Credit_Risk_Analysis/blob/main/SMOOTENN.png)

##### - balanced accuracy score

##### - precision

##### - recall scores 

#### BalancedRandomForestClassifier
![Blanced](https://github.com/austink24/Credit_Risk_Analysis/blob/main/balanced_random.png)
##### - balanced accuracy score

##### - precision

##### - recall scores 


### EasyEnsembleClassifier 
![Easy](https://github.com/austink24/Credit_Risk_Analysis/blob/main/AdAboost.png)
##### - balanced accuracy score

##### -precision

##### -recall scores 


Let's go over the results in the classification report:

Precision: Precision is the measure of how reliable a positive classification is. From our results, the precision for the good loan applications can be determined by the ratio TP/(TP + FP), which is 50/(50 + 22) = 0.69. The precision for the bad loan applications can be determined as follows: 19/(19 + 34) = 0.358. A low precision is indicative of a large number of false positives—of the 53 loan applications we predicted to be bad applications, 34 were actually good loan applications.
Recall: Recall is the ability of the classifier to find all the positive samples. It can be determined by the ratio: TP/(TP + FN), or 50/(50 + 34) = 0.595 for the good loans and 19/(19 + 22) = 0.463 for the bad loans. A low recall is indicative of a large number of false negatives.
F1 score: F1 score is a weighted average of the true positive rate (recall) and precision, where the best score is 1.0 and the worst is 0.0.
Support: Support is the number of actual occurrences of the class in the specified dataset. For our results, there are 84 actual occurrences for the good loans and 41 actual occurrences for bad loans.
In summary, this model may not be the best one for preventing fraudulent loan applications because the model's accuracy, 0.552, is low, and the precision and recall are not good enough to state that the model will be good at classifying fraudulent loan applications. Modeling is an iterative process: you may need more data, more cleaning, another model parameter, or a different model. It's also important to have a goal that's been agreed upon, so that you know when the model is good enough.


        

There is a bulleted list that describes the balanced accuracy score and the precision and recall scores of all six machine learning models (15 pt)
Summary:

There is a summary of the results (2 pt)
There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)
