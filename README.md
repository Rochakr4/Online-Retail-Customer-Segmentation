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
K means clustering and agglomerative clustering methods were used to produce clusters using RFM values. Both, the elbow chart as well as dendrogram analysis are suggesting that the customer base essentially comprises mostly of just two segments: Champions and Extinct cheaps. That is customers who either have high RFM scores or Low RFM scores. The population of the customers in between is quite low.

The future scope of the project includes bringing in demographic data of customers in order to be able to segment them better.

