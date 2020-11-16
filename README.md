# Homework-2

# Online Retail --- K-Means Clustering

#####    by <b>[Naidan Zheng](https://github.com/Naidanzheng)</b>

---

## Repo Content
- <b>Data</b> - The raw dataset can be found on the [UCI Machine Learning website](https://archive.ics.uci.edu/ml/datasets/Online+Retail). 
- <b>[images](https://github.com/Naidanzheng/Homework-2/blob/Master/Image)</b> - Various plots and images used in the documents found in this repo.
- <b>[Homework 2.ipynb](https://github.com/Naidanzheng/Homework-2/blob/Master/DATA602%20Project%201.ipynb)</b> - The main Jupyter Notebook containing the models and analysis for this project.
- <b>[README.md](README.md)</b> - A description of the project goals, process, and results.

---


## Table of Content
- <b>[Overview](https://github.com/Naidanzheng/Homework-2/blob/Master/README.md#overview) 
- <b>[Goals](https://github.com/Naidanzheng/Homework-2/blob/Master/README.md#goals) 
- <b>[Motivation & Background](https://github.com/Naidanzheng/Homework-2/blob/Master/README.md#motivation--background) 
- <b>[Data](https://github.com/Naidanzheng/Homework-2/blob/Master/README.md#data) 
- <b>[Modeling](https://github.com/Naidanzheng/Homework-2/blob/Master/README.md#modeling) 
- <b>[Conclusion](https://github.com/Naidanzheng/Homework-2/blob/Master/README.md#conclusion) 
- <b>[Future Work](https://github.com/Naidanzheng/Homework-2/blob/Master/README.md#future-work) 
- <b>[Software Requirements](https://github.com/Naidanzheng/Homework-2/blob/Master/README.md#software-requirements) 
- <b>[Resource](https://github.com/Naidanzheng/Homework-2/blob/Master/README.md#resource) 

---
## Overview
This is a transnational data set which contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail.The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers. We aim to segment the Customers based on K-Mean clustering and RFM so that the company can target its customers efficiently. After modeling, we find the customers with Cluster 2 accounts for only 19.01% but contributes 67.02% of sales, which is the key development target of the business, and also customers with Cluster 2 are frequent buyers.
![Online Retail.png](https://github.com/Naidanzheng/Homework-2/blob/Master/Image/Online%20Retail.png)


## Goals
The stakehold for this project is the online retailers, they can know exactly who their value customers are and who are the key development targets of their business.
We will be using the online retail transaction dataset to build an RFM clustering and choose the best set of customers which the company should target.


## Research Questions
1. Which customers are the most valuable customers? In other words, the total amount of consumption is the highest in a specific time frame. What are the customers characteristics of these high-value customers?
2. Which customers are the most loyal customers(the customers with the highest repurchase rate)?
3. Which group of customers is most likely to respond to our current campaign? 

## Motivation & Background
Traditional retailers are competing to change e-commerce. The consumption behavior of online consumers has become traceable due to the Internet, and a great deal of consumption data has been generated. All electronic retailers face challenges as to how to use this information to mine valuable business data. I am very interested in this topic because my family has a small business, so I hope to earn experience and to use these skills in my family business and future work.




## Data
The dataset contains about a year worth of transactions (dec-2010 to dec-2011) from an online retail company based on in the UK.
This dataset has 8 columns and 541,909 columns, it contains the customer ID, the price of the product, the quantity purchased, the product code, the date of purchase and the country of the product.
![Data.png](https://github.com/Naidanzheng/Homework-2/blob/Master/Image/Data.png)


From this graph, we can clearly see that November is the peak of shopping, the least people shop in February.
Therefore, online retailers can stock up before November to ensure that there are enough goods, and in February, they can provide some discounts to attract customers.
![Month.png](https://github.com/Naidanzheng/Homework-2/blob/Master/Image/Month.png)


The main customers are from the UK, and there are relatively few overseas customers, so online retailers can consider how to attract overseas customers and increase their sales.
![Country.png](https://github.com/Naidanzheng/Homework-2/blob/Master/Image/Country.png)

## Modeling
In clustering calculations, K-Means is a very popular algorithm, and this method is used in this analysis to mine value users.
There are several methods for selecting the number of clusters, and the Elbow Criterion method is used here.
![Cluster.png](https://github.com/Naidanzheng/Homework-2/blob/Master/Image/Cluster.png)
When k = 4, the curve starts to change smoothly, so choose 4 as the number of clusters.

Customers have been grouped, let's look at the consumption behavior characteristics of different types of customers.
These three  graphs show the value customer's contribution to sales.
![Monetary.png](https://github.com/Naidanzheng/Homework-2/blob/Master/Image/Monetary.png)
![Recency.png](https://github.com/Naidanzheng/Homework-2/blob/Master/Image/Recency.png)
![Frequency.png](https://github.com/Naidanzheng/Homework-2/blob/Master/Image/Frequency.png)

To generate value users, compare the user portrait results obtained by the two methods, the result obtained by the K-Means method is better, and the final value users excavated accounted for 19.01% but contributed 67.02% of sales. Customers with Cluster 2 are the frequent buyers and most valueble customers, so they will respond to online retailers' current campaign. Therefore, Customers with Cluster 2 are the key development target of the business.



## Conclusion
Through descriptive statistical analysis, we learned about the overall operation of the e-commerce company, and calculated the monthly sales volume and total monthly sales. The monthly sales increased significantly in September, October and November 2011, and the least people shop in February. Therefore, online retailers can stock up before November to ensure that there are enough goods, and in February, they can provide some discounts to attract customers. We found that most of the orders are from the UK.

In order to mine valuable users, we use two methods. The first method is to use the RFM model to group users, and the second method is to use the K-Means algorithm to group users by "machine learning". Both methods are mining. To generate value users, compare the user portrait results obtained by the two methods, the result obtained by the K-Means method is better, and the final value users excavated accounted for 19.01% but contributed 67.02% of sales. Customers with Cluster 2 are the frequent buyers and most valueble customers, so they will respond to online retailers' current campaign. Therefore, Customers with Cluster 2 are the key development target of the business.

## Future Work
After determining the value user, I can further learn the consumption habits of the value user, so as to provide a consumer-centric smart business model, and perform multiple iterations according to the actual application to optimize the value user mining model. I will test and compare the solutions with other clustering methods, and determine the areas of improvement.

## Software Requirements
<pre>
Languages    : Python 3.9.0
Tools/IDE    : Anaconda, Colab
Libraries    : numPy,pandas, matplotlib, seaborn, datetime, scikit-learn,warning 
</pre>

<pre>
Duration     : November 2020
Last Update  : 11.13.2020
</pre>


## Resource

- <b>[RFM Analysis for Customer Segmentation](https://clevertap.com/blog/rfm-analysis/)
- <b>[Understanding K-means Clustering in Machine Learning](https://towardsdatascience.com/understanding-k-means-clustering-in-machine-learning-6a6e67336aa1)
