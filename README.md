# Credit_Card_Transaction and-Customer_Analysis using Power BI

💳 Credit Card Financial Analysis & Risk Engine
Impact: Developed an end-to-end Power BI & SQL solution to analyze $57M in revenue, identifying a 28.8% WoW growth spike and a 6.06% delinquency risk across customer segments.

🎯 Business Challenge
The goal was to move from static, manual reporting to a dynamic dashboard that tracks real-time KPIs for a credit card provider. Stakeholders needed to understand revenue drivers, customer demographics, and financial risk (delinquency) to optimize marketing spend and credit limits.

🛠️ Tech Stack & Skills
Database: PostgreSQL (ETL & Data Cleaning)
Visualization: Power BI Desktop
DAX: Time Intelligence, Measures, and Calculated Columns
Data Modeling: Star Schema (Fact & Dimension tables)

🚀 Key Technical Implementation
1. SQL Data Transformation
I used SQL to clean and prepare the raw transaction data before importing it into Power BI.
2. Advanced DAX Measures
To track performance dynamically, I developed custom DAX formulas:
Current Week Revenue: Current_Week_Revenue = CALCULATE(SUM('cc_detail'[Revenue]), FILTER(ALL('cc_detail'), 'cc_detail'[Week_Num2] = MAX('cc_detail'[Week_Num2])))
WoW Revenue Growth: Calculated the 28.8% increase by comparing Current vs. Previous week metrics.

📊 Strategic Business Insights
Revenue Concentration: 93% of transaction volume is driven by Blue & Silver card tiers, suggesting a massive opportunity for upselling to Gold/Platinum.
High-Value Segments: Graduates and Business professionals contribute $37M to the total revenue.

Risk Mitigation: Identified that Self-employed individuals are most likely to be delinquent (6.06% overall rate). I recommended a targeted risk-scoring model for this segment.
Geographic Focus: TX, NY, and CA contribute 68% of total revenue.

📈 Dashboard Preview


**🔗 [Live Dashboard](https://app.powerbi.com/links/S7wsCdJhc4?ctid=c6e549b3-5f45-4032-aae9-d4244dc5b2c4&pbi_source=linkShare&bookmarkGuid=a131ec29-5c07-4fb3-b422-ed51f19c0444)**

**Steps Followed:**

1. **Data Collection**: Collected credit card data to serve as the foundation for a thorough analysis.
2. **Data Cleaning**: Ensured the data's accuracy and reliability by carefully cleaning and validating it using Excel and Postgre SQl.
3. **Data Modeling**: Created a strong data model to establish effective relationships between different data sets.
4. **Power Query**: Used Power Query in Power BI to transform raw data into meaningful insights.
5. **DAX (Data Analysis Expressions)**: Utilized DAX to perform calculations and derive valuable insights from the data.
6. **Measures**: Developed customized measures and calculations to uncover trends and patterns.
7. **Charts**: Created visually engaging charts that clearly represent complex store data.
8. **Filters**: Applied filters and slicers to allow users to explore data based on specific criteria.

**WoW change:**
- Revenue increased by 28.8%,
- Total Transaction Amt & Count increased by 25.95% & 3.28%
- Customer count increased by 11.35%

**Useful Insights:**
- Overall revenue is 56.5M
- Total interest is 8M
- Total transaction amount is 46M
- Male customers are contributing more in revenue 31M, female 26M
- Blue & Silver credit card are contributing to 93% of overall transactions
- TX, NY & CA is contributing to 68%
- Overall Activation rate is 57.5%
- Overall Delinquent rate is 6.06%

-> Next Steps/Recommendation: 
After analyzing the data, it is observed that businessmen and self-employed individuals are more likely to be delinquent. It's important to investigate the underlying reasons for this trend.
