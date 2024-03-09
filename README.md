
# Customer segmentation using RFM method

## Introduction
In this project, we will be using a dataset from Kaggle ([__Raw data__](https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci/data)) that contains the online purchase history recorded from December 2009 to December 2011. 

__Annotation__
Data label| Meaning
---|---
Invoice | Order identify number 
StockCode | Product identify number 
Description	|Product Name
Quantity | Product Quantity
InvoiceDate	| Purchase Date
Price | Product's price per piece
Customer ID	| Customer identify number
Country | Customer's Country


The customer data will be used to evaluate and rank using the RFM (Recency, Frequency, Monetary) method. This aims to support the business unit in identifying potential customer groups and developing a targeted approach strategy for the future.

By analyzing and ranking customers based on RFM, we can identify important and potential customer groups. This helps the business unit focus on developing targeted approaches and creating noteworthy marketing programs to enhance interaction and customer retention.

## Project dashboard: [__Link__](https://app.powerbi.com/view?r=eyJrIjoiOTg3OWNkOTktNjVhYy00Mzk3LWE0NWMtYmIzNjkwODE1ZGRlIiwidCI6Ijg4ZjViZjc2LWVhZWYtNDE5Yy1iZTgxLWUwYmNhZjJkNTA4MyIsImMiOjEwfQ%3D%3D) 
![cover](https://github.com/vp1082000/RFM-customer-segment/assets/143709845/8b14acdd-1d99-413b-a969-1c7cb5994dd5)

## RFM method
RFM is a customer segmentation method based on three main factors:

- Recency: The time since the customer's last transaction.
- Frequency: The number of times the customer made a purchase or transaction within a specific period.
- Monetary: The total value of transactions made by the customer.

Each of the Recency, Frequency, and Monetary indices will be evaluated on a scale from 1 to 5, with each score being assigned to a corresponding value range (depending on the evaluation time frame and industry characteristics, these value ranges may vary).

__Example__: in this project, since we don't have any specific industry characteristics, the Monetary index will be divided into five evenly distributed groups based on percentiles at the 0.2, 0.4, 0.6, and 0.8 thresholds.

![RFM example](https://github.com/vp1082000/RFM-customer-segment/assets/143709845/377ad5f1-2d4f-4a1d-b22a-6a4e13ce94ff)

## Overview

__Business results__:
![overview2](https://github.com/vp1082000/RFM-customer-segment/assets/143709845/44e68ca1-c587-4283-b1be-c4cddb4465ed)

During the three-year data recording period from December 2009 to December 2011, the business unit served 5942 customers. Throughout this period, a clear trend can be observed each year, with an increasing number of customers in the months of September and October, reaching its peak in November. The main consumed items during this period were gift products and home decorations.

![overview1](https://github.com/vp1082000/RFM-customer-segment/assets/143709845/d35dba30-b7a0-4445-b799-3d345bff4048)

The explanation for this trend is that this time period is close to the end of the year and coincides with the family gathering holidays in European and American countries, which attract a large number of customers.

__Churn rate__:

![overview3](https://github.com/vp1082000/RFM-customer-segment/assets/143709845/85467430-250b-4547-ad00-d1a9dab09772)

In a highly competitive, price-sensitive retail industry, a churn rate of 15.03% can be considered acceptable. However, the fact that 79.18% of customers are returning indicates a significant level of customer loyalty. To improve business performance, it would be beneficial to focus on acquiring new customers and maintaining relationships with existing customers to reduce the churn rate.

## Cusomer segmentation

Based on the Recency, Frequency, and Monetary point assigned to customer and the characteristics of each group, we can segment the customer data into 10 distinct groups.

Index|Rank|Characteristic
---|---|---
1|	Champions|	Bought recently, buy usually and have large spending budget.
2|	Loyal| 	Medium-large spending budget and buy often.
3|	Potential| Loyalist	Bought recently, and buy more than one but have low-medium budget.
4|	Recent Customers|	New comer with occasionally bought and low budget.
5|	Promising|	bought recently,occasionally but with large budget.
6|	Need Attention|	Didn't bought recently but have medium budget and buy often.
7|	At Risk|	Didn't bought for a perior but have larget budget and/or used to buy often.
8|	Can't Lose|	Didn't bought for a long perior but have larget budget and/or used to buy often.
9|	Hibernate|	Didn't bought for a perior and have low budget and buy occasionally.
10|	Lost|	Didn't bought for a long perior and have low budget.

Apply that to the dataset and we can get the current state of each segment through the tree map.

![Segment1](https://github.com/vp1082000/RFM-customer-segment/assets/143709845/8256bdcf-c861-4ce3-907d-31c943bceea1)


The detail on average Recency, Frequency and Monetary of each rank show as below.

![Segment2](https://github.com/vp1082000/RFM-customer-segment/assets/143709845/546efc9c-ed52-4ef7-97ae-b9a015208e44)

Based on the customer segmentation and spending characteristics of each group, we can prepare different approaches for each customer group that the company wants to focus on for future development. These approaches may include tailored marketing strategies, personalized offers, targeted communication channels, and specific product or service enhancements to meet the unique needs and preferences of each customer group. 

By understanding the distinct behaviors and preferences of each group, the company can effectively allocate resources and prioritize efforts to maximize customer satisfaction and business growth.


Index|	Rank|	Marketing Strategy
---|---|---
1|	Champions|	Reward them through new products. Likely to adopter and promote your brand.
2|	Loyal| 	Upsell higher value products. Engage them in new compagn and  ask for review.
3|	Potential Loyalist|	Offer membership program, recommend other products.
4|	Recent Customers|	Provide on-boarding support, start duilding relationship.
5|	Promising|	Create brand awareness, offer small discount to engage for first/second buy.
6|	Need Attention|	Make limited time offers. Recommend based on past purchase. Reactive them.
7|	At Risk|	Invest valuable resources like recommend popular products at discount, reconnect with them.
8|	Can't Lose|	Send personalized email to reconnect, offer discount, provide helpful resources to win them back.
9|	Hibernate|	Recreate brand value through offer relevant product and special discounts.
10|	Lost|	Create campaign that revive interest, otherwise ignore.

___THE END___






























