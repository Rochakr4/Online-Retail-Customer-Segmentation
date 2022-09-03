# Online-Retail-Customer-Segmentation
# Introduction
With the evolution of marketing techniques, firms are now able to reach a much wider audience than ever before. But it’s not practical to spend their efforts on this wide population uniformly. One needs to identify the segment of the customer base and how these segments are responding to the product/service. Only then would one be able to take adequate measures and receive a better response from their customers. This is what we call customer segmentation.
Here I’ll develop an Unsupervised ML Clustering model to segment the customers of an online retail store to help them understand their customer base better.


# Objective:
To cluster the customer base of this particular online retail store using Unsupervised clustering algorithms, so that the management can take tailored decisions for each segments.

# Data



1 InvoiceNo object

2 StockCode object

3 Description object

4 Quantity int64

5 InvoiceDate object

6 UnitPrice float64

7 CustomerID float64

8 Country object


# Approach

There are many segmentation methodologies in use today, of which I’ve used the Recency, Frequency, and Monetary (RFM) methodology, which scores each customer on these metrics and segments them accordingly. 
Recency is how recent the customer’s last purchase was. Lower the recency better for the business.
Frequency and monetary metrics describe how frequent each customer is and how much they spend with the business. The higher these scores, the better the customer is for the firm.
These metrics coupled with unsupervised ML algorithms would give us a better idea about what kind of customer base the store has. I’ll use K mean clustering and Hierarchical agglomerative clustering for the task.

# Results
I started with data cleaning and necessary feature changes. Then, to comprehend the data,
an EDA was performed, which yielded many meaningful insights about the data. Then, using the
available features, a behavioural customer segmentation based on recency, frequency, and
monetary value was carried out.

The quintile method was used to compute R, F, and M scores, which divide recency, frequency,
and monetary values into 5 groups (denoted from 1 to 5). Then, by combining R, F, and M scores,
a three-digit RFM cell code was created and a composite score, which is the weighted sum of R,
F, and M scores, was created.

Based on RFM cell code, customers were classified into 9 customer segments (‘Loyal Customer’,
‘Potential Loyalist’, ‘Recent Customers’, ‘Promising’, ‘Customers Needing Attention’, ‘About To
Sleep’, ‘At Risk’, ‘Can’t Lose Them', and ‘Lost’) and analysed.

Based on the RFM composite score, customers were classified into 5 customer segments (A+, A,
B+, B, C) and analysed.

Before implementing Kmeans and hierarchical clustering techniques (using recency, frequency,
and monetary values), necessary feature engineering was carried out. Both Kmeans and
hierarchical clustering suggested the presence of two clusters.

The clusters created were analysed with respect to customer segments created using RFM cell code
and composite score.

In the case of K-means clustering,

 K-means is able to distinguish clearly between 'lost' and 'Loyal Customer'
categories.

 The first cluster contains all customers classified as 'Lost', 76% of customers
classified as 'Can't Lose them' and 98% of customers classified as 'About to
Sleep'.

 The second cluster contains 98% of all customers classified as 'Loyal customer'
and 91% of customers classified as 'Potential Loyalist'.
 Considering customer grade, the first cluster mainly contains high-graded
customers and the second cluster contains mostly low-grade customers.

In the case of Hierarchical clustering,

 The first cluster contains 81% of customers classified as 'Recent customer' and
76% of customers classified as 'About to sleep'.

 The second cluster contains all customers classified as 'At Risk' and 78% of
customers classified as 'Loyal customer'.

 The first cluster contains 87% of customers classified as 'A+' and 80% of
customers classified as 'A'.

 The second cluster contains 75% of customers classified as 'C'.

