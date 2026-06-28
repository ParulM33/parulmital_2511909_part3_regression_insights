# Model Equations

 

## 1. Dependent Variable 

 

The dependent variable used in all regression models is:

 

monthly_sales

 

This represents the total monthly sales of each store.

 

---

 

## 2. Simple Regression Models 

 

### Model 1: Marketing Spend 

 

monthly_sales = Intercept + (β1 × marketing_spend)

 

This model evaluates how marketing spend impacts sales.

 

---

 

### Model 2: Footfall 

 

monthly_sales = Intercept + (β1 × footfall)

 

This model shows the relationship between customer visits and sales.

 

---

 

### Model 3: Inventory Availability 

 

monthly_sales = Intercept + (β1 × inventory_availability_pct)

 

This model measures the impact of product availability on sales.

 

---

 

## 3. Multiple Regression Model 

 

The final model combines multiple business drivers:

 

monthly_sales = Intercept 

+ (β1 × marketing_spend) 

+ (β2 × footfall) 

+ (β3 × inventory_availability_pct) 

+ (β4 × avg_discount_pct) 

+ (β5 × staff_count) 

+ (β6 × customer_rating) 

+ (β7 × holiday_flag) 

+ (β8 × store_type_Airport) 

+ (β9 × store_type_High Street) 

+ (β10 × store_type_Mall) 

 

---

 

## 4. Dummy Variable Explanation 

 

The categorical variable **store_type** was converted into dummy variables:

 

- store_type_Airport 

- store_type_High Street 

- store_type_Mall 

 

The **Residential store type was used as the reference category** and was not included in the model.

 

This avoids multicollinearity (dummy variable trap) and allows interpretation relative to Residential stores.

 

---

 

## 5. Coefficient Interpretation 

 

- A **positive coefficient** means an increase in that variable increases sales 

- A **negative coefficient** means an increase in that variable decreases sales 

- Dummy variables show how each store type performs compared to Residential stores 

 

Example: 

- Positive coefficient for footfall → higher customer visits increase sales 

- Positive coefficient for inventory availability → better stock increases sales 

 

---

 

## 6. Final Model Selected 

 

The **multiple regression model** was selected as the final model.

 

---

 

## 7. Reason for Selection 

 

The final model was selected because:

 

- It has the highest R-squared value 

- It includes multiple important business drivers 

- It provides a more realistic and complete understanding of sales performance 

 

---

 

## 8. Key Takeaway 

 

Sales are influenced by multiple factors, not just one variable. 

 

The combination of marketing, customer traffic, inventory, staffing, and store type provides the strongest explanation of monthly sales performance.


