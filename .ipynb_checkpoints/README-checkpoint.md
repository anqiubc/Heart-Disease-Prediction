# Heart-Disease-Prediction

## Summary

- Used 13 features to predict if a patience has heart disease using SVM model, which achieves a CV recall of 82.7%, accuracy=82.7%, precision=82.7% and auc=89.3%. 
- Designed a function to evaluate a classification model's performance through multiple metrics on the test set, and another function to display model's performance using Cross-Validation. Compared the following classifiers: Logistic regression, Random Forest, Gradient-boosted decision trees, SVM, KNN, and MLPClassifier. 
- Considering the application purpose for potential disease detecting, selected the final model focused on the recall along with other metrics.

## Dataset
Dataset: https://www.kaggle.com/ronitf/heart-disease-uci
This database contains 76 attributes, but all published experiments refer to using a subset of 14 of them. In particular, the Cleveland database is the only one that has been used by ML researchers to this date. 

## Target
Use all the features provided to predict the presence of heart disease for individual patience, which represented by 1(has heart disease) and 0 (no heart disease). It's actually a binary classification problem. 

## Conclusion

I designed a function to evaluate a classification model's performance through multiple metrics on the test set, and another function to display model's performance using Cross-Validation. Then I compared the following classifiers: Logistic regression, Random Forest, Gradient-boosted decision trees, SVM, KNN, and MLPClassifier.   

For each kind of model, I did a grid search for choosing the parameter, then compared the performance of different kinds of models.  

As for the key metric for model selection, considering potential disease detecting purpose, I think I should care most about how many people that have heart disease(true=1) that found out to have heart disease(predict=1) by our prediction. That's **recall** for the positive class. At the same time, I focused on other performance metrics as well.    

Based this criterion, the final chosen model is SVM, which gets CV recall=0.827 for the positive class. The other metrics through 5-fold CV are also good: accuracy=0.827, auc=0.893, precision=0.827.  



