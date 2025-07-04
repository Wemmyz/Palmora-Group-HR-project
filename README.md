# Palmora-Group-HR-project
This project presents an interactive Power BI dashboard for analyzing employee data from Palmora Group. It covers gender distribution, salary structure, bonus calculations, and performance ratings across regions and departments.

## Project Overview
This HR analytics solution helps uncover insights about:
-  Salary distribution and gaps
-  Gender-based compensation analysis
-  Performance-based bonus calculations
-  Departmental and regional employee trends
  
The dashboard empowers HR teams to make informed decisions about compensation fairness, diversity, and workforce planning.

## Tools & Skills Demonstrated
•	Power BI Desktop [Download Here](https://www.microsoft.com/en-us/download/details.aspx?id=58494)
-	Data transformation & cleaning (Power Query)

-	DAX for custom metrics

-	Interactive visualizations

### Dataset
•	Source: Internal sample data from Palmora Group

•	Size: 700+ employee records

•	Fields: Name, Gender, Department, Region, Salary, Rating, etc.

### Exploratory Data Analysis
EDA involved the exploring of the Data to answer some questions about the Data such as;

- What is the gender distribution in the organization? Distil to regions and departments
   
- Show insights on ratings based on gender
  
- Analyse the company’s salary structure. Identify if there is a gender pay gap. If there is, identify the department and regions that should be the focus of management

### Key Features & Visualizations

##### 1. Gender Distribution Analysis
- Bar chart: Gender breakdown by department/region
- Pie chart: Overall gender composition
- Measures: Gender count, Gender percentage

##### 2. Rating Insights
- Rating score mapping 
- Histogram: Rating Distribution by gender
- Average rating by gender (using measures)

##### 3. Salary Structure & Gender Pay Gap Analysis
- Average salary by gender using a measure
- Scatter plot: “Salary vs Gender”
- Bar chart: Average salary by Department and region

##### 4. Minimum Salary Analysis
- Bar chart: Employee below minimum salary threshold by region
- Histogram: Salary distribution by $10,000 band

#### DAX Highlights
       
-	Average Rating Measure
Average Rating by Gender = AVERAGE ('Data bonus Merge'[Rating Score])

-	Bonus Calculation 
Bonus Amount = IF ('Data bonus Merge'[Rating Count]>3,'Data_bonus Merge'[Average salary] *0.1,0)

-	Total Compensation
Total Pay = 'Data bonus Merge'[Salary] + 'Data bonus Merge'[Bonus Amount]

- Employees Below Salary Threshold Measure
  
  Employee Below Minimum Salary = COUNTX (FILTER ('Data bonus Merge', 'Data bonus Merge'[Salary] < 90000), 'Data bonus Merge'[Salary])

##### Files Included
•	Palmora Group Project— Power BI report file

•	README.md — This documentation


![Chart 1](https://github.com/user-attachments/assets/aa6d0363-6922-4925-81b6-862a1efacef8)


![Chart](https://github.com/user-attachments/assets/dd3b808e-87a5-4104-b76a-3311a2ab3257)


