# parulmital_2511909_part3_regression_insights
#  Business Problem Summary

The objective of this analysis is to understand which factors are associated with monthly sales performance across retail stores. The leadership team wants to use this information to make better decisions related to marketing spend, inventory management, staffing levels, discount strategies, and store prioritization.

The key question is: what drives monthly sales, and how can the business improve store performance using data?

# Dataset Description

The dataset used in this analysis is business_regression_data.xlsx. It contains store-level monthly performance data, including:

Store details (store_id, region, store_type)
Operational factors (staff_count, inventory_availability_pct)
Customer and demand indicators (footfall, customer_rating)
Marketing and pricing variables (marketing_spend, avg_discount_pct)
External factors (competitor_distance_km, holiday_flag)
Target variable (monthly_sales)
# Dependent and Independent Variables

Dependent Variable

monthly_sales → This is the main variable we are trying to explain.
Independent Variables

marketing_spend
footfall
avg_discount_pct
staff_count
inventory_availability_pct
competitor_distance_km
holiday_flag
customer_rating
store_type (converted into dummy variables)
🔍 Data Preparation and Cleaning

Before running regression models, I performed the following steps:

Checked for missing values and handled them using median substitution for numerical fields
Removed records where monthly_sales was missing
Standardized categorical fields such as region and store_type
Ensured numerical fields were correctly formatted
These steps ensured the dataset was suitable for regression analysis.

# Dummy Variable Approach

Since regression models require numerical inputs, I converted the categorical variable store_type into dummy variables.

Each store type was converted into a binary column (0 or 1)
Residential store type was used as the reference category
Other store types (e.g., Mall, High Street, Airport) are interpreted relative to Residential
This avoids redundancy and ensures the model remains interpretable.

# Regression Approach

The analysis was done in two stages:

1. Simple Regression

I first built simple models using one variable at a time:

Model 1: monthly_sales vs footfall
Model 2: monthly_sales vs marketing_spend
Model 3: monthly_sales vs inventory availability
This helped in understanding individual relationships.

2. Multiple Regression

I then built a final model using multiple variables together, including:

marketing_spend
footfall
avg_discount_pct
staff_count
inventory_availability_pct
competitor_distance_km
holiday_flag
customer_rating
store_type dummy variables
This model gives a more realistic representation since sales are affected by multiple factors together.

# Model Comparison Summary

Simple models were useful but had limited explanatory power
The multiple regression model performed better
It explains a higher portion of variation in monthly sales
Final model:

R-squared: (auto-calculated in Excel)
Adjusted R-squared: (auto-calculated)
# Final Model Selected

The multiple regression model was selected as the final model because:

It includes multiple business drivers
It is more realistic compared to single-variable models
It provides better insights for decision-making
# Business Recommendation
Based on the analysis:

Footfall and inventory availability are important drivers of sales
Marketing spend also plays a role but should be evaluated for efficiency
Store type differences suggest that some formats perform better than others

# Recommended Actions:

Focus on increasing store footfall through targeted campaigns
Improve inventory availability to avoid stock-outs
Monitor high-performing store types and replicate best practices
Investigate stores that underperform compared to model predictions
⚠️ Assumptions and Limitations

Regression shows association, not causation
Some external factors (weather, local events, competitor promotions) are not included
Data is limited to available months and stores
Results should be combined with business judgment

# Screenshots Included
The repository includes the following evidence:

simple_regression_output.png
multiple_regression_output.png
residuals_preview.png
model_comparison_preview.png

 # Conclusion

This analysis shows that multiple operational and business factors influence monthly sales. The regression model provides useful insights, but it should be used as a decision-support tool, not as the only basis for decisions.
