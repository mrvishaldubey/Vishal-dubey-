# Power BI Dashboard Layout Guide

## Overview
This document provides a recommended layout and structure for the Super Sales Store Dashboard in Power BI. The dashboard is organized into four focused pages, each serving a specific analytical purpose.

---

## Page 1: Sales Overview

**Purpose**: Provide a high-level summary of key business metrics and overall performance.

### Layout Structure

**Top Section - KPI Cards** (Horizontal row across the top)
- **Total Sales** 
  - Visual: Card
  - Format: Currency ($)
  - Color: Blue gradient
  
- **Total Profit**
  - Visual: Card
  - Format: Currency ($)
  - Color: Green gradient
  
- **Total Orders**
  - Visual: Card
  - Format: Number
  - Color: Orange gradient
  
- **Profit Margin %**
  - Visual: Card
  - Format: Percentage (%)
  - Color: Purple gradient
  
- **Average Order Value**
  - Visual: Card
  - Format: Currency ($)
  - Color: Teal gradient

**Left Section** (40% width)
- **Sales Trend**
  - Visual: Line chart or Area chart
  - X-Axis: Order Date (by Month/Quarter)
  - Y-Axis: Total Sales
  - Legend: Optional (Year)
  - Tooltip: Total Profit, Total Orders
  
- **Sales by Region**
  - Visual: Donut chart or Pie chart
  - Values: Total Sales
  - Legend: Region
  - Data labels: Percentage

**Right Section** (60% width)
- **Sales by Category**
  - Visual: Clustered bar chart
  - Y-Axis: Product Category
  - X-Axis: Total Sales
  - Color: By Category
  - Sort: Descending by Total Sales
  
- **Monthly Revenue vs Profit**
  - Visual: Clustered column chart (Combo chart)
  - X-Axis: Month
  - Y-Axis (Primary): Total Sales (Columns)
  - Y-Axis (Secondary): Total Profit (Line)
  - Colors: Blue for Sales, Green for Profit

**Bottom Section - Slicers** (Horizontal row)
- Date Range Slicer (Between style)
- Region Slicer (Dropdown)
- Category Slicer (Dropdown)
- Payment Method Slicer (Dropdown)

---

## Page 2: Regional Analysis

**Purpose**: Deep dive into geographic performance and regional trends.

### Layout Structure

**Top Section - Regional KPIs** (4 cards)
- North Region Sales
- South Region Sales
- East Region Sales
- West Region Sales

**Left Section**
- **Sales by Region Map**
  - Visual: Filled Map or Shape Map
  - Location: State
  - Values: Total Sales
  - Tooltips: Total Profit, Total Orders, Profit Margin %
  
- **Regional Sales Trend**
  - Visual: Line chart
  - X-Axis: Order Date (Monthly)
  - Y-Axis: Total Sales
  - Legend: Region
  - Multiple lines showing trends for each region

**Right Section**
- **Top 10 States by Sales**
  - Visual: Clustered bar chart
  - Y-Axis: State
  - X-Axis: Total Sales
  - Color: By Region
  - Sort: Top 10
  
- **Regional Performance Table**
  - Visual: Table or Matrix
  - Rows: Region, State
  - Columns: Total Sales, Total Profit, Total Orders, Profit Margin %
  - Conditional formatting: Color scales on Profit Margin %

**Bottom Section**
- **Sales by Payment Method (by Region)**
  - Visual: Stacked bar chart
  - Y-Axis: Region
  - X-Axis: Total Sales
  - Legend: Payment Method

**Slicers**
- Region (List)
- Date Range (Between)

---

## Page 3: Product Performance

**Purpose**: Analyze product categories, individual products, and inventory insights.

### Layout Structure

**Top Section - Product KPIs** (Cards)
- Unique Products
- Total Quantity Sold
- Average Quantity per Order
- Top Product Sales

**Left Section**
- **Top 10 Products by Sales**
  - Visual: Horizontal bar chart
  - Y-Axis: Product Name
  - X-Axis: Total Sales
  - Color: By Category
  - Data labels: Sales values
  
- **Product Category Distribution**
  - Visual: Treemap
  - Group: Product Category
  - Values: Total Sales
  - Tooltips: Total Profit, Total Orders

**Center Section**
- **Sales by Category Over Time**
  - Visual: Stacked area chart
  - X-Axis: Order Date (Monthly)
  - Y-Axis: Total Sales
  - Legend: Product Category
  
- **Category Profit Analysis**
  - Visual: Clustered column chart
  - X-Axis: Product Category
  - Y-Axis: Total Profit and Total Sales
  - Legend: Measure (Sales/Profit)

**Right Section**
- **Product Performance Table**
  - Visual: Table
  - Columns: Product Name, Category, Total Sales, Total Profit, Quantity, Profit Margin %
  - Sort: By Total Sales (Descending)
  - Conditional formatting: Highlight high performers
  
- **Average Price by Category**
  - Visual: Column chart
  - X-Axis: Product Category
  - Y-Axis: Average Unit Price

**Slicers**
- Product Category (Tile or List)
- Date Range (Between)
- Region (Dropdown)

---

## Page 4: Customer Insights

**Purpose**: Understand customer behavior, preferences, and transaction patterns.

### Layout Structure

**Top Section - Customer KPIs** (Cards)
- Unique Customers
- Average Sales per Customer
- Orders per Customer
- Repeat Customer Rate

**Left Section**
- **Top 10 Customers by Sales**
  - Visual: Horizontal bar chart
  - Y-Axis: Customer Name
  - X-Axis: Total Sales
  - Color: Gradient based on sales value
  - Data labels: Visible
  
- **Customer Purchase Frequency**
  - Visual: Column chart
  - X-Axis: Number of Orders (buckets: 1, 2-3, 4-5, 6+)
  - Y-Axis: Number of Customers
  - Color: Single color

**Center Section**
- **Sales by Payment Method**
  - Visual: Pie chart or Donut chart
  - Values: Total Sales
  - Legend: Payment Method
  - Data labels: Percentage and Value
  
- **Digital vs Cash Payments Trend**
  - Visual: Line chart
  - X-Axis: Order Date (Monthly)
  - Y-Axis: Percentage of Sales
  - Legend: Payment Type (Digital/Cash)

**Right Section**
- **Customer Transaction Details**
  - Visual: Table
  - Columns: Customer Name, Total Sales, Total Orders, Average Order Value, Last Order Date
  - Sort: By Total Sales
  - Conditional formatting: Gradient on Total Sales
  
- **Sales by Sales Person**
  - Visual: Funnel chart or Bar chart
  - Y-Axis: Sales Person
  - X-Axis: Total Sales
  - Sort: Descending

**Bottom Section**
- **Customer Segmentation by Order Value**
  - Visual: Scatter chart
  - X-Axis: Total Orders
  - Y-Axis: Average Order Value
  - Size: Total Sales
  - Details: Customer Name

**Slicers**
- Payment Method (Tile)
- Date Range (Between)
- Region (Dropdown)

---

## Design Guidelines

### Color Scheme
**Primary Colors:**
- Blue (#0078D4) - Sales metrics
- Green (#107C10) - Profit metrics
- Orange (#D83B01) - Orders/Quantity
- Purple (#5C2D91) - Margins/Percentages
- Teal (#008272) - Averages

**Secondary Colors:**
- Light Gray (#F3F2F1) - Backgrounds
- Dark Gray (#323130) - Text
- White (#FFFFFF) - Cards and visual backgrounds

### Typography
- **Title Font**: Segoe UI Semibold, 14-16pt
- **Visual Titles**: Segoe UI, 12pt
- **Data Labels**: Segoe UI, 9-10pt
- **KPI Values**: Segoe UI Bold, 24-32pt

### Visual Formatting Standards

1. **Cards**
   - Background: White with subtle shadow
   - Border: 1px light gray
   - Padding: 10px
   - Value: Large, bold, colored
   - Label: Small, gray, below value

2. **Charts**
   - Grid lines: Light gray, minimal
   - Axis labels: Dark gray, 10pt
   - Data labels: Show for top values only
   - Legend: Bottom or right, depending on visual
   - Tooltips: Enabled with relevant metrics

3. **Tables**
   - Header: Dark background, white text
   - Alternating rows: Light gray
   - Borders: Subtle, light gray
   - Conditional formatting: Color scales or data bars

4. **Slicers**
   - Style: Tile or Dropdown based on space
   - Background: Light gray
   - Selected: Primary color highlight
   - Font: Segoe UI, 10pt

### Interaction Settings

1. **Cross-Filtering**
   - Enable cross-filtering between visuals on the same page
   - Slicers should filter all relevant visuals
   - Card visuals should not filter other visuals

2. **Drill-Through**
   - Set up drill-through from overview to detail pages
   - Example: From Top Products to detailed product page

3. **Tooltips**
   - Use custom tooltip pages for rich contextual information
   - Include relevant metrics and trend indicators

### Performance Optimization

1. **Limit Visuals**: 8-12 visuals per page maximum
2. **Aggregation**: Pre-aggregate data where possible
3. **Filters**: Use page-level filters instead of visual-level when applicable
4. **Images**: Use SVG or optimized PNG for backgrounds/logos

### Responsive Design

1. **Mobile Layout**: Create optimized layouts for each page
2. **Breakpoints**: Test at different screen resolutions
3. **Priority Visuals**: Ensure key metrics visible on all devices

---

## Page Navigation

### Navigation Buttons
Add buttons to the top-left or left sidebar for easy navigation:
- 📊 Sales Overview
- 🌍 Regional Analysis
- 📦 Product Performance
- 👥 Customer Insights

Use icons and consistent styling for all navigation buttons.

### Bookmarks (Optional)
Create bookmarks for:
- Default view (all filters cleared)
- Top performers view
- Regional comparison view
- Custom saved states

---

## Additional Features

### Report Header (Optional)
Add a consistent header across all pages:
- Company logo
- Dashboard title: "Super Sales Store Dashboard"
- Last refresh time
- Navigation menu

### Branding
- Add company logo (top-left corner)
- Use company colors if applicable
- Add footer with data source and version info

### Sync Slicers
Enable slicer sync across pages for:
- Date Range
- Region
This allows users to maintain filter context when navigating between pages.

---

## Best Practices

1. **Consistency**: Use the same visual types for similar data across pages
2. **Hierarchy**: Show summary first, then details
3. **White Space**: Don't overcrowd - leave breathing room
4. **Alignment**: Align visuals to a grid for professional appearance
5. **Storytelling**: Each page should tell a clear story
6. **Testing**: Test all interactions and filters before publishing

---

## Accessibility

1. **Color Blind Friendly**: Use patterns in addition to colors
2. **Alt Text**: Add descriptive alt text to all visuals
3. **Tab Order**: Set logical tab order for keyboard navigation
4. **High Contrast**: Ensure text is readable against backgrounds

---

This layout guide provides a foundation for building an effective and professional Power BI dashboard. Customize as needed based on specific business requirements and user feedback.
