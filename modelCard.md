# Basic information

 ### Group member

 -Tang Runzhe（rtang29@gwmail.gwu.edu)

 -Ying Zhangtao (zying@gwmail.gwu.edu)

 -Zhao Xuan (xuanzhao@gwmail.gwu.edu)

### Date

Augest, 2021

### Model version

1.0

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

'credit_line_increase.csv'

### How training data division and validation data

Training data: 15000 rows and 20 columns 

Validation data: 7500 rows and 20 columns 

Testing data: 7500 rows and 20 columns

### Number of rows in training and validation data

Training data: 15000 rows and 20 columns 

Validation data: 7500 rows and 20 columns

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

### Source of test data

'credit_line_increase.csv'

### Number of rows in test data

7500

### Differences in columns between training and test data

None

### Columns used as inputs in the final model

20

### Columns used as targets in the final model

20

### Type of model

AIR

### Software used to implement the model

Jupyter Notebook

### Version of the modeling software

Version 2.1.5

### Hyperparameters or other settings of model

None

### Metrics used to evaluate final model

AUC

### Final values of the metrics for all data

1. Confusion matrix by RACE=1             actual: 1 actual: 0 predicted: 1       454       400 predicted: 0       132       488 (Hispanic) Confusion matrix by RACE=2             actual: 1 actual: 0 predicted: 1       470       379 predicted: 0       136       506 (Black) Confusion matrix by RACE=3             actual: 1 actual: 0 predicted: 1       180       894 predicted: 0        68      1147 (White) Confusion matrix by RACE=4             actual: 1 actual: 0 predicted: 1       193       835 predicted: 0        52      1166 (Asian) White proportion accepted: 0.531 Hispanic proportion accepted: 0.421 hispanic-to-white AIR: 0.79 White proportion accepted: 0.531 Black proportion accepted: 0.431 black-to-white AIR: 0.81 White proportion accepted: 0.531 Asian proportion accepted: 0.542 asian-to-white AIR: 1.02

2. Confusion matrix by SEX=1             actual: 1 actual: 0 predicted: 1       567       950 predicted: 0       158      1247 (Male) Confusion matrix by SEX=2             actual: 1 actual: 0 predicted: 1       730      1558 predicted: 0       230      2060 (Female) Male proportion accepted: 0.481 Female proportion accepted: 0.500 female-to-male AIR: 1.04
3. White proportion accepted: 0.531 Hispanic proportion accepted: 0.421 hispanic-to-white AIR: 0.79 White proportion accepted: 0.531 Black proportion accepted: 0.431 black-to-white AIR: 0.81 White proportion accepted: 0.531 Asian proportion accepted: 0.542 asian-to-white AIR: 1.02 Male proportion accepted: 0.481 Female proportion accepted: 0.500 female-to-male AIR: 1.04 

### Plots related to the data

![image-20210828173111746](/Users/zhuobinyuan/Library/Application Support/typora-user-images/image-20210828173111746.png)

![image-20210828173139981](/Users/zhuobinyuan/Library/Application Support/typora-user-images/image-20210828173139981.png)

<img src="/Users/zhuobinyuan/Library/Application Support/typora-user-images/image-20210828173039674.png" alt="image-20210828173039674" style="zoom:50%;" />

**<img src="/Users/zhuobinyuan/Library/Application Support/typora-user-images/image-20210828173232281.png" alt="image-20210828173232281" style="zoom:50%;" />**

<img src="/Users/zhuobinyuan/Library/Application Support/typora-user-images/image-20210828173317400.png" alt="image-20210828173317400" style="zoom:50%;" />

<img src="/Users/zhuobinyuan/Library/Application Support/typora-user-images/image-20210828173340552.png" alt="image-20210828173340552" style="zoom:50%;" />

### Potential negative impacts of using the model

- Outdated packages used to create the model could decrease the level of interpretability for the model.

- Variables from the data, like 'loan_to_value_ratio_std', can improve accuracy for the model and simultaneously bring bias as a result of structural inequities.
- Implementing the model without having an appeal mechanism in place for people who are not given a mortgage could result in serious financial and life consequences for those individuals.

### Potential uncertainties relating to the impacts&unexpected

- The model changes when packages used to create the model could decrease the level of interpretability for the model. 
- Legal implications of implementing the model in the real-world.
- Simulated recession conditions for the model resulting in the major drop in performance.

### conclusion
Overall, this was a great learning process to better understand the general rules and steps within interpretable machine learning models for ensuring fairness, security, and accuracy. Our group is open to constructive criticism and would like to receive any feedback as to how to improve the model presented in this model card.


