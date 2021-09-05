# Group_9_ModelCard

# Basic information

### Group Member names and emails
 -Tang Runzhe（rtang29@gwmail.gwu.edu)

 -Ying Zhangtao (zying@gwmail.gwu.edu)

 -Zhao Xuan (xuanzhao@gwmail.gwu.edu)

### Date

Augest, 2021

### Model version

1.0

### Software used to implement the model

Jupyter Notebook/Colaboratory

### Version of the modeling software

Version 2.1.5

### license

Apache 2.0 License, Copyright (c) 2021, Tang Runzhe, Ying Zhangtao & Zhao Xuan.

### Model implementation code

https://colab.research.google.com/github/xuan727/6301_group9/blob/main/6301_group_9.ipynb

### Intended Use

- Intended uses: This model is an "example" probability of default classifier, with an "example" use case for determining eligibility for a credit line increase.
- Intended users: Students in GWU DNSC 6301 bootcamp
- Out-of-scope uses: Any use beyond an educational example

# Training data

### Source of training data
GWU Blackboard email 'rtang29@gwmail.gwu.edu','zying@gwmail.gwu.edu', or'xuanzhao@gwmail.gwu.edu' for more information

### How training data division and validation data

- Training data: 15000 rows and 20 columns 

- Validation data: 7500 rows and 20 columns 

- Testing data: 7500 rows and 20 columns

### Data dictionary

| Name | Modeling Role | Measurement Level| Description|
| ---- | ------------- | ---------------- | ---------- |
|**ID**| ID | int | unique row indentifier |
| **LIMIT_BAL** | input | float | amount of previously awarded credit |
| **SEX** | demographic information | int | 1 = male; 2 = female
| **RACE** | demographic information | int | 1 = hispanic; 2 = black; 3 = white; 4 = asian |
| **EDUCATION** | demographic information | int | 1 = graduate school; 2 = university; 3 = high school; 4 = others |
| **MARRIAGE** | demographic information | int | 1 = married; 2 = single; 3 = others |
| **AGE** | demographic information | int | age in years |
| **PAY_0, PAY_2 - PAY_6** | inputs | int | history of past payment; PAY_0 = the repayment status in September, 2005; PAY_2 = the repayment status in August, 2005; ...; PAY_6 = the repayment status in April, 2005. The measurement scale for the repayment status is: -1 = pay duly; 1 = payment delay for one month; 2 = payment delay for two months; ...; 8 = payment delay for eight months; 9 = payment delay for nine months and above |
| **BILL_AMT1 - BILL_AMT6** | inputs | float | amount of bill statement; BILL_AMNT1 = amount of bill statement in September, 2005; BILL_AMT2 = amount of bill statement in August, 2005; ...; BILL_AMT6 = amount of bill statement in April, 2005 |
| **PAY_AMT1 - PAY_AMT6** | inputs | float | amount of previous payment; PAY_AMT1 = amount paid in September, 2005; PAY_AMT2 = amount paid in August, 2005; ...; PAY_AMT6 = amount paid in April, 2005 |
| **DELINQ_NEXT**| target | int | whether a customer's next payment is delinquent (late), 1 = late; 0 = on-time |

# Test data

- Source of test data: GWU Blackboard, email 'rtang29@gwmail.gwu.edu','zying@gwmail.gwu.edu', or'xuanzhao@gwmail.gwu.edu' for more information
- Number of rows in test data: 7500 rows
- State any differences in columns between training and test data: None

### Number of rows in training and validation data

Training data: 15000 rows and 20 columns 

Validation data: 7500 rows and 20 columns

# Model details

Columns used as inputs in the final model: 'LIMIT_BAL','PAY_0','PAY_4','PAY_5','PAY_6','BILL_AMT1','BILL_AMT2','BILL_AMT'3,'BILL_AMT4','BILL_AMT5','BILL_AMT6','PAY_AMT1','PAY_AMT2','PAY_AMT3','PAY_AMT4','PAY_AMT5','PAY_AMT6'
Column used as target in the final model:'DELINQ_NEXT'
Type of model:DECISION TREE
Software used to implement the model:Python3, scikit-learn
Version of the modeling software:Python 3.7.11, scikit-learn 0.22.2.post1

### Final values of the metrics for all data

1. Confusion matrix by RACE=1             actual: 1 actual: 0 predicted: 1       454       400 predicted: 0       132       488 (Hispanic) Confusion matrix by RACE=2             actual: 1 actual: 0 predicted: 1       470       379 predicted: 0       136       506 (Black) Confusion matrix by RACE=3             actual: 1 actual: 0 predicted: 1       180       894 predicted: 0        68      1147 (White) Confusion matrix by RACE=4             actual: 1 actual: 0 predicted: 1       193       835 predicted: 0        52      1166 (Asian) White proportion accepted: 0.531 Hispanic proportion accepted: 0.421 hispanic-to-white AIR: 0.79 White proportion accepted: 0.531 Black proportion accepted: 0.431 black-to-white AIR: 0.81 White proportion accepted: 0.531 Asian proportion accepted: 0.542 asian-to-white AIR: 1.02

2. Confusion matrix by SEX=1             actual: 1 actual: 0 predicted: 1       567       950 predicted: 0       158      1247 (Male) Confusion matrix by SEX=2             actual: 1 actual: 0 predicted: 1       730      1558 predicted: 0       230      2060 (Female) Male proportion accepted: 0.481 Female proportion accepted: 0.500 female-to-male AIR: 1.04
3. White proportion accepted: 0.531 Hispanic proportion accepted: 0.421 hispanic-to-white AIR: 0.79 White proportion accepted: 0.531 Black proportion accepted: 0.431 black-to-white AIR: 0.81 White proportion accepted: 0.531 Asian proportion accepted: 0.542 asian-to-white AIR: 1.02 Male proportion accepted: 0.481 Female proportion accepted: 0.500 female-to-male AIR: 1.04 

### Plots related to the data

![image](https://user-images.githubusercontent.com/89608926/132131387-9dd1c38d-c94f-4249-b9f2-01de472ff4a1.png)

![image](https://user-images.githubusercontent.com/89608926/132131404-bec76b29-84de-4a5d-a01c-5d02dd7a2869.png)

![image](https://user-images.githubusercontent.com/89608926/132131408-11927831-6960-4d4b-b681-2a25db53d702.png)

![image](https://user-images.githubusercontent.com/89608926/132131433-78cfb591-5d3c-491f-ad96-4dd3faf461e1.png)

![image](https://user-images.githubusercontent.com/89608926/132131446-540d4af4-ea9b-471e-92e5-9bec130df32c.png)

![image](https://user-images.githubusercontent.com/89608926/132131456-09669153-571d-46b2-bcc8-fcad3b3fee95.png)

# Quantitative analysis

Metrics used to evaluate your final model: To determine an ideal depth of six for the final model by using the trainning; validation AUC and AIR
Final values of the mtrics for all data:
- Training AUC: 0.78
- Validation AUC:0.75
- Test AUC:0.74
- Hispanic-to-White AIR:0.83
- Female-to-Male AIR:1.02
- Black-to-White AIR: 0.85
- Asian-to-White AIR:1.00

# Ethical considerations

### Potential negative impacts of using the model

- Outdated packages used to create the model could decrease the level of interpretability for the model.

- Variables from the data, like 'loan_to_value_ratio_std', can improve accuracy for the model and simultaneously bring bias as a result of structural inequities.
- Implementing the model without having an appeal mechanism in place for people who are not given a mortgage could result in serious financial and life consequences for those individuals.

### Potential uncertainties relating to the impacts&unexpected

- The model changes when packages used to create the model could decrease the level of interpretability for the model. 
- Legal implications of implementing the model in the real-world.
- Simulated recession conditions for the model resulting in the major drop in performance.

### Conclusion
Overall, this was a great learning process to better understand the general rules and steps within interpretable machine learning models for ensuring fairness, security, and accuracy. The implicit bias may still exist in the data even though we mitigated the explicit bias by using non-demographic data in the model. When Black-to-White AIR and Hispanic-to-White AIR are above 0.80, the result may turn out a risk to their reputation; meanwhile, the outcome of AIR was improved when the cutoff is at 0.18.

