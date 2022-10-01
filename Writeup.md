# Customer Segmentation 
Calvin Yu
## Abstract 
The goals of this project are to find out the VIP class, to analyze the retention rate, and to do basket analysis for cross-selling. The dataset I used is from UCI, and it has 541909 rows of purchase records with 8 columns. I grouped the dataset by the customer ID, and there are 4372 customers. I used recency, frequency, and monetary to divide the customers into 4 groups. Then, I used the Kmeans clustering algorithm to find the VIP group. I also did a cohort analysis to see the retention rate per month, so the company can have the insight to know when to do promotion. After that, I did a basket analysis using mlxtend to get related items for cross-selling.
## Design
A retail company believes that customer acquisition costs five times more than customer retention, therefore, the CEO would like to focus on the valuable customers and try to make them loyal customers. My job is to identify the valuable customers, give the CEO a breakdown of the retention rate over months, and do cross-selling to maximize the profits. 
## Data
### Online Retail xlsx 
- 541909 rows with 8 columns 
- 4372 customers 
- feature highlights : description , invoice Date, and quantity 
## Algorithms 
1. Use pandas to read the xlsx file and check for missing values
2. Do a Exploratory Data Analysis to evaluate the features 
3. Create the recency function that takes the invoice year and month , and return the recency levels
4. Create the frequency function that takes the total number of purchases of a customer, and return the frequency level
5. Create the monetary function that takes the total spending price of a customer, and return the monetary level
6. Merge the three functions above into a new dataframe, and use elbow method to find the best number of kmean clusters 
<img width="361" alt="Screen Shot 2022-09-28 at 7 12 38 PM" src="https://user-images.githubusercontent.com/63031028/192923267-6d949500-a9bb-46f0-b232-5b32c4a4910b.png">

7. Four is the optimize number, so will use Kmeans to divide the customers into four groups

8. Evaluate the cluster center to find out which group is the VIP 
9. Cluster 2 is the VIP cluster, and will explore what products the VIP class buy the most 

10. Find out that white hanging heart t-light holder is the best selling product in our vip class, show the top items to the marketing team, and let them decide what to do next
<img width="795" alt="Screen Shot 2022-09-30 at 7 28 22 PM" src="https://user-images.githubusercontent.com/63031028/193379608-9414a174-92a8-4f79-9bc2-d5241fcba8c2.png">

11. Create a cohort pivot table to see the retention rate over months 
<img width="796" alt="Screen Shot 2022-09-30 at 7 30 27 PM" src="https://user-images.githubusercontent.com/63031028/193379655-baf2a30d-73a4-430f-86b5-d07548f88a78.png">

12. Use mlxtend to find related items for cross-selling and will recommend the related product to the customers 

## Tools
- Numpy, Pandas : Data engineering, Exploratory Data Analysis
- Matplotlib, Seaborn : Data visualizations 
- Scikit learn - Clustering Algorithm
- Mlxtend - Basket Analysis

## Communication 
Identifying the VIP class can make the company knows whom they should be foucsing on when doing marketing campaign. The bar chart of the best products sold in the VIP class also gives us information on what products should we be prioritizing on when doing promotions. The cohort pivot table shows us the retention rate over month, so the marketing team can do A/B testing. Finally, the basket analysis I did is for cross-selling. So, the idea is that when a customer buys a product, we will recommend a related product to them to expand our profits. 

## Future steps
1. Discuss with the marketing team on what and when should the company do promotions 
2. Dig into the VIP group to see their buying habits 
3. Email the VIP customers with rewards to keep them as loyal customers 
