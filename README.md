# BUAM-RETAIL-CHAIN-ANALYSIS

![Buam-ezgif com-speed](https://github.com/user-attachments/assets/f4e4590f-c0b9-4556-afc6-cbe703d33f78)

## TABLE OF CONTENT
- [INTRODUCTION](#INTRODUCTION)
- [OBJECTIVE](#objective)
- [GOALS](#goals)
- [SKILLS DEMONSTRATED](#skills-demonstrated)
- [DATA OVERVIEW](#data-OVERVIEW)
- [DATA CLEANING/TRANSFORMATION](data-cleaning-/-transformation)
- [DATA MODELLING](#data-MODELLING)
- [ANALYSIS](#analysis)
- [DASHBOARD LINK](#dashboard-link)
- [RECOMMENDATIONS](#recommendations)
- [CONCLUSION](#conclusion)

## INTRODUCTION
Buam is a fast-growing regional retail-chain specializing in a diverse range of products, from
coffees, soft drinks to beverages. With over 15 stores across urban and suburban areas, the
company has established a solid reputation for providing high-quality products at competitive
prices. The company prides itself on its customer-centric approach, constantly striving to
enhance customer satisfaction through personalized shopping experiences, targeted promotions,
and a commitment to delivering value.


## PROBLEM STATEMENT
This retail chain is experiencing stagnant sales growth despite an increase in foot traffic and
online visitors. The company’s leadership believes untapped opportunities lie in understanding
customer behavior, identifying high-performing products, and optimizing inventory. However,
the business lacks clear insights into customer preferences, purchasing patterns, and potential
areas of inefficiency within its sales process.

## OBJECTIVE
Through this project, Buam aims to harness its rich repository of customer and sales data to gain
actionable insights, optimize product performance, and reinforce its competitive edge in the retail
market.
To achieve this, there is a need to an interactive dashboard that combines data from different
sources.

## GOALS
1. Identify top-performing products, locations
2. Analyze trends over time
3. Detect underperforming products and potential reasons for poor sales.
4. Recommend strategies for targeted marketing and promotions.

## SKILLS DEMONSTRATED
- Power query
- Data Modelling
- Data Analysis Expression(DAX)
- Data cleaning/transformation
- Data Visualization
- Exploratory Data Analysis
- Problem-Solving

## DATA OVERVIEW
The dashboard was built using four different tables and a calendar table that was created in
power query, and each of these tables contains the following columns:

**1. Fact Table**  
- **CustomerID**: Links each transaction to a specific customer to enable customer-based analysis.  
- **ProductID**: Identifies the product involved in the transaction for performance tracking.  
- **SalesPersonID**: Associates each transaction with a salesperson for performance evaluation.  
- **Quantity Sold**: Captures the number of units purchased in a single transaction.  
- **Quantity returned**: Captures the number of units returned in a single transaction.  
- **OrderDate**: Records the date the transaction took place to support time-based analysis.  

**2. Customers Table**  
- **CustomerID**: Acts as the unique identifier for each customer, linking customer data to transactions.  
- **Full Name**: Stores the customer’s full name for reporting and personalized engagement.  
- **Customer Age**: Facilitates segmentation and analysis of customers based on age groups.  
- **Gender**: Allows demographic studies and the creation of targeted marketing strategies.  
- **Location**: Provides the customer’s address or region for regional sales analysis.  

**3. Product Table**  
- **ProductID**: Uniquely identifies each product in the inventory.  
- **ProductName**: Represents the name of the product for easy reference and reporting.  
- **Category**: Groups products into categories for aggregated performance analysis.  
- **Sales Price**: Denotes the selling price of the product, used in revenue calculations.  
- **Cost Price**: Denotes the actual price of the product, used in profit calculations.  

**4. Sales Person Table**  
- **SalesPersonID**: Acts as the unique identifier for each salesperson in the organization.  
- **Full Name**: Captures the salesperson’s name for tracking individual performance.  
- **Store Name**: The name of the store of the salesperson.  
- **Date of Birth**: Date of birth of the salesperson.  

**5. Calendar Table Columns and Descriptions**  
- **OrderDate**: Represents the order date, formatted as YYYY-MM-DD, serving as the primary key for linking with fact tables.  
- **Day**: The day of the month (1–31), useful for analyzing daily trends or patterns.  
- **DayName**: The name of the day (e.g., Monday, Tuesday), helpful in identifying weekday vs. weekend trends.  
- **Week**: The week number of the year (1–52), allowing weekly aggregation of data.  
- **WeekDayNumber**: A numerical representation of the weekday (e.g., 1 for Monday, 7 for Sunday), useful for sorting or calculations.  
- **MonthNumber**: The month of the year (1–12), used for monthly trend analysis.  
- **Month**: The name of the month (e.g., January, February), providing clarity in visualizations and reports.  
- **Quarter**: The quarter of the year (1–4), enabling quarterly performance analysis.

## DATA MODELLING
A star schema was used for the modelling. The fact table which contained the observational data
was connected directly to 4 dimensional table forming a one-many cardinality

 <p align="center">
  <a href="">
    <img src="https://miro.medium.com/v2/resize:fit:1100/format:webp/1*vVdiy1zdfoGOd7Nso4YBxQ.png">
  </a>


## ANALYSIS
<p align="center">
  <a href="">
    <img src="https://github.com/user-attachments/assets/0e582efa-5f03-45c2-9ba3-48e1ef0b0e4d">
  </a>

**1. Key Performance Index (KPI):**

 <p align="center">
  <a href="">
    <img src="https://miro.medium.com/v2/resize:fit:1100/format:webp/1*zCTsX4suCA0z7ypF96wY7w.png">
  </a>

This is a summary that gives a comprehensive view of the retail chain performance

- **Cost Of Goods Sold: $3.1M**
  
This indicates the initial cost of purchasing all drinks and beverages that were sold in all
the stores.
- **Total Revenue: $5.4M**
  
This KPI is reflects the total cash flows generated from retailing drinks and beverages
across all the stores
- **Profit Margin: $2.3M**
  
This is the difference between Total Revenue and COGS, representing the gross profit
from selling drinks and beverages.
- **Profit Margin: 42.2%**
  
This is the gross profit expressed as a percentage of total revenue. It indicates the portion
of revenue retained as profit after covering direct costs. It a key indicator of profitablility.

**2. CUSTOMER ANALYSIS**
 - **Profit By Gender**
<p align="center">
  <a href="">
    <img src="https://miro.medium.com/v2/resize:fit:640/format:webp/1*o8jKfDvMq5RuqBc0AYrGIw.png">
  </a>

  
51.5% of the customers are female while the remaining 48.5% are male
The profit split between genders is almost equal, suggesting that both male and female
customer groups significantly contribute to the company’s profitability.
This slight difference might indicate product preferences of the female demography

- **Profit By Age Group**
 <p align="center">
  <a href="">
    <img src="https://miro.medium.com/v2/resize:fit:640/format:webp/1*_2kEaMdIvLPeDQOrjjAznw.png">
  </a>

This bar chart displays Profit by Customer Age, broken into four age ranges, along with the average customer age 45

**21–60 Age Group Dominates Profit:**
The majority of the profit comes from customers aged 21–40 ($815,857) and 41–60 ($869,426), which aligns with the average customer age of 45.
These groups likely represent the most active and financially capable demographics.

**Lower Contribution from 0–20 and 61–80 Groups:**
The 0–20 age group contributes the least profit ($77,465), which is expected due to limited purchasing power (e.g., students or dependents).
The 61–80 age group contributes moderately ($534,763), possibly due to a focus on essentials, reduced spending on non-essential items.


**LOCATION**
- Total Sales Location: *20*

- **Top-5 Profitable Locations**
 <p align="center">
  <a href="">
    <img src="https://miro.medium.com/v2/resize:fit:1100/format:webp/1*_w2uf17qkyU1nwl5gWokeQ.png">
  </a>

This visual shows the best and least 5 profits by location, customers and sales person. It gives users the flexiblility of toggling between the metrics highlighting the corresponding KPI and top or bottom values.

- The store’s most profitable location is in Washington with $135k profit margin

- California follows closely with $133k, contributing significantly to the total sales.

- Michigan, Virginia and Missouri make the top five with close values of $132k, $131k and $128k respectively.


This visual tells the most valuable locations in terms of profit margin, helping to quickly identify the key locations driving the most of the retail chain.

- **Bottom-5 Profitable Locations**
   <p align="center">
  <a href="">
    <img src="https://miro.medium.com/v2/resize:fit:786/format:webp/1*J3ErPopfyWJ1aRCFe5WWUA.png">
  </a>

- The retail chain’s least profitable customers is in Travis Ewing with approx. less than $1k profit margin

- Lisa West follows very closely with about $1k as well

- Bobby Abbott, Christine Hawkins and Jeffery Powell complete the bottom-5 customers all less than $1k.

         The insight from this chart points the need for better customer services and customer retention strategies.

**SALES PERSON**

- Total Sales Person - 10

- **Top-5 Profitable Sales Person**
   <p align="center">
  <a href="">
    <img src="https://miro.medium.com/v2/resize:fit:828/format:webp/1*Wlxo4BeN6pQNObtcLfhJtQ.png">
  </a>

- The store’s most profitable Sales Person is in Crystal Franco with $244k profit margin

- Christopher Cameron follows closely with $234k, contributing significantly to the total sales.

- Dustin Manning, Anthony Lee and William Gon Virginia and Missouri make the top five with close values of $132k, $131k and $128k respectively.

This visual tells the most valuable Sales Person in terms of profit margin, an indicator to the key Sales Persons driving the most of the retail chain.

- **Bottom-5 Profitable Sales Person**
   <p align="center">
  <a href="">
    <img src="https://miro.medium.com/v2/resize:fit:828/format:webp/1*G539xO1y1SUhcs5GWSGHKQ.png">
  </a>

- Tammy Monroe with $220k in Profit, is the least profitable salesperson.
- Seth Adams follows closely with $222k
- Kelsey Beard, Kimberly McDonald and Kelsey Zimmerman follow with decreasing sales figures.
This performance probably indicates lack of product knowledge and offer sales techniques.


**3. TIME FRAME ANALYSIS**

— Profit Trend and MOM growth rate

This line chart breaks down the Profit margin across the months in the year.

The labels represents the MOM growth rate.
 <p align="center">
  <a href="">
    <img src="https://miro.medium.com/v2/resize:fit:1100/format:webp/1*ScvJ27rRmn4yLBuBJyDwOQ.png">
  </a>

- The profit trend shows a cyclical pattern with periods of growth and decline throughout the year.

- There are two significant peaks in profit: one in March and the other in August.

- The lowest point in profit occurred in July.

The fluctuation in profit margin indictate a need for further review marketing and sales strategies to detect the main cause of the cyclical pattern.

- **Profit By Weekdays**

The area chart details the profit generated across different weekdays. It shows a clear pattern of peak profit days and relatively consistent days.
 <p align="center">
  <a href="">
    <img src="https://miro.medium.com/v2/resize:fit:1100/format:webp/1*O7lUMEO5nYY1ugw96p-w4Q.png">
  </a>

**Key Observations:**
- Peak Profit Days: Thursday and Saturday stand out as the days with the highest profit.
- Consistent Profit Days: Monday, Tuesday, Wednesday, and Sunday exhibit a relatively stable level of profit.
- Profit Dip: A noticeable dip in profit occurs on Friday.

This chart helps in understanding customer behavior.

**4. PRODUCT DETAILS**

- Products Sold - 100

- Product Return Rate - 8.03%

- **Most Profitable Products**

This visual shows the best performing products by Profit and Quantity. It gives users the flexiblility of toggling between the metrics highlighting the top products.
 <p align="center">
  <a href="">
    <img src="https://miro.medium.com/v2/resize:fit:1100/format:webp/1*4yr-nwyG24wW-0h3X-DErQ.png">
  </a>

- Begin Brew is the most profitable product, significantly outperforming the others.

- Common Splash, Onto Dew, Eight Brew, and Attorney Mist follow closely behind, forming a group of consistently profitable products.

- **Top Selling Products**
 <p align="center">
  <a href="">
    <img src="https://miro.medium.com/v2/resize:fit:1100/format:webp/1*IVqJKeQFp_GMpwhtkmvF_w.png">
  </a>

- Begin Brew is the best-selling product, with 6,861 units sold.

- The remaining four products have relatively similar sales volumes, ranging from 6,137 to 6,671 units.

These top selling products indicates strong customer preference and behavior.

It was also observed that the top selling products were also the most profitable products indicating strong correlation between quantity sold and profit made.

- **Profit By Product category**

The chart displays the profit generated by different product categories.
 <p align="center">
  <a href="">
    <img src="https://miro.medium.com/v2/resize:fit:1100/format:webp/1*pkD-n2pfTNMWjKz2h0DqPA.png">
  </a>

- Soft Drinks are the most profitable product category, generating $718K in profit.

- Sports Drinks and Tea follow closely behind, with $417K and $367K in profit, respectively.

- Water is the third most profitable category, generating $339K in profit.

- Energy Drinks and Coffee have moderate profit levels, at $174K and $142K, respectively.

- Alcoholic Beverages and Juice are the least profitable categories, with $86K and $52K in profit, respectively.

## DASHBOARD LINK
https://project.novypro.com/rxlqaa

## RECOMMENDATIONS

**1. Optimize Location Performance:** Analyze sales strategies in Washington and replicate successful tactics in underperforming locations like Missouri.
Offer location-specific promotions or events to boost foot traffic and engagement in underperforming regions.
Conduct a detailed evaluation of inventory, customer preferences, and competition in the lower-performing areas.

**2. Address Product Return Rate (8.03%):** The product return rate is relatively high. The following should be done to address that:
- An investigation of common reasons for returns by collecting customer feedback should be conducted.
- Improvement of product descriptions, quality control, and customer service to reduce dissatisfaction.
- A targeted satisfaction guarantee or product replacement program should be introduced.

**3. Leverage High-Performing Products:** The top 5 selling products (e.g., Begin Brew, Common Splash) are driving significant revenue. There is a need to:
- Expand inventory for these products in high-demand locations to avoid stockouts.
- These high selling products indicate strong customer preference so there should be marketing campaigns through promotions, bundle offers, or loyalty programs.
- Analyze customer demographics purchasing these items and tailor messaging to similar segments.

**4. Focus on Age Group Preferences:** Customers aged 21–40 and 41–60 are the highest contributors to profit. Since we understand the customer age group most interested in our products, we can leverage this information to draw in new customers from these age brackets by:

- Creating age-targeted promotions, such as discounts or rewards programs tailored to these segments.
- Expanding product offerings that cater to these age groups’ preferences and lifestyles.

**5. Refine Category-Level Strategies**

- Soft drinks generated the highest profit, while categories like juice and alcoholic beverages are less profitable.
- Expand marketing and inventory focus on soft drinks and other high-performing categories like sports drinks and tea.
- For less profitable categories, evaluate inventory levels, pricing strategies, and customer demand to avoid overstocking and wastage.

**6. Improve Weekday Profitability:**

- Profitability varies by weekday, with Tuesday and Thursday performing better.
- Implement targeted campaigns like “Weekend Specials” to attract customers on lower-performing days like Friday and Sunday.
- Offer weekday-exclusive deals or discounts to encourage more purchases during slower weekdays.

**7. Improve MoM Growth Consistency:** MoM growth shows fluctuations, with significant drops in certain months like September, July and December.

- Align campaigns and inventory management with seasonal trends to stabilize growth.
- A further analysis can be done for these periods of decline to identify potential causes like seasonality using historical data, point out operational inefficiencies.

## CONCLUSION

In conclusion, the Buam Business Dashboard reveals critical insights that can help the company overcome stagnant sales growth and unlock its true potential. By addressing cyclical sales dips with targeted promotions, enhancing customer engagement through loyalty programs, and optimizing inventory for underperforming categories, Buam can strengthen its revenue streams and improve overall efficiency.

Furthermore, focusing on underperforming regions with tailored marketing strategies while maintaining momentum in top-performing locations will enable the company to achieve balanced growth across its operations.

With these data-driven recommendations, Buam is well-positioned to transform insights into action, fostering sustainable growth and solidifying its reputation as a customer-focused retail leader.
