# Vrindavan Store Data Analysis and Dashboard Creation

## Problem Statement

The goal of this project was to clean, preprocess, and organize a dataset from the "Vrindavan Store" to facilitate effective analysis and visualization. The dataset included information about customer orders, such as order ID, customer ID, gender, product categories, and purchase dates. The main challenges addressed included:

### Data Inconsistencies
- **Gender Information**: Inconsistent representations of gender (e.g., "M" vs. "Male").
- **Missing or Incorrect Values**: Some columns, such as age, gender, or product category, contained missing or incorrect values.

### Date Handling
- **Invalid Dates**: The date column contained invalid dates or required extraction of specific parts (like the month or year) for further analysis.

### Data Structure
- **Irrelevant Columns**: The dataset contained irrelevant columns or extra data that needed to be cleaned, including duplicates or missing values.

### Data Transformation
- **New Columns for Analysis**: Additional columns were created, such as categorizing customers into age groups or extracting useful date-related information (e.g., month, quarter).

### Dashboard Creation
- **Interactive Dashboard**: A dynamic dashboard was created where user interaction (via slicers) automatically updated charts and graphs based on selected criteria such as customer demographics or product categories.

## Approach

### 1. Setting Up the Dashboard
**Objective:** Create a dynamic dashboard where user selection in a slicer would automatically change the visuals (charts and data).

**Technical Approach:**  
- Linked the slicer to pivot tables or pivot charts.  
- When a user selected a value from the slicer (e.g., Amazon, Go), it filtered the data accordingly and updated the corresponding charts using Excel's PivotTable and PivotChart functionalities.

### 2. Data Cleaning and Validation

**Objective:** Clean and validate the dataset to ensure it was suitable for analysis.

**Technical Approach:**  
1. **Loaded the Dataset**: The data was loaded from an external source (Excel sheet). The dataset was structured with columns representing attributes like order ID, customer ID, product category, gender, etc.  
2. **Inspected the Data**: Checked for errors such as missing values, duplicates, or incorrect data types.

### 3. Cleaning the Gender Column

**Objective:** Standardize the gender column to resolve inconsistencies.

**Technical Approach:**  
- Used Excel’s Find and Replace (Ctrl + F and Replace All) to standardize gender values.  
- Replaced variations like "M" with "Male" and "W" with "Female" to ensure consistency.

### 4. Handling the Date Column

**Objective:** Ensure the date column was properly formatted and contained valid dates.

**Technical Approach:**  
- Verified the date range for consistency (e.g., January to December).  
- Removed or corrected invalid dates.
- Used the `TEXT()` function to extract specific date parts such as the month or year for further analysis.  
  - Formula: `=TEXT(Date, "mmm")` (extracts the month name).

### 5. Handling Duplicate or Missing Data

**Objective:** Ensure that the dataset was free of duplicates or missing values.

**Technical Approach:**  
- Used Excel’s **Remove Duplicates** feature to eliminate redundant rows.
- Checked for null or blank values and handled them appropriately (either by imputing or removing rows).

### 6. Creating New Columns for Analysis

**Objective:** Added new columns for deeper analysis, such as age categorization.

**Technical Approach:**  
- **Age Group Classification**: Used the `IF()` function to categorize customers into age groups.  
  - Formula: `=IF(Age > 50, "Senior", IF(Age <= 30, "Teenager", "Adult"))`.

### 7. Extracting Month from Date

**Objective:** Extract the month from the date column for categorization.

**Technical Approach:**  
- Used the `TEXT()` function to extract the month from the date field.  
  - Formula: `=TEXT(Date, "mmm")` (e.g., "Jan", "Feb", etc.).

### 8. Ensuring Data Consistency Across Columns

**Objective:** Ensured that all columns were consistent in format and values.

**Technical Approach:**  
- Reviewed each column for incorrect formatting, missing values, or duplicates.
- Applied data validation techniques (e.g., data validation lists, filters, or conditional formatting) to ensure uniformity and standards.

### 9. Final Validation

**Objective:** Ensured the dataset was clean and ready for analysis.

**Technical Approach:**  
- After cleaning and processing, reviewed the dataset to ensure no errors or inconsistencies remained.
- Ensured that any transformations (e.g., replacing values or extracting date parts) were accurately applied.

## Process Overview

### Initial Formatting and Setup:
- Disabled the outline and set the fill option to "No Fill" for cleaner chart displays.
- Adjusted font size and color for readability.

### Gender-Based Shopping Comparison:
- Used a pivot table to compare shopping behavior by gender.
- Applied percentage display to compare male vs. female shoppers.
- Copied the data for further analysis and adjusted the font for clarity.

### Order Status Analysis:
- Inserted a pivot table to analyze different order statuses (e.g., Canceled, Delivered).
- Created a pie chart to visualize the distribution of these statuses.
- Adjusted the chart format to improve readability.

### Sales by Location:
- Used pivot tables to analyze sales by location (state-wise).
- Filtered data to display the top 5 states with the highest sales.
- Created a horizontal bar chart with customized labels.

### Order Contribution by Channel:
- Analyzed sales contributions by different channels (e.g., online, physical stores).
- Created a pie chart to represent sales data.
- Added a slicer for dynamic interaction and filtering across charts.

### Final Dashboard:
- Combined multiple charts into a single interactive dashboard.
- Applied slicer controls to enable dynamic filtering of data by category.

## Key Tools and Techniques Used

- **Pivot Tables**: For summarizing and aggregating data, enabling comparisons like gender vs. shopping behavior, order status distribution.
- **Charts (Pie and Bar)**: To visualize the breakdown of sales data, order statuses, and regional performance.
- **Slicer**: To provide interactivity in the dashboard, allowing users to filter and view data dynamically.
- **Data Formatting**: Applied various formatting techniques such as font adjustments, color changes, and chart element customization for readability.
- **Filtering and Sorting**: Used filters (e.g., top 5 states) to focus on relevant data points.

## Insights

### 1. **Gender-Based Shopping Behavior**:
   - **Insight**: A comparison of shopping behavior between male and female shoppers revealed distinct patterns. One gender group exhibited higher spending or purchase frequency, offering opportunities for targeted marketing.
   - **Actionable Outcome**: Tailoring promotions or product recommendations based on gender could increase engagement and sales.

### 2. **Order Status Distribution**:
   - **Insight**: A pie chart analysis of order statuses showed the proportion of successful versus unsuccessful transactions (e.g., canceled, returned).
   - **Actionable Outcome**: A high percentage of canceled or returned orders signaled issues with product quality, delivery, or customer service. Improving these areas could reduce cancellations and returns.

### 3. **Sales by Location (State-Level Analysis)**:
   - **Insight**: The top states contributing to sales were identified, allowing for region-specific marketing strategies or stock adjustments.
   - **Actionable Outcome**: Targeting high-sales regions with localized promotions or expanding product offerings in underperforming states could boost overall sales.

### 4. **Order Contribution by Channel**:
   - **Insight**: The sales distribution across different channels (e.g., online, mobile, in-store) showed which platforms generated the most revenue.
   - **Actionable Outcome**: Optimizing high-performing channels or improving underperforming ones (e.g., by offering special discounts or improving mobile app features) could increase conversions.

### 5. **Dashboard Insights**:
   - **Insight**: The dashboard allowed for dynamic filtering and analysis, enabling users to interact with the data to explore relationships between gender, order status, and sales trends.
   - **Actionable Outcome**: With interactive slicers, users could drill down into specific data points and make faster, more informed business decisions.

## Conclusion

The project successfully cleaned and processed the Vrindavan Store dataset, enabling better analysis and insights. By using pivot tables, charts, and interactive slicers, a dynamic dashboard was created to help visualize key business metrics such as gender-based shopping behavior, order status distribution, sales by location, and sales contribution by channel.

These insights informed targeted marketing strategies, improved customer service, and optimized sales across various touchpoints.

## Dashboard
![Excel Dashboard](https://github.com/user-attachments/assets/5250beea-8332-4726-a2c1-769792db0313)

