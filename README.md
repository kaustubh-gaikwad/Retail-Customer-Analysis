## Retail Customer Behavior & Segmentation Analysis
Designed and executed a full-cycle retail analytics solution on 500K+ real-world transactions, analyzing customer behavior, performing RFM-based segmentation, and delivering data-driven insights to support targeted marketing, customer retention, and revenue optimization strategies.

## Project Overview

This project replicates a real-world analytics workflow similar to what a Data Analyst at Google or Meta might perform.
Using the UCI Online Retail dataset, analyzed customer transactions to uncover:

Revenue trends & seasonal behavior 

Product performance & sales distribution 

High-value customer segments via RFM analysis 

The goal is to demonstrate how data-driven insights can support business growth, retention, and marketing optimization — core functions of data analytics teams at leading tech companies.

## Dataset Summary

Source: UCI Machine Learning Repository – Online Retail (https://archive.ics.uci.edu/ml/datasets/online+retail) 541,909 transaction records (Dec 2010 – Dec 2011)
Cleaned dataset: (https://docs.google.com/spreadsheets/d/1dlw8GFbVH-gvvlg-3NgS34JFWUA2Jecb/edit?usp=sharing&ouid=106531511300919198144&rtpof=true&sd=true)
| Stage                            | Rows Remaining | % Retained |
| :------------------------------- | :------------: | :--------: |
| Original raw data                |   **541,909**  |    100%    |
| Drop missing `CustomerID`        |    ~406,829    |    ~75%    |
| Remove cancellations / negatives |    ~397,924    |    ~73%    |
| Drop duplicates, etc.            |  **~392,692**  |  **~72%**  |



Features: InvoiceNo, StockCode, Quantity, InvoiceDate, UnitPrice, CustomerID, Country

Region: Primarily UK customers
## Tools & Technologies
Category	Stack
Language	Python 
Libraries	Pandas, NumPy, Matplotlib
Environment	Jupyter Notebook
Data Format	Excel → CSV outputs, PNG visualizations

## Data Cleaning & Preparation

Performed rigorous preprocessing to ensure accuracy and consistency:

Removed cancelled invoices (InvoiceNo starting with “C”)

Filtered positive Quantity and UnitPrice values

Dropped rows missing CustomerID

Converted InvoiceDate to datetime format

Created TotalPrice = Quantity × UnitPrice

Removed duplicates


## Exploratory Data Analysis (EDA)
1. Top Products by Sales & Revenue

- Identified SKUs driving the highest revenue and sales volume.
- Revealed which products contribute disproportionately to profits — an example of Pareto (80/20) distribution in retail.

2. Monthly Revenue Trend

- Displays strong seasonality — peak months likely align with holiday campaigns.

- This pattern can guide inventory planning and marketing spend allocation.

3. Distribution of Order Values (Log Scale)

- Most orders are between $100 – $1,000.

- A long-tail pattern exists — few high-value orders generate a large portion of total revenue.

- Typical of marketplaces like Amazon, Meta Ads, or Google Shopping.

4. Cumulative Distribution of Order Values

- ~90 % of orders are below a few thousand dollars.

- Highlights skewed spending behavior and reinforces the need for customer segmentation.

## RFM (Recency–Frequency–Monetary) Analysis
Metric	Description	Business Meaning
Recency (R)	Days since last purchase	Measures engagement freshness
Frequency (F)	Number of invoices	Indicates loyalty and repeat behavior
Monetary (M)	Total spend	Reflects customer lifetime value (CLV)

We assigned quintile scores (1 – 5) and built an RFM_Score to classify customers.

## Customer Segments
Segment	Description	Business Strategy
- Champions	Recent, frequent, high-spending	Reward with loyalty programs
- Loyal	Repeat buyers with good recency	Maintain retention
- At Risk	Previously active, now dormant	Re-engagement campaigns
- Dormant	Low frequency & old activity	Consider churned
- Potential	Moderate recency or spend	Target for upselling

 Output: rfm_table.csv

## Key Insights

- The business relies heavily on high-value “champion” customers for revenue.

- Seasonal revenue spikes highlight the importance of time-based promotions.

- The long-tail effect shows that a small percentage of customers drive most sales.

- RFM segmentation provides actionable marketing insights:

- Personalize offers to retain loyal customers

- Target at-risk customers with win-back campaigns

- Identify growth opportunities within “potential” segments
  

## Skills Demonstrated

- Data wrangling and cleaning in Pandas

- Exploratory Data Analysis (EDA)

- Visualization & storytelling with Matplotlib

- RFM segmentation & behavioral analytics

- Business insight communication using data



📁 Project Structure

- Retail_Analysis_Pipeline.ipynb – Main Jupyter notebook

- Online Retail.xlsx – Raw dataset (UCI source, not uploaded due to size)

- outputs/ – Folder containing generated results:

- retail_clean.csv – Cleaned dataset (~392k records)

- eda_top_products.csv – Top-selling products summary

- eda_monthly_revenue.csv – Monthly revenue trend data

- rfm_table.csv – RFM segmentation table
  
- rfm segment.png - Customer count by segment

- monthly_revenue.png – Monthly revenue chart

- top_products.png – Top products by revenue chart

- order_value_distribution_log_bins.png – Order value histogram (log scale)

- order_value_cdf_logx.png – Cumulative distribution (log scale)

- README.md – Project documentation and explanation
  
## Business Impact Summary

This project simulates a data-driven decision support system — similar to those used by e-commerce, advertising, or analytics teams at Google, Meta, or Amazon.
It demonstrates the ability to transform raw transactional data into insightful visualizations and actionable recommendations for business growth.

LinkedIn: http://linkedin.com/in/kaustubhgaikwad-msba |  kaustubh01gaikwad@gmail.com
