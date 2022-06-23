# Credit_Risk_Analysis

## Analysis Overview

In this project, we use Python to build and evaluate several machine learning models to predict credit risk.

We adopted the following procedure:

* oversample the data using the RandomOverSampler and SMOTE algorithms.
* Undersample the data using the ClusterCentroids algorithm.
* Use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm.
* Compare two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier.
* We will evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk.

### Resources

Data Source: LoanStats_2019Q1.csv
Software: Python, Anaconda Navigator, Conda, Jupyter Notebook.

## Results (Balanced Accuracy Scores, Confusion Matrixes and Imbalanced Classification Reports)

* Naive Random Oversampling results: Our balanced accuracy test it 64.5%, the precision for the high_risk has a very low positivity at 1% and the recall is 64%
<img width="535" alt="image" src="https://user-images.githubusercontent.com/94248676/174723664-fcc4d3a1-e6fa-46b9-94d8-c4e5c4cb9c99.png">

* SMOTE oversampling results: the accuracy score is 62.3%, the precision for the high_risk loans has a low positvity again at 1% and recall is 64% overall
<img width="538" alt="image" src="https://user-images.githubusercontent.com/94248676/174724066-21850f7c-dd41-4397-a68b-a1f0e5d3a4be.png">

* Undersampling results: balanced accuracy score is 51.6% overall, the precision is at 99% and the recall is 44%
<img width="532" alt="image" src="https://user-images.githubusercontent.com/94248676/174724238-4553f927-f1f4-4319-ad92-fc5bce71c03d.png">


* Combination(over and undersampling) results: balanced accuracy score is 61.5% the precision is 99% and the recall is 54% overall
<img width="536" alt="image" src="https://user-images.githubusercontent.com/94248676/174724309-512a285b-5ac4-4859-8e4e-aa152497ebaf.png">

* Balanced Random Forest Classifier results: the accuracy score is 78.7% the precision is 99% and the recall is 91%
<img width="536" alt="image" src="https://user-images.githubusercontent.com/94248676/175208648-cbd7c4a7-dd4e-4341-a41c-9826ff1f7293.png">

* Easy Ensemble AdaBoost Classifier results: the accuracy score is 92.5% the precision is 99% and the recall is 94%
<img width="536" alt="image" src="https://user-images.githubusercontent.com/94248676/175208782-d36970ea-6f68-4410-974a-5d7efe56e6ea.png">


## Summary

All the models used to perform the credit risk analysis show weak precision in determining if a credit risk is high.
The Ensemble models brought a lot more improvment specially on the sensitivity of the high risk credits.
The EasyEnsembleClassifier model shows a recall of 92% so it detects almost all high risk credit. On another hand, with a low precision, a lot of low risk credits are still falsely detected as high risk which would penalize the bank's credit strategy and infer on its revenue by missing those business opportunities.
For those reasons I would not recommend the bank to use any of these models to predict credit risk.
