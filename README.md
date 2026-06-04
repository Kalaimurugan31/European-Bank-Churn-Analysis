PHASE 1 — OPEN & PREPARE DATA
Step 1 — Open Dataset
1.	Open Excel 
2.	Open your CSV/Excel dataset 
3.	Save file as: 
Bank_Churn_Project.xlsx
________________________________________
Step 2 — Convert to Table
1.	Select all data 
2.	Press: 
Ctrl + A
Then:
Ctrl + T
3.	Tick: 
My table has headers
4.	Click: 
OK
________________________________________
PHASE 2 — DATA CLEANING
Step 3 — Check Blank Cells
1.	Select dataset 
2.	Go to: 
Home → Find & Select → Go To Special
3.	Select: 
Blanks
4.	Click: 
OK
If Excel says:
No cells were found
Your data has no blanks.
________________________________________
Step 4 — Check Duplicate Rows
1.	Select dataset 
2.	Go to: 
Data → Remove Duplicates
3.	Click: 
OK
________________________________________
Step 5 — Validate Important Columns
These columns should contain only:
Column	Correct Values
HasCrCard	0 or 1
IsActiveMember	0 or 1
Exited	0 or 1
Use filter dropdown to verify.
________________________________________
Step 6 — Check Numeric Columns
Verify:
•	Age 
•	Balance 
•	Salary 
•	CreditScore 
No:
•	Negative balances 
•	Wrong ages 
•	Text in numeric columns 
________________________________________
PHASE 3 — CREATE NEW ANALYSIS COLUMNS
Step 7 — Create Engagement Category
Add new column:
Engagement Category
Formula:
=IF(AND(L2=1,J2>=2),"Highly Engaged",
IF(AND(L2=0,I2>100000),"High Value Risk",
IF(L2=0,"Disengaged","Moderate")))
Then:
•	Press Enter 
•	Double-click formula corner to apply all rows 
________________________________________
Step 8 — Create Relationship Score
Add new column:
Relationship Score
Formula:
=L2*2 + IF(J2>=2,2,0) + K2 + IF(I2>50000,1,0)
________________________________________
Step 9 — Create RiskLevel
Add new column:
RiskLevel
Formula:
=IF(P2>=5,"Low Risk",
IF(P2>=3,"Medium Risk","High Risk"))
________________________________________
PHASE 4 — KPI CREATION
Step 10 — Create KPI Sheet
Create new sheet:
KPIs
________________________________________
Step 11 — Total Customers
Formula:
=COUNTA(B:B)-1
________________________________________
Step 12 — Churn Rate
Formula:
=COUNTIF(N:N,1)/(COUNTA(N:N)-1)
Format as percentage.
________________________________________
Step 13 — Active Customer %
Formula:
=COUNTIF(L:L,1)/(COUNTA(L:L)-1)
________________________________________
Step 14 — Credit Card Ownership %
Formula:
=COUNTIF(K:K,1)/(COUNTA(K:K)-1)
________________________________________
PHASE 5 — PIVOT TABLE ANALYSIS
Step 15 — Create Pivot Table
1.	Select data 
2.	Go to: 
Insert → Pivot Table
3.	Select: 
New Worksheet
________________________________________
Pivot Table 1 — Churn by Activity
Rows:
IsActiveMember
Values:
Average of Exited
Insight:
•	Inactive customers churn more. 
________________________________________
Pivot Table 2 — Churn by Product Count
Rows:
NumOfProducts
Values:
Average of Exited
Insight:
•	Multi-product customers stay longer. 
________________________________________
Pivot Table 3 — Geography Analysis
Rows:
Geography
Values:
Average of Exited
Average of Balance
________________________________________
Pivot Table 4 — Engagement Analysis
Rows:
EngagementCategory
Values:
Count of CustomerId
Average of Exited
________________________________________
PHASE 6 — DASHBOARD CREATION
Step 16 — Create Dashboard Sheet
Create new sheet:
Dashboard
________________________________________
Step 17 — Add KPI Cards
Create cards for:
•	Total Customers 
•	Churn Rate 
•	Active Customers 
•	Avg Balance 
•	High-Risk Customers 
________________________________________
Step 18 — Insert Charts
Recommended Charts
Chart	Type
Churn by Product Count	Bar Chart
Geography vs Churn	Column Chart
Active vs Inactive	Pie Chart
Engagement Category	Doughnut Chart
Balance vs Churn	Scatter Plot
________________________________________
Step 19 — Add Slicers (Optional)
1.	Click pivot table 
2.	Go to: 
PivotTable Analyze → Insert Slicer
Choose:
•	Geography 
•	Gender 
•	RiskLevel 
________________________________________
PHASE 7 — INSIGHTS
Step 20 — Write Insights
Examples:
Insight 1
Inactive customers exhibit significantly higher churn rates.
Insight 2
Customers with multiple banking products demonstrate stronger retention.
Insight 3
High-balance inactive customers represent silent churn risk.
Insight 4
Credit card ownership improves customer stickiness.
________________________________________
PHASE 8 — RECOMMENDATIONS
Step 21 — Write Recommendations
Examples:
•	Improve engagement campaigns 
•	Cross-sell additional products 
•	Monitor inactive premium customers 
•	Create loyalty reward programs 
•	Increase digital banking interaction 
________________________________________
PHASE 9 — FINAL REPORT
Step 22 — Create Report in Word
Structure
1. Introduction
Explain project objective.
2. Dataset Description
Explain columns.
3. Methodology
Explain formulas, pivots, KPIs.
4. Analysis
Insert charts and findings.
5. Insights
Business observations.
6. Recommendations
Retention strategies.
7. Conclusion
Final summary.
________________________________________
FINAL FILES TO SUBMIT
File	Format
Excel Analysis	.xlsx
Dashboard	Excel / Power BI
Research Report	PDF/Word
PPT (optional)	.pptx
________________________________________
MAIN GOAL OF YOUR PROJECT
Customer Engagement
        +
Product Usage
        +
Relationship Strength
        ↓
Customer Retention Analysis
This is the same type of work done in:
•	Banking analytics 
•	Financial analyst roles 
•	Business intelligence 
•	Customer retention teams 

