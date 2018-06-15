# Breast-Cancer-Wisconsin-Dataset-Investigation
Doing an independent project on the Breast Cancer Wisconsin Dataset

This dataset contains 569 people who have been diagnosed with either benign or malignant cancer.  30 different features have been measured about each individual's cancer.  The point of investigating the dataset is to predict whether a patient has benign or malignant cancer.

In our dataset  212  people had malignant cancer, and  357  people had benign cancer.  As such there should not be a problem with class imbalance, but for the purposes of this investigation it should be noted that approximately 63% of the patients in the dataset had benign cancer.

I had heard somewhere that logistic regression worked really well on cancer datasets and wanted to confirm it for myself.  So far the dataset only has a logistic regression model which is very accurate with the following result:

CV accuracy: 0.981 +/- 0.018

Test accuracy: 0.982

Where the training and test set have been put into an 80%/20% split respectively, which has been done randomly, and the dataset is stratified (meaning the training and test datasets have same class proportions of benign and malignant cancer).  I am using PCA for feature extraction, and am using grid search CV to determine the best hyperparameters.  The best hyperparameters for this model are a regularization parameter equal to 1, and PCA components equal to 10 (so we are reducing the number of components in the model from 30 to 10).

I will try and see if I can increase the accuracy of my predictions.

I have also added an investigation of feature importance on the data set using random forests.  This can be seen in the graph given in my uploaded files (or you can run the code).
