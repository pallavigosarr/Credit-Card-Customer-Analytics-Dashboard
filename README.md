# Credit_Card_Transaction_Analysis
A dynamic financial dashboard designed to provide real-time, actionable insights into credit card operations, transaction patterns, and customer demographics. This project enables financial stakeholders to effectively monitor key performance indicators (KPIs), track revenue streams, and analyze consumer spending behavior.

## 📊 Dashboard Previews
### 1. Credit Card Transaction Report
> Focuses on operational metrics, revenue streams, and transactional trends.
* **Key Metrics:** Revenue, Total Interest, Transaction Amount, At Risk Revenue, Transaction Frequency, Profit
* **Granular Views:** Analysis by quarter, gender, card type (Blue, Silver, Gold, Platinum), and expense category (Bills, Entertainment, Fuel, Grocery, Food, Travel), Relation between revolving balance and utilization ratio, Revenue trend, WOW revenue growth %
* **Drill Though:** Expense Type baars are drilled through Analysis showing type of payment method used among( Online, Swipe and Chip) based on age group.
* **Page Navigation:** Button navigated to Decomposition Tree showing analysis of Total Revolving Balance
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
*	Blue card category customers are highest revenue contributors (83.49%).
*	Swipe method is highest used method among the total transactions volume (66.93%).
*	Looking at the revenue trend we can see, revenue has gone up in months, January, April, July, October, December. July is the highest contributing month showing total revenue of INR 5.65 million and March is the lowest contributing month with total revenue of INR 4.2 million. Analysis is required here to find the reason.
*	Week 53rd shows, highest WOW revenue growth %, i.e. 28.8%. Further analysis is required to find the reason.
*	At Risk Revenue of 3 Million shows, the revenue amount having delinquent_Acc =1 which can turned to be risky in future and needs to be monitored.
*	Top revenue is contributed by client_num 920819113 from Medium income group having satisfaction score of 4 having occupation as Govt. 
*	Bank has 5987 female customers and 4306 male customers.
*	Among, transaction carried out, satisfaction score 3 is major contributor. 
*	4188 customers have above average satisfaction score (4 and 5). 
*	Out of total capacity of INR 8642, revolving balance is INR 1164, which is ~13%.
*	Low income group contributes more to revenue and Businessmen are mong highest contributor according to occupation. Bank should focus more on marketing to get more revenue from high income group.
*	Age group of 46+ contributes 55.28% and age group 36-45 contributes 36.31% to revenue. Bank should pay attention on age group 26-35 by conducting surveys to understand their demands and should give discounts and offers to increase their contribution.
*	We have 568 blue card customers with delinquent_acc value of 1 and total revolving balance of 6.36 lacs. They need to be paid attention to.
*	Out of total customer acquisition cost spent, 74.3% amount is where customers have not activated the card within 30 days. Bank should take follow ups so customers activate the card within 30 days.
*	Customers majorly contribute to revenue by using credit card for Bill payments.
*	High Average utilization ratio and high average total revolving balance for Gold card with Delinquent_Acc value of 1 in Week 34 shows, customers have missed payment schedule and have used major portion of their credit limit. 

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
├── dashboard/
│   └── Online_Retail_Store.pbix
│
├── presentation/
│   └── Online_Retail_Data_Analysis.mp4
│
├── Certificate/
│   └── Tata_Internship_certificate.pdf
│
└── README.md
```


