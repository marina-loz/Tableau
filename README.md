# **Superstore Dashboard Project**
### **Tableau Link**
[View the Dashboard on Tableau Public](https://public.tableau.com/views/SuperstoreDash_17336851771920/ProfitCentersbyGeographyandCategory?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)


## **Overview**
This Tableau dashboard analyzes the profitability and performance trends of a superstore across various dimensions, providing actionable insights for strategic decision-making. The key focus areas include:

### **1. Top/Bottom 2 Profit Centers of Subcategory + Region**
- **Description**:
  - A **bar chart** displays the **top 2 most profitable** and **bottom 2 least profitable** subcategory and region combinations.
  - Example:
    - **Copiers | West**: High profit.
    - **Tables | East**: Significant losses.
- **Purpose**:
  - To identify regions and subcategories for scaling or optimization.

---

### **2. Subcategories: Profit vs. Sales**
- **Description**:
  - A **scatter plot** visualizes the relationship between sales and profit for each subcategory.
  - Example:
    - **Copiers**: High profit with moderate sales.
    - **Tables**: High sales but low profit.
- **Purpose**:
  - To identify subcategories requiring pricing adjustments or cost reduction.

---

### **3. Which Products Are at Risk**
- **Description**:
  - A **table with a heatmap** lists the products with the lowest profitability.
  - Example:
    - **GBC DocuBind P400 Electric Binding System**: Loss of -$20,388.
  - Color coding highlights products with significant losses.
- **Purpose**:
  - To recommend discontinuing or revising unprofitable products.

---

### **4. Top 3 State-Month Combinations**
- **Description**:
  - A **bar chart** showcases the **top 3 state-month combinations** based on average profit (Avg. Profit).
  - Additional metrics calculated:
    - **Ad Spend**: Advertising expenditures calculated as 20% of average profit.
    - **ROAS**: Return on Advertising Spend.
  - Example:
    - **Indiana | October**:
      - Average Profit: $643.1.
      - Ad Spend: $128.6.
      - ROAS: 5.
  - **Formulas**:
    - Ad Spend:
      ```plaintext
      Ad Spend = Avg. Profit * 0.2
      ```
    - ROAS:
      ```plaintext
      ROAS = Avg. Profit / Ad Spend
      ```
- **Purpose**:
  - To determine the most effective state-month combinations for advertising campaigns.

---

### **5. AVG Profit vs. Return Rate**
- **Description**:
  - A **bubble chart** shows the relationship between average profit and return rate across regions.
  - Example:
    - **Utah**: High return rate and losses.
    - **Michigan**: Low return rate and high profit.
  - The size and color of the bubbles represent the impact of returns.
  - **Return Rate**:
    - **Formula**:
      ```sql
      (SUM([Returned Indicator]) / COUNT([Order ID]))*100
      ```
    - Measures the percentage of returned products to total orders.
- **Purpose**:
  - To analyze regions with high return rates to minimize losses.

---

### **6. Return Rate by Hierarchy**
- **Description**:
  - A **treemap visualization** organizes return rate data hierarchically:
    - **Category**
    - **Product Name**
    - **Customer Name**
  - Drill-down functionality allows detailed analysis from categories to specific customers.
  - Example:
    - **Technology**: Return Rate (%): 27.331.
    - **Furniture**: Return Rate (%): 25.601.
- **Purpose**:
  - To identify categories, products, and customers contributing most to returns and address the causes effectively.
---

## **Data Used**

1. **Orders Table**:
   - Includes sales, profit, product, category, and subcategory details..
2. **Returns Table**:
   - Tracks returned products to calculate return rates.
3. **People Data**:
   - Name of Regional Manager and Region.

---

## **Insights & Recommendations**

### **1. Top Profit Centers**
- Subcategories like **Copiers** (West region) and **Phones** (Central region) remain the most profitable.
- Expanding operations in these areas or replicating their strategies across other regions could significantly boost overall revenue.

### **2. Products to Eliminate**
- Products such as **GBC DocuBind P400 Electric Binding System** and **Cubify CubeX 3D Printer Double Head Print** show substantial losses.
- These products should be evaluated for potential discontinuation or significant cost reductions to minimize financial impact.

### **3. Advertising Opportunities**
- The **top 3 state-month combinations** for advertising based on Return on Advertising Spend (ROAS) are:
  - **Indiana | October**: Average Profit $643.1, Ad Spend $128.6, ROAS 5.
  - **Vermont | November**: Average Profit $596.0, Ad Spend $119.2, ROAS 5.
  - **Washington | March**: Average Profit $521.3, Ad Spend $104.3, ROAS 5.
- Allocate marketing budgets to these state-month combinations to maximize returns on advertising investments.

### **4. Underperforming Subcategories**
- Subcategories like **Tables** and **Bookcases** demonstrate high sales volumes but low profitability and elevated return rates.
- Focus on optimizing production costs, revisiting pricing strategies, or redesigning these products to improve profitability.

### **5. Return Rate Trends**
- Categories like **Technology** (Return Rate 27.331%) and **Furniture** (Return Rate 25.601%) contribute heavily to overall return rates.
- Drill-down analysis reveals specific products and customers responsible for these returns, enabling targeted interventions to reduce return rates and enhance customer satisfaction.

---

### **Navigation Guide**
1. **Top/Bottom Profit Centers**:
   - Identify high-performing and low-performing subcategory and region combinations.
2. **Subcategories: Profit vs. Sales**:
   - Explore subcategories needing cost or pricing adjustments.
3. **Which Products Are at Risk**:
   - Evaluate products with the highest losses and consider necessary actions.
4. **Top 3 State-Month Combinations**:
   - Focus on state-month pairs with high advertising ROI.
5. **AVG Profit vs. Return Rate**:
   - Investigate regions with high return rates and low profits.
6. **Return Rate by Hierarchy**:
   - Drill down into return rates by category, product, and customer to mitigate issues.


