📊 SQL & Excel-Based Funnel Analysis

This project presents a comprehensive sales funnel analysis using SQL and Excel, focusing on user interactions across six key e-commerce events. The analysis visualizes how users move through the funnel in the top three countries based on total event volume.

🔍 Project Overview

Funnel analysis is a widely used technique in product and user analytics. It helps visualize the steps users take toward a specific goal (such as making a purchase), and highlights where users drop off. This method is commonly used in e-commerce, SaaS, and marketing to improve user journeys and conversion rates.

Goals:

Extract and transform user interaction data

Identify top 3 countries by event volume

Build a clean funnel dataset for analysis

Visualize funnel steps and drop-offs in Excel

🗂️ Dataset Description

Source: raw_events table from a BigQuery project

Content: Timestamped user event data with geographical information

Events Used in Funnel:

page_view

view_item

add_to_cart

add_shipping_info

add_payment_info

purchase

🧠 Methodology
🔹 Step 1: SQL Data Preparation

Structured the funnel dataset using SQL with the following logic:

Deduplication: Ensured only the first occurrence of each event per user was counted using the ROW_NUMBER() function. This prevents overcounting (e.g., a user going back and forth to checkout multiple times).

Country Filtering: Identified the top 3 countries by total number of relevant events.

Event Selection: Focused only on the 6 key funnel events listed above.

Event Ranking: Created an ordered funnel structure to ensure linear progression through funnel steps.

Final Output: A summarized table showing the number of users at each funnel step for each of the top 3 countries.

💡 Using MIN() was not sufficient for capturing the first unique event per user. ROW_NUMBER() provided a more accurate result.

🔹 Step 2: Excel-Based Analysis

Once the data was prepared, it was exported to Excel for visualization and further analysis:

Created funnel charts for each of the top 3 countries

Calculated drop-off rates between each step

Analyzed conversion rates from start to finish

Generated actionable insights based on the trends observed

📈 Analysis Results

The Excel workbook includes:

Visual funnel breakdowns by country

User drop-off and conversion metrics

Observations and insights for optimization opportunities

🛠️ Tools & Technologies

SQL (Google BigQuery)

Excel (Charts, Pivot Tables, Conditional Formatting)

📌 Conclusion

This project demonstrates how combining SQL and Excel can produce powerful funnel visualizations to help understand user behavior. It enables businesses to:

Pinpoint where users abandon the process

Compare performance across key regions

Identify steps to improve the user journey and increase conversions
