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

Current Week Revenue: Current_Week_Revenue = 
CALCULATE(
    SUM('cc_detail'[Revenue]), 
    FILTER(
        ALL('cc_detail'), 
        'cc_detail'[Week_Num2] = MAX('cc_detail'[Week_Num2])
    )
)

Previous Week Revenue:Previous_Week_Revenue = 
CALCULATE(
    SUM('cc_detail'[Revenue]), 
    FILTER(
        ALL('cc_detail'), 
        'cc_detail'[Week_Num2] = MAX('cc_detail'[Week_Num2]) - 1
    )
    
Week-over-Week (WoW) Revenue Growth:WoW_Revenue_Growth = 
DIVIDE(
    ([Current_Week_Revenue] - [Previous_Week_Revenue]), 
    [Previous_Week_Revenue], 
    0
)

WoW Revenue Growth: Calculated the 28.8% increase by comparing Current vs. Previous week metrics.

📊 Strategic Business Insights

Revenue Concentration: 93% of transaction volume is driven by Blue & Silver card tiers, suggesting a massive opportunity for upselling to Gold/Platinum.
High-Value Segments: Graduates and Business professionals contribute $37M to the total revenue.

Risk Mitigation: Identified that Self-employed individuals are most likely to be delinquent (6.06% overall rate). I recommended a targeted risk-scoring model for this segment.
Geographic Focus: TX, NY, and CA contribute 68% of total revenue.

📈 Dashboard Preview


**🔗 [Live Dashboard](https://app.powerbi.com/links/S7wsCdJhc4?ctid=c6e549b3-5f45-4032-aae9-d4244dc5b2c4&pbi_source=linkShare&bookmarkGuid=a131ec29-5c07-4fb3-b422-ed51f19c0444)**


