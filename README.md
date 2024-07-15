# Multi-Class-Classification-Challenge

Goal: Your task is to employ a multi-class approach to predict the outcomes of patients with the disease.

Evaluation: Submissions will be evaluated using multi-class logarithmic loss. Each ID in the test set corresponds to a single true class label, Status. For each ID, submit predicted probabilities for each of the three possible outcomes: Status_C, Status_CL, and Status_D.

Metric: The evaluation metric is calculated using the multi-class logarithmic loss formula:

logloss  =   −1/N ∑i=1N∑j = 1Myijlog(pij),

Where:

( N ) is the number of rows in the test set.
( M ) is the number of outcomes (3).
( y_{ij} ) is 1 if row ( i ) has the ground truth label ( j ), and 0 otherwise.
( p_{ij} ) is the predicted probability that observation ( i ) belongs to class ( j ).
The submitted probabilities for a given row are not required to sum to one because they are rescaled prior to being scored (each row is divided by the row sum). In order to avoid the extremes of the log function, predicted probabilities are replaced with max(min(p,1−10−15),10−15)
.
