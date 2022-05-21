# Spam-Mail-Detection
Building models for detection of spam messages based on various email characteristics.

Dataset: http://archive.ics.uci.edu/ml/datasets/Spambase

This dataset has 4601 records where each record represents a different email message. Each record is described with 58 attributes out of which 57 attributes represent various content based characteristics already extracted from each email message (related to the frequency of certain words, punctuation symbols, usage of capital letters in a message). The last attribute represents the class label for each message (spam or non-spam).

I considered the following algorithms to build a cost-sensitive model with a 10:1 cost ratio for different misclassification errors:
1. Decision Tree, KNN, Logistic Regression, Support Vector Machine 
2. Ensemble Models - Gradient Boosting, Random Forest 
3. Neural Network  – 3 input layers with ReLU activation

Misclassifying a non-spam mail as a spam mail is more costly than classifying a spam mail as non-spam. Hence, predicting Class 0 (Non-Spam) as Class 1 (Spam) has a cost of 10x compared to predicting Class 1 as Class 0 has a cost of 1x.

Best Performing Model: Random Forest (Accuracy – 0.946)

Lowest average misclassification cost is at about 0.7 threshold.

