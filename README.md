# Berkeley-Profession-Certificate-in-ML---Assignment-3
### Comparing Classifiers
The following notebook was used to generate this report:
https://github.com/jheberer/Berkeley-Profession-Certificate-in-ML---Assignment-3/blob/main/classifiers.ipynb

## Problem Statement
Individuals have become numb to the bombardment of marketing campaigns. The above analysis gives some context for our particular situation: Only 11% of individuals in the marketing dataset accept the term deposit offer.
The objective of our analys is to create a model that can predict which clients accept the deposit, so that we know we are investing marketing funds in targeting the correct clients, and therefore receiving a better ROI on our marketing spend.

## Process
Once again a CRISP-DM framework was used for this analysis. As we have reviewed this several times, I will not repeat it here.

A classification model is called for given the the nature of the business problem-- we are predicting whether a client falls in one of two categories: Subscribes for a term deposit, or does not subscribe.

The nature of the data made this analysis difficult, as it contained a lot of non-numeric data that required reworking. 

Once data was prepared, we trimmed down the number of columns to focus on simple demographic data:
 - age
 - type of job
 - education
 - credit default
 - housing loan
 - personal loan

After finalizing data preparations, we ran a series of four models on the data. Without getting into technical detail, these models are:
 - logistic regression
 - k nearest neighbors
 - svc
 - decision trees

## Results
The logistic regression and SVM models performed best--both exceeded baseline, albeit marginally.
![image](https://github.com/jheberer/Berkeley-Profession-Certificate-in-ML---Assignment-3/assets/7217117/1f4e4c75-a99e-4ea5-bbbf-b032c868985a)


After selecting these as the champion models, we attempted to optimize their performance. In both cases we were unsuccessful, possibly due to the imbalanced nature of the data (many more no's than yes's), and possibly due to ovefitting.
Follow-up is recommended.
In terms of features that made the likelihood of subscription higher:
1. more education
2. retired, or currently a student
3. educated from university
4. single

Those that had a deleterious effect:
1. blue collar job
2. divorced
3. lower educational attainment

## Business Recommendations
The model should be implemented immediately. The bank should target students and highly educated individuals, with an emphasis on single individuals.

## Next Steps
Get more useful data. This can be done by resampling existing population, or adding weights to the positive class.
