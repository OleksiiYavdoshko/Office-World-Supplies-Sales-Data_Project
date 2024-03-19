# Office World Supplies Sales Data Analysis

![](Intro_image_Office_Supplies.jpg)
---

## Introduction
This is an Excel and Power BI project of an **imaginary store** called **Office World**. Data set was provided on Skills Bootcamp from We Are Group. The project is to analyse and derive insights to answer crucial questions and help the store make data-driven decision. 

### Company background
Office World, with over 60 years of experience, is a well-established retailer specializing in office supplies and technology products. The company is committed to offering quality products and excellent customer service. 

### Current position
Office World seeks to enhance its marketing efforts by gaining a deeper understanding of product popularity, profitability, and customer preferences. The company aims to leverage this insight to expand its customer base and improve customer satisfaction.

### Company objectives
Office World's primary objectives include identifying in-demand products, maximizing profitability, and reaching new customers through targeted marketing strategies.

## Executive summary

### The problem
Office World aims to analyse its product sales data to identify popular and profitable products and understand its current customer base better.

### The analysis's goal
The objective of this analysis is to assess product popularity, profitability, and customer segmentation to inform marketing strategies and improve product offerings.

### The data and techniques employed
The analysis utilizes sales data including order date, ship date, customer segment, product category, region, quantity ordered new, cost of sales, unit price, etc. Techniques such as data cleaning, exploratory data analysis, and visualization were employed to derive insights from the data.

### Brief interpretation of results
The analysis reveals insights into product popularity, profitability, and customer segments. These insights will guide Office World in optimizing its marketing strategy.

## Main body

### Summary of errors in data
The dataset was carefully reviewed for errors and inconsistencies to ensure data accuracy and reliability for meaningful analysis. The errors include:
1. Structural errors:
- Spelling errors (In ship mode there are 2 values that are actually the same (Parcel 2 Go and ParcelToGo), there is only 1 value of Parcel 2 Go, so change it to ParcelToGo);
- Incongruent values (In Product Category there are 2 same values as well. There are Tech and Technology. There is only 1 value for Tech, so change it to Technology).
2. Data types and formats:
- Incorrect data types (In the ship date column there are 2 data types: date and text);
- Incorrect formats (In order date column there are 2 different format of date type).
3. Duplicates:
- More than one instance of the same record of data in a dataset, thus leading to incorrect calculations, results or conclusions (7 duplicates values were found in the dataset).

### Additional calculations and columns
Additional calculated columns were made:
- Date difference (difference between Ship date and Order date);
- Total costs ((Cost of Sales + Shipping Cost) *(1-discount));
- Sales Revenue (Quantity ordered new * Unit Price);
- Profit (Sales Revenue - Total costs).

### Hypothesis
- **Correlation between order priority and date difference** (This question explores whether there is a relationship between the urgency of order priority and the time it takes for orders to be shipped, which can inform decision-making regarding order processing efficiency);
- **Correlation between ship mode and date difference** (This question investigates whether the chosen shipping mode affects the time it takes for orders to be shipped, which can impact logistics and customer satisfaction);
- **Is there a relationship between the quantity of products ordered and the discount offered?** (This question examines whether there is a correlation between the quantity of products ordered and the discount offered, which can influence purchasing behaviour and pricing strategies);
- **Which product sub-category, product category and customer segment are the best-selling and are most profitable (worst selling)** (This question aims to identify the top-performing and underperforming product sub-categories, categories, and customer segments in terms of sales and profitability, guiding resource allocation and marketing efforts);
- **Which regions have the highest and lowest sales and profits?** (This question analyses regional sales and profitability data to identify geographic trends and opportunities, helping prioritize markets and allocate resources effectively);
- **How does the unit price of products vary across different product sub-categories?** (This question examines the variability in unit prices across different product sub-categories, providing insights into pricing strategies and market dynamics within specific product categories);
- **Trends or patterns in sales, profits over time (monthly, quarterly)** (This question explores temporal trends and patterns in sales and profits over time, allowing for the identification of seasonality, growth trends, or other cyclical patterns that can inform strategic decision-making and resource planning).

## Analysis
<p align="center" width="100%">
    <img width="40%" src="Average_of_Date_difference_by_Order_Priority.png">
</p>

The data presented in the chart indicates a notable correlation between the date difference and order priority. Specifically, orders with low priority exhibit a higher average date difference, around 4 days, whereas orders with high and critical priority show substantially lower average date differences, ranging between 1.3 to 1.4 days.

<p align="center" width="100%">
    <img width="40%" src="Average_of_Date_difference_by_Ship_Mode.png">
    <img width="40%" src="Count_of_Order_Date_by_Ship_Mode.png">
</p>

Similar analysis was conducted to investigate the correlation between ship mode and date difference. The data suggests that there is minimal variation in date differences, ranging from 1 to 2 days across different ship modes. Notably, Royal Mail exhibits the highest average date difference, nearly 2 days. However, upon closer examination, it is evident that Royal Mail also handles the largest number of orders (1280), which may vary significantly in priority. Therefore, it is reasonable to infer that there is no significant correlation between ship mode and date difference.

<p align="center" width="100%">
    <img width="70%" src="Pivot_table.png">
</p>
<p align="center" width="100%">
    <img width="40%" src="Correlation_analysis.png">
</p>

To examine the relationship between the quantity of products ordered and the discount offered, I created a pivot table and conducted a correlation analysis. The pivot table reveals that there is only one order for a product with a 17% discount and just ten orders for products with a 21% discount. While these numbers may initially seem like outliers, upon closer examination, they do not appear to significantly skew the data. Furthermore, the correlation analysis revealed that there is no correlation between the quantity ordered and the discount percentage. Despite the common assumption that higher discounts might lead to larger quantities ordered, this analysis suggests otherwise.

Overall, the purpose of this analysis was to investigate whether higher discounts influence the quantity of ordered products. However, the findings indicate that discount percentage alone may not be a significant driver of order quantity.
<p align="center" width="100%">
    <img width="40%" src="Sum_of_Sales_by_Product_Category.png">
    <img width="40%" src="Sum_of_Profit_by_Product_Category.png">
</p>
<p align="center" width="100%">
    <img width="40%" src="Sum_of_Quantity_by_Product_Category.png">
    <img width="41%" src="Sum_of_Unit_Price_by_Product_Category.png">
</p>

The analysis of the provided charts reveals that the Technology category emerges as both the most selling and most profitable product category. Despite Office Supplies being the most ordered category, its comparatively lower average unit price results in smaller profits.
<p align="center" width="100%">
    <img width="40%" src="Sum_of_Sales_by_PSC_and_PC.png">
    <img width="40%" src="Sum_of_Profit_by_PSC_and_PC.png">
</p>

The charts above indicate that the Telephones and Communication, along with Office Machines, emerge as the most profitable sub-categories.
<p align="center" width="100%">
    <img width="40%" src="Sum_of_Sales_by_Customer_Segment.png">
    <img width="40%" src="Sum_of_Profit_by_Customer_Segment.png">
</p>
<p align="center" width="100%">
    <img width="40%" src="Sum_of_Quantity_by_Customer_Segment.png">
    <img width="40%" src="Sum_of_Unit_Price_by_Customer_Segment.png">
</p>

The analysis of the provided charts reveals that the Corporate customer segment emerges as both the most selling and most profitable. While the Consumer segment has the highest average unit price, its smaller quantity of orders results in comparatively lower sales and profit.
