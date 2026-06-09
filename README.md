# Credit_Card_Transaction_Analysis
A dynamic dashboard designed to provide real-time, actionable insights into credit card operations, transaction patterns, and customer demographics. This project enables financial stakeholders to effectively monitor key performance indicators (KPIs), track revenue streams, and analyze consumer spending behavior.

## 📊 Dashboard Previews
### 1. Credit Card Transaction Report
> Focuses on operational metrics, revenue streams, and transactional trends.
* **Key Metrics:** Revenue, Total Interest, Transaction Amount, At Risk Revenue, Transaction Frequency, Profit
* **Granular Views:** Analysis by quarter, gender, card type (Blue, Silver, Gold, Platinum), and expense category (Bills, Entertainment, Fuel, Grocery, Food, Travel), Relation between revolving balance and utilization ratio, Revenue trend, WOW revenue growth %
* **Drill Though:** Expense Type baars are drilled through Analysis showing type of payment method used among( Online, Swipe and Chip) based on age group.
* **Page Navigation:** Button navigated to Decomposition Tree showing analysis of Total Revolving Balance.
* **Screenshots**:
<img width="892" height="498" alt="Credit_card_transaction_report" src="https://github.com/user-attachments/assets/beac8c42-9188-4eb9-a56a-6f9961c93cf8" />
<img width="650" height="401" alt="Drill_through_page" src="https://github.com/user-attachments/assets/86aada48-56e7-47bb-9e7d-90f049fcaf84" />
<img width="781" height="410" alt="Analysis_of_revolving_bal" src="https://github.com/user-attachments/assets/7dc614c9-d1c6-4427-8971-f50c98af27d7" />



### 2. Credit Card Customer Report
> Focuses on customer demographics, segmentation, and behavioral insights.
* **Key Metrics:** Total no. of customers, No. of customers with above average satisfaction score, No. of high income group customers 
* **Demographic Segmentation:** Analysis by age group,income group, gender, satisfaction score and occupation
* **Risk & Engagement:** Capacity vs Debt, Acquisition efficiency, Delinquency Risk Audit
* **Screenshot**:
<img width="851" height="488" alt="Credit_card_customer_report" src="https://github.com/user-attachments/assets/f01fbc6d-c4a6-437b-85ca-7dd53b0e88ab" />

## 🚀 Key Insights & Findings
* Bill payment transactions emerged as the largest contributor to overall credit card revenue.
* Blue Card customers generated 83.49% of total revenue, making them the most valuable customer segment.
* Swipe transactions accounted for 66.93% of total transaction volume, indicating strong preference for traditional payment methods.
* Revenue exhibited seasonal peaks during January, April, July, October, and December, with July generating the highest revenue of ₹5.65M.
* Week 53 recorded the highest WoW Revenue Growth of 28.8%, indicating a potential promotional or seasonal impact.
* Identified high-risk customer segments with elevated credit utilization ratios and revolving balances, particularly among delinquent Gold Card customers.
* At-Risk Revenue totaled approximately ₹3M, highlighting potential exposure to future defaults.
* Customers aged 46+ contributed 55.28% of total revenue, making them the most profitable age segment.
* Low-income customers generated a significant share of revenue despite lower earning capacity, indicating strong engagement with credit products.
* Analysis revealed 568 delinquent Blue Card customers with substantial revolving balances requiring closer monitoring.
* Female customers represented the majority of the customer base, accounting for 58% of total customers.
* Nearly 74.3% of customer acquisition spending was associated with customers who did not activate their cards within 30 days.
 

## 🛠️ Tech Stack & Skills Used

* **Business Intelligence:** Microsoft Power BI Desktop
* **Database / Data Source:**  Flat CSV Files
* **Data Transformation:** Power Query (ETL process, data cleaning, custom column creation)
* **Analytical Calculations:** DAX (Data Analysis Expressions) for time-intelligence and custom KPIs

## 📈 DAX Formulas & Custom Metrics

Below are examples of the custom time-intelligence metrics created for this analysis:

Previous_week_rev = 
var maxweek= MAX(CreditCard[week_no])
RETURN
CALCULATE(
    [Total_Revenue],
    CreditCard[week_no]=maxweek-1
)

Current_week_rev = 
var Maxweek=MAX(CreditCard[week_no])
RETURN
CALCULATE([Total_Revenue], CreditCard[week_no]=Maxweek)

WoW Revenue Growth % = 
   DIVIDE(
        [Current_week_rev] - [Previous_week_rev],
        [Previous_week_rev],
        0
    )
    

## Repository Structure

```text
Credit_Card_Transaction_Analysis
/
├── Data/
│   └── CreditCard.csv
│   └── Customer.csv
|
├── Screenshots/
│   └── Credit_card_transaction_report.png
│   └── Credit_card_customer_report.png
│   └── Analysis_of_revolving_bal.png
│   └── Drill_through_page.png
│
├── Dashboard/
│   └── Credit_Card_Dashboard.pbix
│
├── Overview/
│   └── Overview.docx
│
└── README.md
```


