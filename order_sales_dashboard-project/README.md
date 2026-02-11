# Order Sales Dashboard

## Objective
To provide visibility and continuous monitoring of sales performance metrics, enabling:
- Early detection of sales trends and anomalies
- Proactive identification of underperforming products/regions
- Data-driven decision support for sales operations
- Regular performance tracking against historical baselines

## Requirements
1. **Monthly Review Meetings**: Track MoM performance trends of sales revenue breakdown by product.
2. **Quarterly Business Reviews**: YoY comparisons and trend analysis against budget
3. **Weekly Ops Review**: Quick performance pulse checks of confirmed orders against expected revenues 
4. **Monthly Product Planning**: Identify top/bottom performers for inventory decisions

## Special Considerations
- Present sales revenue to compare nett sales revenue.
- Present sales quantity to compare actual volumes sold through.
  
## Tools
- Visualisation in Databricks
  
## Data Sources
- Primary table: sales_transactions
- Update frequency: Weekly/Monthly
- Historical data range: [1st Jan Year - 31 Dec Year]
  
## Key Metrics
- Net Sales Revenue: Gross sales - (Discounts + Returns) [Excluding Tax].
- Sales Quantity: Total units of inventory invoiced.
- MoM Growth Rate: (Current Month Sales - Previous Month Sales) / Previous Month Sales
- YoY Growth Rate: (Current Month Sales - Same Month Last Year Sales) / Same Month Last Year Sales

## Methodology
1. **Data Extraction:** 
   - Query sales transactions from the Databricks Lakehouse.
   - Refresh schedule: Daily/Weekly/Monthly
   
2. **Data Preparation:**
   - Note: Raw data cleaning and validation is handled upstream via ETL pipelines.
   - Aggregate daily transactions into Monthly grains.
   - Create calculated fields for YoY and MoM comparisons

3. **Dashboard Creation:** 
   - Design dashboard layout for optimum screen size
   - Implement interactive filters for date ranges and products
   
4. **Chart Elements:** 
   - Time series charts: Monthly sales trends
   - Bar charts: Product comparisons
   - Heatmaps: Sales patterns by product and time
   
5. **Final Polish:** 
   - Add consistent color scheme
   - Proper labelling of axis, legends and chart titles for clear visual storytelling.

## Dashboard Components
### 1. Annual Sales Performance
- Monthly revenue trends with YoY comparison
- Product-wise sales breakdown
- Sales heatmaps for pattern identification

### 2. Regional Analysis 
- Region-wise product distribution
- Sales representative performance
- Target vs. actual comparisons

### 3. Product Analysis
- Top performing products by revenue
- Quantity sold trends
- Product order size distribution
