# powerbi

Assignment: Power BI Data Analysis and Visualization
Dataset Description
You are provided with a dataset containing transactional and customer information. Your goal is to analyze the data, extract insights, and present the results using Power BI. The dataset fields are as follows:
●	Date, Day, Month, Year: Transaction date details.
●	Customer_age, age_group: Age of customers and categorized age groups.
●	Customer_gender: Gender of the customers.
●	Country, State: Location details.
●	Product_category, Sub_category, Product: Product information.
●	Order_quantity: Quantity of the product ordered.
●	Unit_cost, Unit_price: Cost and price per unit of the product.
●	Profit, Cost, Revenue: Financial metrics of the transaction.

________________________________________
Tasks
Task 1: Data Preparation and Transformation
1.	Data Cleaning:
○	Remove any null or duplicate values from the dataset.
○	Ensure all column names are properly formatted (e.g., no spaces or special characters).
○	In the country column, group “USA” and “United States” as “United States” so that in the report we only see one value per Country.
2.	Data Types:
○	Verify and set appropriate data types for each column. For example:
■	Dates for the Date column.
■	Numeric types for fields like Order_quantity, Unit_cost, Revenue.
3.	Add Custom Columns: 
○	Create a calculated column for Total Cost:
Total Cost = [Order_quantity] * [Unit_cost]
○	Create a calculated column for Profit Margin (%):
 Profit Margin (%) = DIVIDE([Profit], [Revenue]) * 100


________________________________________
Task 2: Data Analysis Using DAX
1.	Create 3 Measures:
Total Revenue:
 	Total Revenue = SUM([Revenue])

Average Order Quantity:
 	Avg Order Quantity = AVERAGE([Order_quantity])

Gender-wise Profit Contribution:
	Gender Profit = 
SUMX(
FILTER(
Sales, 
Sales[Customer_gender] = "Male"
), Sales[Profit]
)
2.	Yearly Analysis:
Create a measure to calculate yearly profit:
 	Yearly Profit = SUM([Profit])

________________________________________

Task 3: Data Visualization
1.	Visuals:
○	Revenue Trends: Use a line chart to show revenue trends over months.
○	Top Products: Create a bar chart showing the top 5 products by revenue.
○	Profit by Region: Use a map visualization to display profit distribution by Country.
○	Customer Demographics: Create a pie chart to show the distribution of customers by gender and age group.

2.	Interactive Features:
○	Add slicers for Year, Product Category, and Country.
○	Disable tooltips to display detailed data on hover on above (Customer Demographics) 2 pie charts.
________________________________________
Task 4: Edit Interaction
1.	Ignore filter on a BAR chart while selecting value in Year Slicer.
________________________________________
Task 5: Insights and Recommendations
1.	Based on your analysis, answer the following:
○	Which product category generates the most profit?
○	Which age group is the most profitable?
○	How does gender influence revenue?
2.	Provide 2-3 actionable recommendations for improving business performance based on your insights.
________________________________________
Submission Guidelines
●	Format: Submit your Power BI file (.pbix).
●	Deadline: [4th January 2025]
●	Evaluation: Assignments will be graded on data accuracy, creativity in visuals, interactivity, and insights.
Assignments:
1.	CV Submit
2.	Home work 2: https://www.youtube.com/watch?v=EiIAkJ9R7mM
3.	Project
a.	Dataset: sales_data_for_powerbi_project (csv)
b.	Dataset Location: C:\powerbi_project_data
4.	Optional: analyze covid data set.

●	Report Look and Feel



Task 4: Dashboard Creation
2.	Combine Visuals:
○	Design a single-page dashboard with key insights like total revenue, profit, top products, and customer demographics.
○	Use KPIs to display Total Revenue, Total Profit, and Total Orders.
3.	Formatting:
○	Ensure the dashboard is visually appealing with consistent colors and fonts.
○	Add titles, legends, and data labels where applicable.
