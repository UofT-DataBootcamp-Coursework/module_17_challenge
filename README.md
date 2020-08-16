# Module 17 Challenge - Supervised Machine Learning & Credit Risk

## Challenge Overview

The goals of this challenge are for you to:

- Implement machine learning models.
- Use resampling to attempt to address class imbalance.
- Evaluate the performance of machine learning models.

## Resources

Data Sources: [LoanStats_2019Q1](Module-17-Challenge-Resources/LoanStats_2019Q1.csv)

Software: Python (libraries: pandas, numpy, pathlib, collections, sklearn, and imblearn), Juptyer Notebook

## Analysis

### Naive Random Sampling

**Balanced Accuracy Score =** 0.65

**Classification Report**

![](images/nro.PNG)

**Precision Score =** 0.01

**Recall Score =** 0.69

### SMOTE Oversampling

**Balanced Accuracy Score =** 0.66

**Classification Report**

![](images/SMOTE.PNG)

**Precision Score =** 0.01

**Recall Score =** 0.63

### Undersampling

**Balanced Accuracy Score =** 0.66

**Classification Report**

![](images/under.PNG)

**Precision Score =** 0.01

**Recall Score =** 0.68

### Combination Sampling

**Balanced Accuracy Score =** 0.55

**Classification Report**

![](images/combo.PNG)

**Precision Score =** 0.01

**Recall Score =** 0.72

### Conclusion

All four models produced the same extremely low precision scores of 0.01, implying that all four models were not precise in identifying potentially high risk customers (way too many false positives were identified)

The combination over-and-under sampling model produced the highest recall score of 0.72, while the other three were between 0.66 and 0.68. A recall score of 0.72 implies that approximately 72% of high risk customers were identified by the model, which for the purposes of assess credit risk, seems a bit low considering the rammifications of more than 25% of customers defaulting on their loan repayments.

The combination over-and-under sampling model produced the lowest balanced accuracy score of 0.55, while the other three were between 0.65 and 0.66. In general, all four did not produce a sufficiently high accuracy score. 

With credit ratings, it is important for a model to strike a balance between precision and recall, with a bit more empahsis on its ability to be more precise than it is to be more sensitive. When attempting to forecast who is at a higher risk, it is better to have the predicted high risk customers that are more likely to be truely high risk customers identified rather than cast a larger net and capture an abundance of false positives (assuming there are no additional screening measures used to verify the results of the model). With the latter, if you incorrectly classify a potential customer as high risk when they are not, you would be jeopardizing the loan agreement as the customer may determine they are not high risk and would take their business elsewhere. 

I would not recommend any of the four tested models as each one produced an extremely low precision score, the highest recall score was only 0.72 implying over a quarter of those who would be considered high risk are not identified, and all their respective balanced accuracy scores where not sufficiently high enough. 

## Report completed by:

![](images/sal.jpg)
