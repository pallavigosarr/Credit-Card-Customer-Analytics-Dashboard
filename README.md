# Credit_Card_Transaction_Analysis
A dynamic financial dashboard designed to provide real-time, actionable insights into credit card operations, transaction patterns, and customer demographics. This project enables financial stakeholders to effectively monitor key performance indicators (KPIs), track revenue streams, and analyze consumer spending behavior.

## 📊 Dashboard Previews
### 1. Credit Card Transaction Report
> Focuses on operational metrics, revenue streams, and transactional trends.
* **Key Metrics:** Revenue, Total Interest, Transaction Amount, At Risk Revenue, Transaction Frequency, Profit
* **Granular Views:** Analysis by quarter, gender, card type (Blue, Silver, Gold, Platinum), and expense category (Bills, Entertainment, Fuel, Grocery, Food, Travel), Relation between revolving balance and utilization ratio, Revenue trend, WOW revenue growth %
* **Drill Though:** Expense Type baars are drilled through Analysis showing type of payment method used among( Online, Swipe and Chip) based on age group.
* **Page Navigation:** Button navigated to Decomposition Tree showing analysis of Total Revolving Balance
* ****Screenshot**:
<img width="892" height="498" alt="Credit_card_transaction_report" src="https://github.com/user-attachments/assets/beac8c42-9188-4eb9-a56a-6f9961c93cf8" />
<img width="650" height="401" alt="Drill_through_page" src="https://github.com/user-attachments/assets/86aada48-56e7-47bb-9e7d-90f049fcaf84" />
<img width="781" height="410" alt="Analysis_of_revolving_bal" src="https://github.com/user-attachments/assets/7dc614c9-d1c6-4427-8971-f50c98af27d7" />



### 2. Credit Card Customer Report
> Focuses on customer demographics, segmentation, and behavioral insights.
* **Key Metrics:** Total no. of customers, No. of customers with above average satisfaction score, No. of high income group customers 
* **Demographic Segmentation:** Analysis by age group,income group, gender, satisfaction score and occupation
* **Risk & Engagement:** Capacity vs Debt, Acquisition efficiency, Delinquency Risk Audit
* ****Screenshot**:
<img width="851" height="488" alt="Credit_card_customer_report" src="https://github.com/user-attachments/assets/f01fbc6d-c4a6-437b-85ca-7dd53b0e88ab" />


## Repository Structure

```text
Credit_Card_Transaction_Analysis
/
│
├── data/
│   ├── client_data.csv
│   └── price_data.csv
│   ├── clean_data_after_eda.csv
│   └── data_for_predictions.csv
│
├── Tasks-notebooks/
│   ├── Task1_Email.md
│   ├── Task2_EDA.ipynb
│   └── Task3_Ans_Feature_Engineering.ipynb
|   └── Task4_Ans_Modeling.ipynb
│
├── Executive summary/
│   └── Executive_Summary.pdf
│

