# **Superstore Dashboard Project**
### **Tableau Link**
[View the Dashboard on Tableau Public](https://public.tableau.com/views/SuperstoreDash_17336851771920/ProfitCentersbyGeographyandCategory?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)


## **Overview**
This Tableau dashboard analyzes the profitability and performance trends of a superstore across various dimensions, providing actionable insights for strategic decision-making. The key focus areas include:

- **Top and bottom profit centers** by category, region, and product.
- **Products at risk** due to low profitability or high return rates.
- **Subcategories’ performance** in terms of profit versus sales.
- **Average profit vs. return rate** for products and regions.
- **Profit and ad spend by state** to identify advertising opportunities.
- **Advertising ROI (ROAS)** by state to optimize future marketing strategies.
  
---

## **Key Objectives**
1. **Identify profit opportunities**:
   - Highlight categories and regions with the highest and lowest profitability.
2. **Evaluate return rate impact**:
   - Identify products and categories with high return rates to mitigate financial losses.
3. **Assess advertising feasibility**:
   - Identify states and months offering the best return on ad spend (ROAS).

---

## **Dashboard Features**

### **1. Top/Bottom Profit Centers**
- **Bar Charts**:
  - Display the top 2 and bottom 2 profit centers for combinations such as:
    - **Shipping Mode + Product ID**
    - **Subcategory + Region**
  - Help identify areas of high and low profitability.

### **2. Subcategories: Profit vs. Sales**
- **Scatter Plot**:
  - Visualizes the relationship between profit and sales for each subcategory.
  - Highlights subcategories like **Tables** with high sales but low profits for further analysis.

### **3. Products at Risk**
- **Table Visualization**:
  - Lists products with the lowest profitability.
  - Includes a heatmap to highlight products with significant losses, aiding in decision-making.

### **4. Profit and Ad Spend by State**
- **Map Visualization**:
  - Shows state-level profit and advertising spend allocations.
  - Identifies states like **California** and **New York** with high ROAS for targeted advertising.

### **5. Advertising ROI (ROAS)**
- **Map Visualization**:
  - Displays ROI metrics for each state to optimize marketing efforts.
  - Prioritizes high ROAS states for advertising investments.

### **6. Average Profit vs. Return Rate**
- **Bubble Chart**:
  - Plots regions, categories, or subcategories based on their average profit and return rate.
  - Highlights areas with high return rates negatively impacting profits.

### **7. Return Rate by Hierarchy**
- **Treemap Visualization**:
  - Organizes data hierarchically by category, product name, and customer name.
  - Visualizes % return rate with larger, darker blocks representing higher rates.
  - Allows drill-down analysis from categories to individual customers.

---

## **Data Used**

1. **Orders Table**:
   - Includes sales, profit, product, category, and subcategory details..
2. **Returns Table**:
   - Tracks returned products to calculate return rates.
3. **People Data**:
   - Name of Regional Manager and Region.

---

## **KPIs Calculated**

1. **Return Rate**:
   - Formula:
     ```sql
     (SUM([Returned_Binary]) / COUNT([Order ID]))*100
     ```
   - Measures the % of returned products to total orders.

2. **Advertising Spend**:
   - Formula:
     ```sql
     Profit * 0.2
     ```
   - Calculates the advertising budget as 20% of profit.

3. **ROAS (Return on Ad Spend)**:
   - Formula:
     ```sql
     Profit / Ad Spend
     ```
   - Evaluates the return generated per dollar spent on advertising.

---

## **Insights & Recommendations**

### **1. Top Profit Centers**
- Subcategories like **Copiers** (West region) and **Phones** (Central region) are highly profitable.
- Scaling these areas could significantly increase revenue.

### **2. Products to Eliminate**
- Products like **GBC DocuBind P400 Electric Binding System** have high losses and should be discontinued.

### **3. Advertising Opportunities**
- States like **California**, **New York**, and **Washington** show the highest ROAS, making them top priorities for marketing efforts.

### **4. Underperforming Subcategories**
- Subcategories like **Tables** and **Bookcases** with high return rates and low profitability require cost optimization or pricing adjustments.

---

## **How to Navigate the Dashboard**

1. **Top/Bottom Profit Centers**:
   - Explore profitability by selecting different categories and regions.
2. **Subcategories: Profit vs. Sales**:
   - Hover over scatter plot points to view detailed performance metrics.
3. **Products at Risk**:
   - Use filters to identify and evaluate specific products.
4. **Profit and ROAS by State**:
   - Click on states to drill down into profitability and ROAS metrics.
5. **Return Rate Hierarchy**:
   - Drill down from category to product to customer to analyze return trends.

