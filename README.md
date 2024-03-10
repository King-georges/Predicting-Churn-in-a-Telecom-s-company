#  SyriaTel Customer Churn
### Author: George Opondi
---

## Overview
The objective of this project is to develop a robust classifier capable of predicting customer churn for SyriaTel, a telecommunications company. Customer churn prediction entails identifying customers who are likely to discontinue their services with the company in the near future. The task is framed as a binary classification problem, where the classifier will categorize customers into two groups: those expected to churn and those likely to remain.

---


## Business problem
The primary business challenge facing SyriaTel, a leading telecommunications company, lies in minimizing customer churn to ensure sustained growth and profitability. Elevated rates of customer churn pose a significant threat to revenue streams and market competitiveness. To tackle this challenge effectively, SyriaTel aims to implement proactive strategies aimed at identifying customers likely to discontinue their services and engaging them through tailored retention initiatives. By harnessing advanced analytics and predictive modeling techniques, the company seeks to develop a delicate understanding of customer behavior patterns and preferences. This understanding will empower SyriaTel to personalize retention efforts, thereby maximizing customer satisfaction and loyalty.

The objective of this project is therefore to design and deploy a robust classifier capable of accurately predicting customer churn for SyriaTel. By doing so, the company will be equipped to proactively identify customers at risk of churn and implement targeted retention strategies. These strategies will aim to minimize churn, optimize revenue streams, and foster sustainable business growth. By prioritizing customer retention, SyriaTel endeavors to cultivate enduring relationships with its clientele, fortify brand loyalty, and achieve enduring success in a competitive marketplace.
 
---

## Data Understanding

### Details on the data set

### Title: SyriaTel Customer Churn
Relevant information: This data set is used to predict customer churn based on the variables/columns available. The churn column is therefore the target variable.

In this dataset, there are 3333 unique rows and  21 independent predictive variables or column attributes.

### Sources:
 a) This data set is obtained from Kaggle
 
 b) (https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset)

### Description of columns
- _state_ : The state of the customer.
- _account length_ : The length of the account in days or months.
- _area code_ : The area code of the customer's phone number.
- _phone number_ : The phone number of the customer.
- _international plan_ : Whether the customer has an international plan or not
- _voice mail plan_ : Whether the customer has a voicemail plan or not
- _number vmail messages_ : The number of voicemail messages the customer has.
- _total day minutes_ : Total minutes of day calls.
- _total day calls_ : Total number of day calls.
- _total day charge_ : Total charge for the day calls.
- _total eve minutes_ : Total minutes of evening calls.
- _total eve calls_ : Total number of evening calls.
- _total eve charge_ : Total charge for the evening calls.
- _total night minutes_ : Total minutes of night calls.
- _total night calls_ : Total number of night calls.
- _total night charge_ :  Total charge for the night calls.
- _total intl minutes_ : Total minutes of international calls.
- _total intl calls_ : Total number of international calls.
- _total intl charge_ : Total charge for the international calls.
- _customer service calls_ : Total charge for the international calls.
- _churn_ : Whether the customer churned or not (True/False).

---

## Visualizations
![alt text](<Images/Distribution of day calls.png>)
The distribution of day calls is left-skewed because it’s longer on the left side of its peak. The long tail on its left represents the small proportion of total day calls. It is therefore negatively skewed.


![alt text](<Images/Distribution of evening calls.png>)


![alt text](<Images/Distribution of night calls.png>)


![alt text](<Images/Distribution of international calls.png>)


![alt text](<Images/Customer churn rate.png>)


![alt text](<Images/Customer service calls Distribution by Churn Status.png>)


![alt text](<Images/Total day minutes vs. Total day charges by Churn Status.png>)


![alt text](<Images/Total international minutes vs. Total international charges by Churn Status.png>)


![alt text](<Images/Total night minutes vs. Total night charges by Churn Status.png>)

![alt text](Images/Histogram.png)
