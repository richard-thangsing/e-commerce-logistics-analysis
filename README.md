# E-Commerce Logistics Metrics Analysis
## Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning/ Preparation](#data-cleaning-preparation)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Results/ Findings](#results-findings)
- [Recommendations](#recommendations)

### Project Overview
This data analysis project aims to provide vital insights into some key performances of an e-commerce enabler and marketplace integrator department store called Olist in Brazil over the past year. By poring over and analyzing various aspects of the orders/ sales data, we seek to identify crucial business insights, make data-driven actionable recommendations to streamline certain processes and logistics, and finally gain a deeper understanding of the store's performance.

### Data Sources
Orders Data: The dataset used for this analysis is the Olist's 'olist_order_dataset.csv' file, containing information about each sale made by the store.

### Tools
- pandas for Exploratory Data Analysis (EDA)
- matplotlib for visualization
- seaborn for visualization

### Data Cleaning/ Preparation
In the initial data preparation phase, we performed the following tasks:
1. Data loading and inspection
2. Checking and handling null/ missing values
3. Data cleaning and formatting

### Exploratory Data Analysis (EDA)
EDA involved exploring the orders data to answer several key questions such as:
1. What does the order status distribution look like?
2. What is the percentage of orders delivered early, on-time, or late?
3. What is the average delivery time?
4. What are the quantiles of delivery times?
5. The monthly order volume trend. 
6. What is the cancellation rate?
7. What is the repeat purchase rate?

### Results/ Findings
The analysis results are presented/ summarized as follows:


<img width="298" height="268" alt="order_status_dist" src="https://github.com/user-attachments/assets/f01dac74-1e24-4c59-98ce-03f2b03fb959" />


1. Olist has a good On-Time Delivery (OTD) rate - 91.89% of the orders are delivered early, this is crucial for maintaining high seller ratings on marketplaces and shows the efficiency and optimization of the logistics. 1.34% orders are delivered on time and 6.77% are delivered late, outside the promised window.
2. The average delivery time is 12.56 days. However, this is highly sensitive to extreme outliers making it less reliable for customer promises. In this case the median value of 10.22 days is a more accurate indication of the days taken for an order to get delivered. 50% of orders take less than 10.22 days, and 50% take longer. This is what the customer typically experienced.


<img width="428" height="289" alt="detailed_quantiles" src="https://github.com/user-attachments/assets/e6ad14d1-9fe1-423f-bc57-495f65a2e2ea" />

<img width="1214" height="578" alt="monthly_order_volm" src="https://github.com/user-attachments/assets/dc06ac16-316b-4fce-a8ff-014879ff2a7d" />

3. Olist has a cancellation rate of 0.63% which can be considered outstandingly low and highly acceptable. For B2B e-commerce platforms a cancellation rate of < 1.0% is healthy, it indicates strong supply chain integration and minimal catalog listing errors. For standard B2C e-commerce a cancellation rate of 2.0%- 8.0% is excellent, it signals robust inventory sync, low fraud rates, and high consumer trust. In Amazon Marketplace a cancellation rate of < 2.5% is considered best_in-class, far below the threshold where account suspension risk occurs.
4. The repeat purchase rate is 0.00%. There are no customers who made more than one purchase.

### Recommendations
After an analysis of the Average Process Time, it has been found that the approval time of 0.43 days, i.e., about 10 hours is excellent. However, the time to carrier is a bit mixed. Nearly 3 days to hand an item to a courier is slow for retail. For a marketplace integrator like Olist, this reflects small merchants taking time to pack items, or the time spent shipping items to a central cross-docking hub before final dispatch.
For a pure B2C buyer, 12.56 days is unacceptable today. Modern consumers expect delivery within 2 to 5 days. For a hybrid integrator managing independent cross-country sellers, this is decent and realistic, but needs optimization.
So taking all the above into consideration some recommendations include:
1. A focus on lowering the Time to Carrier by penalizing slow merchants, or incentivizing them to use a fulfillment service.
2. A business solution where products are pre-stowed in a central partner warehouse to remove or mitigate the timeline constrained on account of third-party carriers and decentralized warehouses.




