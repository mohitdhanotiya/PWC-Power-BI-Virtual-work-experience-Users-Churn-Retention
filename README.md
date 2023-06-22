# PWC Power BI Virtual work experience-Users Churn Retention

## Table of Content
- Problem Statement
- Importing Data
- Data Preparation
- Data Modelling
- DAX
- Data Visualization

### Problem Statement
The purpose of this task is to:
- Define proper KPI's
- Create a dashboard for the retention manager reflecting the KPI's
- Write a short email to him (the engagement partner) explaining your findings, and include suggestions as to what needs to be changed
- Customers who left within the last month
- Services each customer has signed up for: phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies
- Customer account information: how long as a customer, contract, payment method, paperless billing, monthly charges, total charges and number of tickets opened in the categories administrative and technical
- Demographic info about customers – gender, age range, and if they have partners and dependents

### Importing Data
The Dataset was provided by PWC Switzerland.

### Data Preparation
Dataset was loaded into Power BI , Data was tranformed and loaded in Power Query editor.
- Validation of each coloumn Data Type's
- Removing Unnecessary Row's and Column's

### Data Modelling
After the dataset was cleaned and transformed, The Data is ready for Modelling.

### DAX
- Churn Rate = CALCULATE(COUNT('01 Churn-Dataset'[customerID]),'01 Churn-Dataset'[Churn]="Yes")/COUNT('01 Churn-Dataset'[customerID])
- % churn by onlinesecurity = CALCULATE(COUNT('01 Churn-Dataset'[customerID]),'01 Churn-Dataset'[OnlineSecurity]="Yes")/COUNT('01 Churn-Dataset'[customerID])
- % churn by Paperless billing = CALCULATE(COUNT('01 Churn-Dataset'[customerID]),'01 Churn-Dataset'[PaperlessBilling]="Yes")/COUNT('01 Churn-Dataset'[Custom])
- % churn by PhoneService = CALCULATE(COUNT('01 Churn-Dataset'[customerID]),'01 Churn-Dataset'[PhoneService]="Yes")/COUNT('01 Churn-Dataset'[customerID])
- % churn by StreamingMovies = CALCULATE(COUNT('01 Churn-Dataset'[customerID]),'01 Churn-Dataset'[StreamingMovies]="Yes")/COUNT('01 Churn-Dataset'[customerID])
- % Dependents = CALCULATE(COUNT('01 Churn-Dataset'[customerID]),'01 Churn-Dataset'[Dependents]="Yes")/COUNT('01 Churn-Dataset'[customerID])
- % Partner = CALCULATE(COUNT('01 Churn-Dataset'[customerID]),'01 Churn-Dataset'[Partner]="Yes")/COUNT('01 Churn-Dataset'[customerID])

### Data Visualization
- Pie chart to show Demographics
- Stacked column chart to show churn rate by Internet services
- Area chart to show churn by Tenure
- Line and stacked column chart to show Avg monthly charges and churn rate based on payment method
- Clustered bar chart to show churn rate by Techsupport
- Pie chart to show customer distribution by contract
