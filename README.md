# **Introduction**
The ***"ga_sessions_366"*** table is a part of the ***"google_analytics_sample"*** dataset and it holds information about website sessions tracked by Google Analytics. This table covers a 366-day period and provides detailed insights into how users interact with the website and how the website performs. It includes important data like how long each session lasts, the number of pages viewed, where the users are located, and how they found the website. This information is crucial for website owners and marketers to make smart decisions about their online presence and improve user engagement and conversion rates.
<br>
<br> I will explore this dataset using SQL on Google Bigquery.
## **Table schema**
<br> ![image](https://github.com/honganh218/Explore-Ecommerce-Dataset/assets/133098903/522fefc3-3ced-4b19-8f7e-df013cd7eb08)
<br> For more information, please visit [[UA] BigQuery Export schema](https://support.google.com/analytics/answer/3437719?hl=en).

# **Exploring the Dataset**
### **Query 01: Calculate total visit, pageview, transaction and revenue for January, February and March 2017 order by month**
The table is stored in an array format, so we query ***"ga_sessions_2017"*** and ***"table_suffix"*** to filter for the month specified in the question.
<br> The ***'date'*** column is defined as a ***'string'*** type; therefore, ***PARSE_DATE*** is used to change the data type and ***FORMAT_DATE*** is used to make the result more readable.
<br>
<br> ![image](https://github.com/honganh218/Explore-Ecommerce-Dataset/assets/133098903/dcb3c4d7-f4df-4c7c-a707-498722880075)
<br> Part of result
<br>
<br> ![image](https://github.com/honganh218/Explore-Ecommerce-Dataset/assets/133098903/70bd34e4-dd68-4024-9762-eee9a5012ef0)
### **Query 02: Bounce rate per traffic source in July 2017**
<br> ![image](https://github.com/honganh218/Explore-Ecommerce-Dataset/assets/133098903/21b59581-eecd-498f-9343-fa811c4dc768)
<br> Part of result
<br>
<br> ![image](https://github.com/honganh218/Explore-Ecommerce-Dataset/assets/133098903/ec2cf0a7-894a-4c9d-8521-ef0fd07b2077)
### **Query 3: Revenue by traffic source by week, by month in June 2017**
![image](https://github.com/honganh218/Explore-Ecommerce-Dataset/assets/133098903/33a428a4-3aaa-4a68-baa5-cd436fab0316)
<br> Part of result
<br>
<br>![image](https://github.com/honganh218/Explore-Ecommerce-Dataset/assets/133098903/78c07ed0-8fe0-42a1-8932-aef0bcbba9a0)
### **Query 04: Average number of product pageviews by purchaser type (purchasers vs non-purchasers) in June, July 2017**
The idea is to create two CTEs independently. The first CTE will calculate the average pageview of purchasers, and the second CTE will calculate the average pageview of non-purchasers. Then, merging 2 tables using a ***LEFT JOIN***.
<br>![image](https://github.com/honganh218/Explore-Ecommerce-Dataset/assets/133098903/cb7c5d66-a8d3-410f-959c-d030def7a223)
<br> Part of result
<br> ![image](https://github.com/honganh218/Explore-Ecommerce-Dataset/assets/133098903/a8921bce-9c8f-4215-bf93-0a15bc1a617e)
### **Query 05: Average number of transactions per user that made a purchase in July 2017**
![image](https://github.com/honganh218/Explore-Ecommerce-Dataset/assets/133098903/a42acea6-0a2c-4c27-b75a-dc084633bdfe)
<br> Part of result
<br> ![image](https://github.com/honganh218/Explore-Ecommerce-Dataset/assets/133098903/a0031046-c850-4d5a-bddb-1a7e12cadf16)
### **Query 06: Average amount of money spent per session. Only include purchaser data in July 2017**
![image](https://github.com/honganh218/Explore-Ecommerce-Dataset/assets/133098903/ef8be654-df2b-4474-85ae-68feb5fe0456)
<br> Part of result
<br> ![image](https://github.com/honganh218/Explore-Ecommerce-Dataset/assets/133098903/40d9f789-3379-471e-98a5-dd06ed06a8ea)
### **Query 07: Other products purchased by customers who purchased product "YouTube Men's Vintage Henley" in July 2017. Output should show product name and the quantity was ordered.**
![image](https://github.com/honganh218/Explore-Ecommerce-Dataset/assets/133098903/f44d0a42-34aa-4845-a389-69e998c96556)
<br> Part of result
<br> ![image](https://github.com/honganh218/Explore-Ecommerce-Dataset/assets/133098903/3ac3c475-1107-4d04-957b-b86829bcbb29)
### **Query 08: Calculate cohort map from pageview to addtocart to purchase in last 3 month.**
![image](https://github.com/honganh218/Explore-Ecommerce-Dataset/assets/133098903/6bc7d626-3f3d-406c-b413-71adfb13a0dc)
<br> Part of result
<br> ![image](https://github.com/honganh218/Explore-Ecommerce-Dataset/assets/133098903/4e23f338-8801-43c9-b743-a4af84407348)


