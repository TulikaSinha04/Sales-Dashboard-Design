# Sales-Dashboard-Design

## Objective
Create a basic interactive dashboard that shows sales performance by product, region, and month. The dashboard should help business users quickly understand sales trends and identify top-performing regions and categories.

## Tools
Power BI Desktop 

## Dataset

File: Superstore_Sales_BI.csv

## Columns:

'Order Date' – date of the order

'Region' – region of the sale

'Category' – product category

'Sales' – sales amount

'Profit' – profit amount

## Steps to Build the Dashboard

1. Import the CSV

2. Open Power BI → Home → Get Data → Text/CSV → Select Superstore_Sales.csv.

3. Click Transform Data to open Power Query for data cleaning.

4. Convert Order Date to Month-Year
   Power Query: Add Column → Custom Column →
   = Date.ToText([Order Date], "MMM yyyy") 
   Name it MonthYear.

5. Create Measures (DAX)
Total Sales = SUM('Superstore_Sales_BI'[Sales])

6. Total Profit:
Total Profit = SUM('Superstore_Sales_BI'[Profit])

7. Profit Margin:
Profit Margin % = DIVIDE([Total Profit],[Total Sales],0)

## Add Visuals

1. Line Chart: Sales over Months
   Axis: MonthYear
   Values: Total Sales

2. Bar Chart: Sales by Region
   Axis: Region
   Values: Total Sales
   Use conditional formatting to highlight top-performing regions
   
3. Donut Chart: Sales by Category
   Legend / Details: Category
   Values: Total Sales

4. Add Slicer
   Slicer field: Region or Category

# Allows interactive filtering on all visuals.

Formatting & Labels
Enable data labels for clarity.
Add titles for each visual and a dashboard title.
Use colors strategically to highlight top regions or categories.

# Export
File → Export → Export to PDF or take a screenshot of the dashboard.

# Sample Insights
.txt

# Deliverables
Task8_power BI.pdf – export of the dashboard.
Dashoboard Summary.txt – key insights summarizing the data.




