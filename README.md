# cc_fraud
1)
Creditcard_fraud_sampling.ipynb


The purpose of this notebook is to experiment with different resampling technique in an imbalanced sample problem and not aimed at finding the best model to predict fraud. This will be followed up with a separate exercise.
Source of data: Kaggle dataset for credit card fraud. The file is too big to store up here, but can be found on this link:
https://www.kaggle.com/mlg-ulb/creditcardfraud

Summary of findings:

I experimented with undersampling, oversampling and custom sampling of the dataset. I aimed to find as many fraud cases as possible without significantly increasing the number of false-positive predictions. It might result in significant loss to the business if ordinary transactions are blocked. Therefore, I focused on precision scoring, however, I included accuracy scoring to provide further insight.
The best results came out with the undersampling technique, although no resampling at all also performed acceptable, in terms of not generating a high number of false positives.

2)
Creditcard_fraud_model_tuning.ipynb
This notebook contains experiments with different models, mostly tree-based models, on an undersampled train set. This is a work in progress yet.


1)
SAMPLING - details:
Logistic regression on the undersampled data found 83 out of the 98 fraud cases, and falsely predicted fraud in 51 cases only. The cross-validated precision score on the training data was 1. I found two other models (with different regularization strength) where the model resulted in the same (1) precision score but achieved a bit better result on this particular test set. They both found 80 out of 98 fraud cases but predicted fraud in only 17 or 18 other cases, where the true label was ‘regular’ (not fraud) transactions.


Please see the file "Comments_to_Creditcard_fraud_notebook.docx" for further comments.
