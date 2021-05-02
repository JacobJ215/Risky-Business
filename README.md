# Unit 11-Risky-Business


## Background 

This notebook uses serval machine tools and techniques to help predict credit risk using data typically seen from peer-to-peer lending services. 

Due to the fact that credit risk is inherently imbalanced, this notebooks will rely on techniques that employ imbalanced classes. 

Here we use the imbalanced-learn and Scikit-learn libraries to build and evaluate models using the two following techniques:

1. Resampling 
2. Ensemble Learning


## Resampling 

In this section we evaluate the lending_data.csv, by first creating a training set for out models and a testing set to make our predictions. We then resample these sets using four different sampling techniques. We are applying two Oversampling techniques, one Undersampling techique and one Combination Sampling technique. 

For the Oversampling techniques we are using the Naive Random Oversampling algorithim and the SMOTE algorithm.

For the Undersampling technique we are using the Cluster Centroids algorithm.

Lastly for the Combination Sampling technique we are using the SMOTEENN algorithm.

We then use each newly resampled data set to train our Logistic Regression model. 

### Analysis

After comparing the results of each model using the balanced accuracy score and imbalanced classification score it can be noted that the Logistic Regression model using the SMOTE Oversampler had the best balanced accuracy score with a score of 0.9948, both the Oversampled and Undersampled models had the same recall score of 0.99 and both the Logistic Regression model using the SMOTE Oversampler and the SMOTEENN combination sampler had best geometric mean scores with scores at 0.99.


## Ensemble Learning

In this section we trained and compare two different ensemble classifiers to predict loan risk and evaluate each model. These classifiers were namely the Balanced Random Forest Classifier and the Easy Ensemble Classifier.


### Analysis

After comparing the results of each model using the balanced accuracy score and imbalanced classification score it can be noted that the Easy Ensemble classifier had the best balanced accuracy score with a score of 0.925, the best recall score with a score of 0.94 and the best geometric mean score with a score of 0.93. 

From the Balanccned Random Rorest Classifier's importance feauters method it can be noted that the top three features are total_rec_prncp, total_rec_int, total_pymnt_inv.
