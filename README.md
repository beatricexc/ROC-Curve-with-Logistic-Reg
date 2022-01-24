# ROC-Curve-with-Logistic-Reg

The ROC curve ( Receiver Operating Characteristic Curve) is a graph showing the performance of a classification model at all classification tresholds. 

This curve plots two parameteres: 

- True Positive Rate (tpr)
- False Positive Rate (fpr)

TRUE POSITIVE RATE (TPR) is a synonym for recall and is therefore defined as follows : 
TPR = TP/(TP+FN)

FALSE POSITIVE RATE is defined as follows:
FPR = FP/(FP + TN)

AUC stands for "Area under the ROC Curve". The AUC measures the entire two-dimensional area underneath the entire ROC curve from (0,0) to (1,1)

AUC represents the probability that a random positive  example is positioned to the right of a random negative example.

AUC ranges in value from 0 to 1. A model whose predictions are 100% wrong has an AUC of 0.0; one whose predictions are 100% correct has an AUC of 1.0.

AUC is desirable for the following two reasons:

AUC is scale-invariant. It measures how well predictions are ranked, rather than their absolute values.
AUC is classification-threshold-invariant. It measures the quality of the model's predictions irrespective of what classification threshold is chosen.
However, both these reasons come with caveats, which may limit the usefulness of AUC in certain use cases:

Scale invariance is not always desirable. For example, sometimes we really do need well calibrated probability outputs, and AUC won’t tell us about that.

Classification-threshold invariance is not always desirable. In cases where there are wide disparities in the cost of false negatives vs. false positives, it may be critical to minimize one type of classification error. For example, when doing email spam detection, you likely want to prioritize minimizing false positives (even if that results in a significant increase of false negatives). AUC isn't a useful metric for this type of optimization.
