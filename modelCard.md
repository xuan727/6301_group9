# Basic information

 ### Group member

 -Tang Runzhe（rtang29@gwmail.gwu.edu)

 -Ying Zhangtao (zying@gwmail.gwu.edu)

 -Zhao Xuan (xuanzhao@gwmail.gwu.edu)

### Date

08/27/2021

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

- Name
Index(['ID', 'LIMIT_BAL', 'SEX', 'RACE', 'EDUCATION', 'MARRIAGE', 'AGE',
       'PAY_0', 'PAY_2', 'PAY_3', 'PAY_4', 'PAY_5', 'PAY_6', 'BILL_AMT1',
       'BILL_AMT2', 'BILL_AMT3', 'BILL_AMT4', 'BILL_AMT5', 'BILL_AMT6',
       'PAY_AMT1', 'PAY_AMT2', 'PAY_AMT3', 'PAY_AMT4', 'PAY_AMT5', 'PAY_AMT6',
       'DELINQ_NEXT'],
      dtype='object')
- Modeling role
['ID', 'LIMIT_BAL', 'SEX', 'RACE', 'EDUCATION', 'MARRIAGE', 'AGE',
       'PAY_0', 'PAY_2', 'PAY_3', 'PAY_4', 'PAY_5', 'PAY_6', 'BILL_AMT1',
       'BILL_AMT2', 'BILL_AMT3', 'BILL_AMT4', 'BILL_AMT5', 'BILL_AMT6',
       'PAY_AMT1', 'PAY_AMT2', 'PAY_AMT3', 'PAY_AMT4', 'PAY_AMT5', 'PAY_AMT6',
       'DELINQ_NEXT']
- Measurement level
AUC 0.7373
- Description
	ID	LIMIT_BAL	SEX	RACE	EDUCATION	MARRIAGE	AGE	PAY_0	PAY_2	PAY_3	PAY_4	PAY_5	PAY_6	BILL_AMT1	BILL_AMT2	BILL_AMT3	BILL_AMT4	BILL_AMT5	BILL_AMT6	PAY_AMT1	PAY_AMT2	PAY_AMT3	PAY_AMT4	PAY_AMT5	PAY_AMT6	DELINQ_NEXT
count	30000.000000	30000.000000	30000.000000	30000.000000	30000.000000	30000.000000	30000.000000	30000.000000	30000.000000	30000.000000	30000.000000	30000.000000	30000.000000	30000.000000	30000.000000	3.000000e+04	30000.000000	30000.000000	30000.000000	30000.000000	3.000000e+04	30000.00000	30000.000000	30000.000000	30000.000000	30000.000000
mean	15000.500000	167484.322667	1.603733	2.721967	1.853133	1.551867	35.485500	-0.016700	-0.133767	-0.166200	-0.220667	-0.266200	-0.291100	51223.330900	49179.075167	4.701315e+04	43262.948967	40311.400967	38871.760400	5663.580500	5.921163e+03	5225.68150	4826.076867	4799.387633	5215.502567	0.221200
std	8660.398374	129747.661567	0.489129	1.094397	0.790349	0.521970	9.217904	1.123802	1.197186	1.196868	1.169139	1.133187	1.149988	73635.860576	71173.768783	6.934939e+04	64332.856134	60797.155770	59554.107537	16563.280354	2.304087e+04	17606.96147	15666.159744	15278.305679	17777.465775	0.415062
min	1.000000	10000.000000	1.000000	1.000000	0.000000	0.000000	21.000000	-2.000000	-2.000000	-2.000000	-2.000000	-2.000000	-2.000000	-165580.000000	-69777.000000	-1.572640e+05	-170000.000000	-81334.000000	-339603.000000	0.000000	0.000000e+00	0.00000	0.000000	0.000000	0.000000	0.000000
25%	7500.750000	50000.000000	1.000000	2.000000	1.000000	1.000000	28.000000	-1.000000	-1.000000	-1.000000	-1.000000	-1.000000	-1.000000	3558.750000	2984.750000	2.666250e+03	2326.750000	1763.000000	1256.000000	1000.000000	8.330000e+02	390.00000	296.000000	252.500000	117.750000	0.000000
50%	15000.500000	140000.000000	2.000000	3.000000	2.000000	2.000000	34.000000	0.000000	0.000000	0.000000	0.000000	0.000000	0.000000	22381.500000	21200.000000	2.008850e+04	19052.000000	18104.500000	17071.000000	2100.000000	2.009000e+03	1800.00000	1500.000000	1500.000000	1500.000000	0.000000
75%	22500.250000	240000.000000	2.000000	4.000000	2.000000	2.000000	41.000000	0.000000	0.000000	0.000000	0.000000	0.000000	0.000000	67091.000000	64006.250000	6.016475e+04	54506.000000	50190.500000	49198.250000	5006.000000	5.000000e+03	4505.00000	4013.250000	4031.500000	4000.000000	0.000000
max	30000.000000	1000000.000000	2.000000	4.000000	6.000000	3.000000	79.000000	8.000000	8.000000	8.000000	8.000000	8.000000	8.000000	964511.000000	983931.000000	1.664089e+06	891586.000000	927171.000000	961664.000000	873552.000000	1.684259e+06	896040.00000	621000.000000	426529.000000	528666.000000	1.000000

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

training & testing

Air

AUC

### Software used to implement the model

Jupyter Notebook

### Version of the modeling software

Version 2.1.5

### Hyperparameters or other settings of model

None

### Metrics used to evaluate final model

Decision Tree

confusion metrics

Cutoff

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


