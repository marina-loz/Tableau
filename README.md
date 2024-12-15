# **Return Rate Analysis Project**
### **Tableau Link**
[View the Dashboard on Tableau Public](https://public.tableau.com/views/storytelling1-1_pdf/Story2?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link).

To provide a clear walkthrough of the analysis and dashboard, I created a video presentation that explains the goals, methodology, and insights of the **Return Rate Analysis Project**.  

You can watch the video presentation here:  
🔗 [**Video Presentation Link**](https://drive.google.com/file/d/1naLFYw6KmfTdTf8kxS5dZL_oXO9YbetQ/view?usp=sharing)


## **Overview**
This Tableau project explores **Return Rate Analysis** to identify trends, root causes, and actionable insights for product returns. By analyzing returns across categories, time periods, and regions, the project helps in understanding the correlation between sales and returns while highlighting key problem areas.

---

## **1. Project Goals**
The goals of the **Return Rate Analysis** are as follows:
1. **Understand Return Trends**: Identify patterns in return rates over time, categories, and geography.  
2. **Uncover Root Causes**: Analyze correlations between sales and return rates to find underlying issues.  
3. **Measure Impact**: Use key metrics like **Return Rate**.  
4. **Provide Actionable Insights**: Develop recommendations to minimize return rates and financial losses.  
5. **Interactive Monitoring**: Build a dynamic Tableau dashboard for real-time return rate analysis.  

---

## **2. Structure of the Tableau Story**

### **Page 1: Introduction**
- **Title**: *"Return Rate Analysis: Goals and Objectives"*  
- **Content**:  
   - Explains the goals of the analysis (as listed above).  

---

### **Page 2: Return Metrics**
- **Title**: *"Which Metric is Better?"*  
- **Key Metrics**:  
   1. **Return Rate**:  
      - **Definition**: Percentage of orders that are returned.  
      - **Formula**:  
        ```sql
        (SUM([Returned Indicator]) / COUNT([Order ID]))*100
        ```
   2. **Total Cost of Returns**:  
      - **Definition**: Total financial impact of returned products.  
      - **Formula**:  
        ```sql
        SUM(IF [Returned Indicator] = 1 THEN [Product Cost] ELSE 0 END)
        ```
   3. **Total Number of Returns**:  
      - **Definition**: Total count of returned orders.  
      - **Formula**:  
        ```sql
        SUM([Returned Indicator])
        ```
- **Purpose**: Compares the three metrics to explain when each is useful:
   - **Return Rate**: Best for analyzing trends across categories and regions.  
   - **Cost of Returns**: Useful for understanding financial losses.  
   - **Total Returns**: Ideal for operational analysis.  

---

### **Page 3: Root Cause Analysis**
- **Title**: *"What Causes Returns?"*  
- **Chart**: **Scatter Plot** - *Correlation Between Sales and Returns*  
- **Insight**:  
   - Products with higher sales often have higher returns.  
   - Example: **Binders** and **Paper** show both high sales and high return counts.  
   - Categories like **Appliances** and **Accessories** are exceptions, with lower returns despite moderate sales.  
- **Purpose**: Identifies key product subcategories contributing to high returns.  

---

### **Page 4: Return Rate Analysis Dashboard**
- **Title**: *"Interactive Return Rate Analysis Dashboard"*  
- **Components of the Dashboard**:  
   1. **Total Profit**:  
      - KPI displaying overall profit: **$360,129.5**.  
   2. **Return Rate by Category**:  
      - Bar chart showing return rates for major categories:  
         - **Technology**: 19%  
         - **Furniture**: 18%  
         - **Office Supplies**: 10%  
   3. **Correlation Between Sales and Returns**:  
      - Scatter plot illustrating how higher sales lead to higher returns for certain products.  
   4. **Return Rate by Geography**:  
      - Map visualizing return rates across U.S. states.  
      - State like **California (11.14%)**  has the highest return rates.  
   5. **Return Seasonalities**:  
      - Line chart showing return rate trends by month.  
      - Insight: Return rates peak in **August** and during the **holiday season** (November-December).  
   6. **Highlight Category Filter**:  
      - Interactive filter to analyze return rates for specific categories.  

- **Purpose**:  
   - Allows users to explore data interactively.  
   - Provides insights across multiple dimensions: category, geography, and time.

---

## **3. Key Insights**
1. **High Return Categories**:  
   - Categories like **Technology** and **Furniture** have the highest return rates.  
2. **Geographic Patterns**:  
   - State like **California** contribute the most to returns.  
3. **Correlation Between Sales and Returns**:  
   - Products with high sales, such as **Binders**, also have higher return counts.  
4. **Seasonality**:  
   - Return rates spike during specific months, particularly **August** and **November-December** (holiday season).  

---

## **4. Recommendations**
1. **Product Quality Improvement**:  
   - Focus on high-return products like **Binders** and **Tables** to identify quality issues.  
2. **Geographic Targeting**:  
   - Implement targeted strategies to reduce returns in high-return states like **California**.  
3. **Monitor Trends**:  
   - Use the Tableau dashboard to regularly analyze return rates and identify problem areas.  

---

## **5. How to Use the Tableau Story**
1. **Navigate Between Story Pages**:  
   - Use the tabs at the top to move between Introduction, Metrics, Root Cause Analysis, and Dashboard.  
2. **Interactive Features**:  
   - Apply filters (e.g., Category, Year) to analyze specific segments.  
   - Hover over charts and maps to explore detailed insights.  
3. **Key Visuals**:  
   - Use the scatter plot to identify correlations.  
   - Analyze categories and geographies using bar charts and maps.

---

## **6. Files Submitted**
- **PDF Export of the Tableau Story**: `Return_Rate_Analysis.pdf`  

---

## **Conclusion**
This project provides a comprehensive analysis of product returns using Tableau, identifying key patterns, root causes, and actionable insights. The interactive dashboard enables dynamic exploration of return trends, empowering stakeholders to make data-driven decisions to reduce returns and improve profitability.  
