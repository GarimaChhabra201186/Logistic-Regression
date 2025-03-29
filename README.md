# Logistic-Regression
Logistic Regression concept and Hands on notebook

Recall that Accuracy is given by:
Accuracy=True Positives+True Negatives/Total Number of Predictions

It gives equal importance to both false positives and false negatives. However, this may not be the case in most business problems. Accuracy is preferred in cases where the cost of predicting false positives and false negatives is roughly the same. For example, suppose you want to predict an image whether it is a cat or not. In this case, both the cost of false positives and the cost of false negatives do not exceed one another, and you will not be charged any penalty or additional costs if any kind of misclassification occurs in this case.

Precision is given by:

Precision=TruePositives/TruePositives+FalsePositives

Precision is preferred in cases where the cost of false positives is much higher than that of false negatives. For example, suppose you are trying to predict whether an email is spam or ham. If an email is classified as spam, then it will be moved into the trash folder; this is the case of a false positive. On the other hand, in case of false negatives, the spam email stays in the inbox. So, the potential problem, in this case, is that an email that was incorrectly classified as spam would have contained some important information, and the cost of missing that information is much higher than having a spam email in your inbox.

Recall is given by:

Recall=TruePositives/TruePositives+FalseNegatives

A Recall is preferred in cases where the cost of false negatives is higher than that of false positives. For example, suppose you are trying to predict whether a person has Covid-19 or not. If an actual Covid-19 positive patient is predicted negative, and this is the case of false-negative for which the cost is quite high as they are a potential carrier of the virus, then whoever comes in contact with the patient would get infected.

In cases where both the precision and the recall need to be optimised, the F1 score would be the best option. It is calculated as the harmonic mean of both the precision and the recall.
 
The F1 score is given by:

F−measure=2×Precision×RecallPrecision+Recall
 
In some cases, there will be a trade-off between the precision and the recall. In such cases, the F-measure will drop. It will be high when both the precision and the recall are high. 

Depending on the business case at hand and the goal of data analysis, you need to select an appropriate metric. In our case, the task is to identify the minority class really well which is the case of actual positives. You need to track how many times the minority class is being predicted correctly. In this case, a recall would be the most appropriate metric to use because the actual positives are quite few in number. So, the true test is whether or not the model is able to capture these actual positive cases correctly.


