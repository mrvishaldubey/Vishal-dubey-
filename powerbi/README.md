# Power BI Dashboard Setup Guide

## Overview
This guide provides step-by-step instructions to create a comprehensive Super Sales Store Dashboard in Power BI using the provided sales data.

## Prerequisites
- Power BI Desktop (latest version recommended)
- Sales data file: `data/sales_data.csv`

## Setup Instructions

### Step 1: Import Data

1. **Open Power BI Desktop**
   - Launch Power BI Desktop on your computer

2. **Get Data**
   - Click on "Get Data" from the Home ribbon
   - Select "Text/CSV" from the list
   - Navigate to `data/sales_data.csv` and click "Load"

3. **Verify Data Import**
   - Check the Fields pane to ensure all columns are imported correctly
   - Review data types in the table view (Order Date should be Date type, numerical fields should be numbers)

### Step 2: Data Preparation

1. **Transform Data** (if needed)
   - Click on "Transform Data" to open Power Query Editor
   - Ensure proper data types:
     - Order Date: Date
     - Quantity: Whole Number
     - Unit Price, Total Sales, Profit, Discount: Decimal Number
   - Click "Close & Apply" when done

2. **Create Date Table** (Optional but recommended)
   ```DAX
   DateTable = 
   ADDCOLUMNS(
       CALENDAR(MIN(Sales[Order Date]), MAX(Sales[Order Date])),
       "Year", YEAR([Date]),
       "Month", FORMAT([Date], "MMMM"),
       "Month Number", MONTH([Date]),
       "Quarter", "Q" & QUARTER([Date]),
       "Year-Month", FORMAT([Date], "YYYY-MM")
   )
   ```

### Step 3: Create DAX Measures

Create calculated measures for KPIs and analytics. Go to the Modeling tab and click "New Measure" to create each of the following:

**Key Measures** (See `DAX_Measures.txt` for complete formulas):
- Total Sales
- Total Profit
- Total Orders
- Profit Margin %
- Average Order Value
- YoY Growth %
- MoM Growth %

### Step 4: Build Dashboard Visualizations

Refer to `Dashboard_Layout.md` for detailed dashboard structure.

#### Recommended Visuals:

**Page 1: Sales Overview**
- Card visuals for KPIs (Total Sales, Total Profit, Total Orders, Profit Margin %, Average Order Value)
- Line chart: Sales Trend over time
- Donut chart: Sales by Region
- Bar chart: Sales by Category
- Slicers: Date Range, Region, Category

**Page 2: Regional Analysis**
- Map visual: Sales by State/Region
- Clustered bar chart: Top States by Sales
- Line chart: Regional Sales Trend
- Table: Detailed regional performance

**Page 3: Product Performance**
- Bar chart: Top 10 Products by Sales
- Bar chart: Sales by Category
- Treemap: Product Category distribution
- Table: Product details with sales and profit

**Page 4: Customer Insights**
- Bar chart: Top 10 Customers by Sales
- Pie chart: Sales by Payment Method
- Clustered column chart: Customer purchase patterns
- Table: Customer transaction details

### Step 5: Add Interactivity

1. **Add Slicers**
   - Date Range (using Order Date)
   - Region dropdown
   - Product Category dropdown
   - Payment Method dropdown

2. **Configure Interactions**
   - Click on "Format" > "Edit Interactions"
   - Configure how visuals interact with each other
   - Ensure slicers filter all relevant visuals

3. **Add Tooltips**
   - Customize tooltips to show relevant details on hover

### Step 6: Apply Formatting

1. **Choose a Theme**
   - Go to View > Themes
   - Select a professional theme or customize your own

2. **Format Visuals**
   - Use consistent colors across all pages
   - Format numbers with proper currency symbols and decimal places
   - Add titles and labels to all visuals

3. **Add Page Navigation** (Optional)
   - Create buttons for easy navigation between pages
   - Use "Page Navigation" action for buttons

### Step 7: Save and Publish

1. **Save the Report**
   - File > Save As
   - Choose a location and name (e.g., `SuperSales_Dashboard.pbix`)

2. **Publish to Power BI Service** (Optional)
   - Click "Publish" from Home ribbon
   - Sign in to Power BI Service
   - Select a workspace to publish

## Tips for Best Results

- **Refresh Data**: Set up automatic data refresh if connecting to live data source
- **Performance**: Limit visuals per page to 10-15 for optimal performance
- **Mobile View**: Create a mobile-optimized layout for each page
- **Bookmarks**: Use bookmarks to save specific states of the dashboard
- **Drill-through**: Enable drill-through pages for detailed analysis

## Troubleshooting

**Data not loading correctly?**
- Check the file path to `sales_data.csv`
- Verify the CSV file is not open in another program
- Ensure data types are correct in Power Query

**Measures not calculating correctly?**
- Check DAX syntax for errors
- Verify table and column names match exactly
- Use DAX Studio for debugging complex formulas

**Visuals not displaying?**
- Ensure fields are dragged to correct wells (Values, Axis, Legend)
- Check if filters are applied that might hide data
- Verify data relationships if using multiple tables

## Additional Resources

- [Power BI Documentation](https://docs.microsoft.com/power-bi/)
- [DAX Function Reference](https://dax.guide/)
- [Power BI Community](https://community.powerbi.com/)

## Support

For questions or issues with this dashboard setup, please refer to the main project README.md or contact the project maintainer.
