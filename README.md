# Credit_Risk_Analysis

## Overview of the Analysis
The purpose of this analysis is to utilize and review several machine learning models to help us best predict credit risk. 

## Results
- RandomOverSampler model:
  - ![ROS](https://github.com/typicalchazz/Credit_Risk_Analysis/blob/main/Images/RandomOverSampler.png)
  
  - The accuracy test shows a 64% accuracy score.
  - The precision for high_risk is only about 1%, with a sensitivity of 66% and an F1 of 2%
  - The precision for low risk is 100%, with a sensitivity of 62%

- SMOTE model:
  - ![S](https://github.com/typicalchazz/Credit_Risk_Analysis/blob/main/Images/SMOTE.png)
  
  - The accuracy test shows a 65.1% accuracy score.
  - The precision for high_risk is only about 1%, with a sensitivity of 61% and an F1 of 2%
  - The precision for low risk is 100%, with a sensitivity of 69%

- ClusterCentroids model:
  - ![CC](https://github.com/typicalchazz/Credit_Risk_Analysis/blob/main/Images/ClusterCentroids.png)
  
  - The accuracy test shows a 65.1% accuracy score.
  - The precision for high_risk is only about 1%, with a sensitivity of 69% and an F1 of 1%
  - The precision for low risk is 100%, with a sensitivity of 40%

- SMOTEENN model:
  - ![SS](https://github.com/typicalchazz/Credit_Risk_Analysis/blob/main/Images/SMOTEENN.png)
  
  - The accuracy test shows a 54.4% accuracy score.
  - The precision for high_risk is only about 1%, with a sensitivity of 72% and an F1 of 2%
  - The precision for low risk is 100%, with a sensitivity of 57%

- BalancedRandomForestClassifier model:
  - ![BRFC](https://github.com/typicalchazz/Credit_Risk_Analysis/blob/main/Images/BRFC.png)
  
  - The accuracy test shows a 76.5% accuracy score.
  - The precision for high_risk is only about 3%, with a sensitivity of 65% and an F1 of 6%
  - The precision for low risk is 100%, with a sensitivity of 88%

- EasyEnsembleClassifier
  - ![EEC](https://github.com/typicalchazz/Credit_Risk_Analysis/blob/main/Images/EEC.png)

  - The accuracy test shows a 93.2% accuracy score.
  - The precision for high_risk is only about 9%, with a sensitivity of 92% and an F1 of 16%
  - The precision for low risk is 100%, with a sensitivity of 94%


## Summary
All of the models used had weak precision. the 1st 4 models (RandomOverSampler, SMOTE, ClusterCentroids, and SMOTEENN) utilized over/under/combination sampling, while the last 2 (BalancedRandomForestClassifier and EasyEnsembleClassifier) were Ensemble models. The Ensemble models were more promising than the sampling models, with the EasyEnsembleClassifier being the strongest, with a high balanced accuracy score, relatively high high_risk precision, and the highest F1 score out of all models. If I had to pick a model to utilize, I would recommend the EasyEnsembleClassifier model, but in reality I believe all models don't suffice. The EasyEnsembleClassifier may detect a large portion of high risk credit, but with its precision being so low, it is still falsely detecting low risk credits as high risk.