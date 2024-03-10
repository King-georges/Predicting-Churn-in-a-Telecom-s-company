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

The distribution of evening calls is also left-skewed because it’s longer on the left side of its peak. The long tail on its left represents the small proportion of total day calls. It is therefore negatively skewed.


![alt text](<Images/Distribution of night calls.png>)

The distribution of night calls is approximately symmetrical, with the observations distributed similarly on the left and right sides of its peak. Therefore, the distribution has approximately zero skew


![alt text](<Images/Distribution of international calls.png>)

The distribution of international calls is right-skewed because it’s longer on the right side of its peak. The long tail on its right represents the small proportion of total international calls. It is therefore positively skewed.


![alt text](<Images/Customer churn rate.png>)

The current customer churn rate for SyriaTel is at 14.5%


![alt text](<Images/Customer service calls Distribution by Churn Status.png>)

The box for churned customers is slightly higher than the box for non-churned customers, which means that churned customers tend to make more customer service calls than non-churned customers. The median for churned customers is also higher than the median for non-churned customers. There are also more outliers for churned customers than non-churned customers, which means that there are a few churned customers who made a very high number of customer service calls. Overall, the box plot suggests that there is a positive relationship between the number of customer service calls a customer makes and their churn status. Customers who make more customer service calls are more likely to churn.


![alt text](<Images/Total day minutes vs. Total day charges by Churn Status.png>)

The scatter plot shows that, for both churned and non-churned customers, as the total number of minutes spent on calls increases, the total cost of those calls also increases. This is because customers are typically charged per minute for their calls.

However, the slope of the line is steeper for churned customers than for non-churned customers. This suggests that churned customers tend to have a higher total charge per minute than non-churned customers. In other words, churned customers may be on plans with higher rates, or they may simply make more expensive calls (e.g., international calls).


![alt text](<Images/Total international minutes vs. Total international charges by Churn Status.png>)

Overall, the scatter plot suggests that there may be a relationship between total international minutes, total international charges, and churn status. Customers who spend more minutes on international calls and who have a higher total charge for those calls may be more likely to churn, especially if they are on plans with high international calling rates.


![alt text](<Images/Total night minutes vs. Total night charges by Churn Status.png>)

Overall, the scatter plot suggests that there may be a relationship between total night minutes, total night charges, and churn status. Customers who talk for a longer total time at night and who have a higher total charge for their calls may be more likely to churn.


# Modelling

## Baseline model using Logistic regression

Instantiate the basline model using logistic regression and the following were the results:

![alt text](<Images/confusion matrix for baseline model.png>)

## Baseline model classification metrics

Baseline Accuracy:** 0.8635

**Baseline Precision:** 0.9729

**Baseline Recall:** 0.8803

**Baseline F1-score:** 0.9243



**Baseline Accuracy:** Accuracy is a measure of the overall correctness of the model's predictions. It calculates the ratio of correct predictions (both true positives and true negatives) to the total number of predictions. In this context, the baseline accuracy of 0.8635 means that the baseline model correctly predicts approximately 86.35% of the cases in the dataset.

**Baseline Precision:** Precision measures the proportion of true positive predictions among all positive predictions made by the model. It is calculated as the ratio of true positives to the sum of true positives and false positives. In this case, the baseline precision of 0.9729 indicates that when the baseline model predicts a customer will churn, it is correct about 97.29% of the time.

**Baseline Recall:** Recall, also known as sensitivity, measures the proportion of true positive predictions among all actual positive instances in the dataset. It is calculated as the ratio of true positives to the sum of true positives and false negatives. The baseline recall of 0.8803 means that the baseline model identifies approximately 88.03% of the actual churn cases correctly.

**Baseline F1-score:** F1-score is the harmonic mean of precision and recall. It provides a balanced measure of a model's performance, especially when dealing with imbalanced datasets. The baseline F1-score of 0.9243 indicates the overall effectiveness of the baseline model in correctly identifying positive cases while minimizing false positives and false negatives.


## Training and Evaluating other classification Models

**K-Nearest Neighbors:** 0.9130434782608695

**Support Vector Machines:** 0.9355322338830585

**Decision Trees:** 0.9355322338830585

**Random Forests:** 0.9475262368815592

The Random Forest model performed the best on the  dataset, achieving the highest accuracy on the testing set. This suggests that the Random Forest model was able to learn the patterns in the training data and generalize well to unseen data in the testing set.  **Random Forest:** Achieved an accuracy of 0.9475, indicating it correctly classified nearly 95% of the instances in the testing set.  **Logistic Regression:** Achieved an accuracy of 0.8561, which is considerably lower than the Random Forest model. Therefore, there is need of applying hyperparameter tuning to improve it's accuracy on prediction.


## Random forest tuned Model  evaluation

![alt text](<Images/Confusion matrix for tuned random forest.png>)

**Accuracy:** 0.9505

**Precision:** 0.9359

**Recall:** 0.7228

**F1-score:** 0.8156


## Comparison with the baseline logistic regression model

**Baseline Accuracy:** 0.8635,  **Random Forest Tuned Accuracy:** 0.9535

**Baseline Precision:** 0.9729, **Random Forest Tuned Precision:** 0.9375

**Baseline Recall:** 0.8803, **Random Forest Tuned Recall:** 0.7426

**Baseline F1-score:** 0.9243, **Random Forest Tuned F1-score:** 0.8287


In evaluating the performance of the predictive models, there is an observation of notable improvements with the tuned Random Forest model compared to the baseline:

**Baseline Accuracy:** 86.35%

**Random Forest Tuned Accuracy:** 95.35%

**Baseline Precision:** 97.29%

**Random Forest Tuned Precision:** 93.75%

**Baseline Recall:** 88.03%

**Random Forest Tuned Recall:** 74.26%

Baseline F1-score:** 92.43%

**Random Forest Tuned F1-score:** 82.87%

These metrics demonstrate the effectiveness of the efforts in optimizing the Random Forest model. Despite the baseline model's respectable performance, the tuned Random Forest model showcases significant enhancements across all evaluation criteria. This improvement indicates the potential for the tuned Random Forest model to better predict customer churn, thereby enabling more proactive and targeted retention strategies.

## Recommendations 

1. **Customer Service Call Handling:**

> Since churned customers tend to make more customer service calls than non-churned customers, improving the quality and efficiency of customer service interactions is crucial.

> Focus on resolving customer issues promptly and satisfactorily to minimize the need for repeated calls.
Implement proactive customer outreach programs to address potential issues before they escalate.

2. **Plan and Pricing Optimization:**

> Analyze the relationship between total call charges and churn status to identify customers on plans with high rates or those making expensive calls.

> Consider offering tailored plans with competitive pricing and features that align with customer usage patterns, especially for international calls.

> Provide transparent pricing information and flexible options to meet diverse customer needs.

3. **Retention Strategies:**

> Leverage predictive modeling techniques to identify customers at risk of churn based on behavioral patterns and preferences.

> Develop targeted retention initiatives tailored to the needs of high-risk customers, such as personalized offers, discounts, or loyalty rewards.

> Implement proactive communication strategies to engage customers and reinforce the value proposition of SyriaTel's services.

4. **Feature Importance Insights:**

> Utilize the insights from RFECV feature selection to prioritize key features for churn prediction.

> Pay special attention to features like number of voicemail messages, total call minutes, and international calling plans, which have been identified as significant predictors of churn.

5. **Continuous Monitoring and Improvement:**

> Regularly monitor churn rates and customer feedback to assess the effectiveness of retention initiatives.

> Continuously refine predictive models and strategies based on evolving customer behaviors and market dynamics.

By implementing these recommendations, SyriaTel can enhance its efforts to reduce churn, improve customer satisfaction, and foster long-term relationships with its clientele.

