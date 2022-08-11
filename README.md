![Credit-Risk-Analysis-course](https://user-images.githubusercontent.com/103154070/184243923-00644444-a00b-4942-be0a-698450a87276.jpg)

Jill commends you for all your hard work. Piece by piece, you’ve been building up your skills in data preparation, statistical reasoning, and machine learning. You are now ready to apply machine learning to solve a real-world challenge: credit card risk.
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, you’ll need to employ different techniques to train and evaluate models with unbalanced classes. Jill asks you to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, you’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, you’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, you’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once you’re done, you’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.


## Results

### Native Random Oversampling 
![NativeRO](https://user-images.githubusercontent.com/103154070/184247946-388626c4-1595-4b5b-b90b-19449ecc69a7.png)

- Accuracy Score: 64.6%
- Precision Score: High-Risk = 1%; Low- Risk = 100%
- Recall Score(Sensitivity): High-Risk = 60.9%%; Low- Risk = 68.2%



### SMOTE oversampling 
![smote](https://user-images.githubusercontent.com/103154070/184247948-0d143e6a-3a3b-4df6-8dfd-0264b09997be.png)

- Accuracy Score: 62.3%
- Precision Score: High-Risk = 1% ; Low-Risk = 100%
- Recall Score (Sensitivity): High-Risk = 60.9%; Low-Risk = 63.8%

### Undersampling 
![under](https://user-images.githubusercontent.com/103154070/184247952-f38bd449-08ab-46ed-8e10-7f5ea7bb152c.png)

- Accuracy Score:62.3%
- Precision Score: High-Risk = 1%; Low-Risk = 100%
- Recall Score (Sensitivity): High-Risk = 60.9%; Low-Risk = 44.9%


### Combination Under/Over-Sampling 
![combo](https://user-images.githubusercontent.com/103154070/184247960-a92d9467-8119-4422-91ce-dcbd4eee8f55.png)

- Accuracy Score: 52.9%
- Precision Score: High-Risk = 1%; Low-Risk = 100%
- Recall Score (Sensitivity): High-Risk = 70.1; Low-Risk = 57.8%


### Balanced Random FOrest Classifier
![brfc](https://user-images.githubusercontent.com/103154070/184247986-129be50a-3922-4f19-9d91-d141f294a0ce.png)

- Accuracy Score: 77.3%
- Precision Score: High-Risk = 3%; Low-Risk = 100%
- Recall Score (Sensitivity): High-Risk = 66.3%; Low-Risk = 88.2%

### Easy Ensemble AdaBoost Classifier
![easy](https://user-images.githubusercontent.com/103154070/184247998-97176bb2-d9f4-4616-987d-e69a74a6469a.png)

- Accuracy Score: 91.8%
- Precision Score: High-Risk = 9%; Low-Risk = 100%
- Recall Score (Sensitivity): High-Risk = 89.4%; Low-Risk = 94.2%


## Summary
From the results above we can see that the Combination Over/Under-Sampling model produces the lowest accuracy score of 52.9% whereas the Easy Ensemble AdaBoost Classifier model provides us with the highest accuracy score of 91.8%.  The EEAC model is so high due to the huge imbalance of the dataset.  Solely based off this score, it could be assumed that this would be the best model for creditors to use, however the precision score for detecting High-Risk clients/debtors is very low at 9%.  The precision score for high-risk cliets/debtors for all six models is very low, so I would not recommend any of these models.  Without having a strong precision score, creditors run the risk of making inaccurate decisions on who should be approved for various loans.  
