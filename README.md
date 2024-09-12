# Products_Customers

## Table of Contents

- [Project Overview](#project-overview)
- [Tools](#tools)
- [Data Preparation](#data-preparation)
- [Explaratory Data Analysis](#explaratory-data-analysis)
- [Data Analysis](#data-analysis)


### Project Overview 
---

- The report provides insights about customers and products
![1](https://github.com/user-attachments/assets/9b7fc08a-dadb-4ffc-b019-41129f88c363)
![2](https://github.com/user-attachments/assets/2f008166-82f7-438e-9266-2ea7432372d7)
![3](https://github.com/user-attachments/assets/4c2285f1-7d88-408d-84e2-a04f48859662)


### Tools
---

- Data Source - Excel [Download Here](https://www.microsoft.com/en-us/microsoft-365/p/excel-home-and-student/CFQ7TTC0HLKR?activetab=pivot:overviewtab)

- Data Visualization - PowerBI [Download here](https://dev.mysql.com/downloads/workbench/)
  

### Data Preparation
---

The initial data took several tasks to elaborate

1) Data Loading and inspection
2) Clearing off **extra null values**
3) Establishing relationships between tables.
4) Added columns to enable more advanced DAX calculations.
5) DAX calculations
6) Built concise and perceptible visuals


### Explaratory Data Analysis 
---

EDA involved in the following report to answer key questions, such as:

- **Gender Distribution**

- **Grouping Customers in age groups**

- **Top Customers and Highest sold Products** 

- **Popular Weekdays by sales**

- **Revenue by Country and Categories**


  ### Data Analysis
---

Data Analysis featured following syntaxes:

To calculate ages
```dax
Table.AddColumn(#"Removed Columns3", "Age", each Date.From(DateTime.Date(2020,01,01)) - [Birth date], type duration)
```

To group by ages
```dax
Table.AddColumn(#"Renamed Columns", "Age Group", each if [Age] < 18 then "< 18" else if [Age] < 25 then "18 to 24" else if [Age] < 35 then "24 to 34" else if [Age] < 45 then "34 to 45" else if [Age] < 55 then "45 to 55" else if [Age] < 65 then "55 to 64" else if [Age] > 64 then 64 else null)
```


### Results/Findings
---

The analysis are as follows:

- Genders are relatively close to one another.
- Population under age 18 most frequently visit doctors.
- Mondays are most visited days for doctors. we can conclude it is due to starting of the week.
- Hospitals in cities are visited according to the population of each city.


