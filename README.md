# PROBLEM STATEMENT:  

An E Commerce company provider is facing a lot of competition in the current market and it has become a 
challenge to retain the existing customers in the current situation. Hence, the company wants to develop a 
model through which they can do churn prediction of the accounts and provide segmented offers to the 
potential churners. In this company, account churn is a major thing because 1 account can have multiple 
customers. hence by losing one account the company might be losing more than one customer. You have 
been assigned to develop a churn prediction model for this company and provide business recommendations 
on the campaign.

# NEED OF THE PROJECT: 
This study is vital for the client to gain a deeper understanding of the customer lifecycle, uncover churn 
patterns, and pinpoint the key drivers behind customer attrition. With these insights, the company can make 
data-driven decisions to proactively retain similar customer profiles in the future. 
Given that each account may serve multiple customers, losing a single account could result in the loss of 
several users—making churn prevention even more critical. 
By identifying the factors that contribute to churn early, the company can design strategic retention 
initiatives before the customer disengages completely. 

# UNDERSTANDING BUSINESS OPPORTUNITY: 
This e-commerce company operates on a model where users create individual profiles to make purchases 
online. The platform is widely appreciated for its round-the-clock accessibility and global reach—customers 
can shop at any time and have products delivered from virtually anywhere. 
Notably, a single account may be used by multiple individuals for separate transactions. For instance, if 
Person A has an account, Person B may use it to make purchases, highlighting a flexible and shared user 
experience. The core objective of the business is to simplify the shopping journey, allowing customers to 
complete purchases quickly and conveniently, without spending long hours as they might in a physical store. 
Given this structure, retaining every customer who enrolls on the platform becomes crucial. Each active 
account represents ongoing potential revenue, as customers are likely to continue engaging and transacting 
over time.


# MODEL BUILDING: 
Our churn prediction models are trained on two distinct datasets: 
Actual Data: The original dataset with natural class imbalance 
Oversampled Data: A balanced version created using SMOTE to enhance the model’s ability to detect 
churn cases 

# MODEL CAN MAKE WRONG PREDICTIONS AS: 
False Positive: The model predicts the customer will churn, but in reality, customer does not.  
False Negative: The model predicts the customer will not churn, but in reality, customer does.  
We aim to maximize recall, ensuring the model effectively identifies customers at risk of churn. This 
approach prioritizes capturing true churn cases, even if it results in a few false alarms, enabling timely 
and targeted retention efforts 


# PARAMETRIC MODELS: 
• Logistic Regression: Assumes the data has a linear pattern, features aren’t too closely related 
(no multicollinearity), and sometimes expects errors to follow a normal distribution. 
• Naive Bayes: Assumes all features are independent from each other once the class label is 
known. 
• Linear Discriminant Analysis (LDA): Assumes that each class generates data based on a 
Gaussian distribution with a shared covariance matrix. It seeks linear combinations of features 
that best separate the classes by maximizing the ratio of between-class variance to within-class 
variance. 

# NON-PARAMETRIC MODELS. 
• KNNClassifier: Classifies based on the majority label among nearby data points. 
• DecisionTree: Splits data using feature thresholds for pure class outcomes.  
• BaggingClassifier: Combines predictions from multiple best with unstable base learners like 
trees. 
• RandomForest: A type of bagging with randomized feature selection at each split.  
• AdaBoostClassifier: Sequentially focuses on misclassified samples, adjusting weights to 
improve learning. 
• GBMClassifier: Builds trees sequentially, correcting errors at each stage.  
• XGBClassifier: An optimized version of GBM with regularization, handling sparsity, and fast 
computation. 


# BUSINESS INSIGHTS: 

• City Tier: Tier 3 cities have the highest churn (21.4%), Tier 1 the lowest (14.5%). 
• Payment Method: Cash on Delivery and E-Wallet users churn more than card users. 
• Account Segment: Regular Plus has the most customers—but also the highest churn. 
• Marital Status: Single customers churn more; married ones stay longer. 
• Complaints: Customers with complains on last 12 months seems to churn the most. 
• Tenure: Newer customers (<5 months) churn more. 
• Cashback: Less cashback often means more churn. 
o In City Tier 1, customers who preferred Debit Cards received cashback frequently, whereas 
those opting for E-Wallets received none.  
o In City Tier 2, frequent cashback was observed among UPI users, with E-Wallet users again 
receiving none.  
o Interestingly, in City Tier 3, the pattern shifts—E-Wallet users received the most cashback, 
followed by those using Debit Cards. 
• Coupons: Customers with less coupons churns often.   
• Account Structure: Accounts with too few or too many users show higher churn. 
• Tenure Patterns: Regular and Super Plus segments have longer tenure, especially in Tier 1 and 
2 cities. 
• Account segment and Tenure: 36.63% of customers chose the Regular Plus segment, their 
average tenure is significantly lower than other segments. 
• Including City_Tier in the analysis reveals that Regular segment customers demonstrate the highest 
tenure across all three tiers, followed by Super Plus. 
• The Regular Plus segment has the most customers, but their average tenure is low. Most of them 
contacted customer care just 2 or 3 days ago, which suggests frequent issues.This might also be the 
reason for less Tenure. 
• Although only 4.62% of customers belong to the Regular segment, they tend to have a longer tenure 
compared to other segments. Their engagement with customer care is also relatively better. 

# BUSINESS RECOMMENDATIONS: 
Tenure: 
• Customers with a tenure of less than five months are at a higher risk of churning, especially 
during their early post-signup period.  
• This vulnerability is often driven by competitive market offers that carry them away.  
• To counter this, businesses should prioritize engagement during these crucial early months by 
providing frequent cashbacks, compelling promotional offers, and discounted first-year 
memberships such as 50% offer to strengthen retention and build loyalty. 

CC_Agent_Score: 
• This is customer satisfaction score reflects the quality of service delivered by customer care 
agents.  
• To reduce the risk of churn from poor service interactions, businesses must take proactive 
steps to ensure top-tier support quality.  
• Investing in training, monitoring service standards, and fostering empathetic communication 
can significantly enhance the customer experience and build long-term loyalty. 

Complain_ly_Yes: 
• Customers who have raised complaints in the past year require special attention.  
• Businesses must actively monitor repeat issues to ensure they’re not recurring.  
• If the same problem persists, offering a free replacement or a full refund can demonstrate 
commitment to customer satisfaction helping to rebuild trust and prevent churn. 

Cashback: 
• Cashback is a powerful lever in influencing customer retention.  
• When aligned with tenure, it can play a critical role in reducing early-stage churn.  
• Providing more frequent or higher-value cashback during the initial months post-signup helps 
Business in reducing chances of early churn. 

Day_since_CC_contact: 
• Customers who have recently contacted customer care should be proactively monitored.  
• Prompt acknowledgment of their concerns, followed by timely and effective resolution, is 
critical.  
• Taking swift action not only strengthens customer trust but also reduces the likelihood of churn 
driven by unresolved service issues. 

Account_segment: 
• The Regular Plus segment appears to be the most susceptible to churn.  
• Customers in this group typically exhibit shorter tenure and frequent contact with customer care, 
pointing to recurring service issues or unmet expectations.  
• This suggests an urgent need for targeted retention strategies focused on strengthening engagement 
during the early lifecycle, proactively resolving service concerns, and restoring trust through tailored 
offers or enhanced support 

Expanding Customer Base in Tier 2 and Tier 3 Cities: 
Customer distribution analysis reveals a significant concentration in Tier 1 cities, while Tier 2 and Tier 3 
cities remain underpenetrated specifically in Tier 2. 
To boost overall customer volume and tap into emerging markets, the business should prioritize 
customer acquisition in these regions by performing:  
• Regional Offers. 
• Targeted Marketing. 
• Customer Referral Programs. 
• Expanding Delivery Network.
