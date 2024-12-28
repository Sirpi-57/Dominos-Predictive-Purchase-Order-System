# Dominos-Predictive-Purchase-Order-System

## Objective
The goal of this project is to optimize Dominos' ingredient ordering process by accurately forecasting pizza sales and generating efficient purchase orders. Leveraging predictive analytics, the system helps maintain optimal inventory levels, reduce waste, and streamline supply chain operations.

## Dataset

### Sales Dataset

This dataset contains detailed information about pizza sales, including:

**pizza_id:** Unique identifier for each pizza.

**order_id:** Identifier for each order.

**pizza_name_id:** Identifier for the pizza name.

**quantity:** Number of pizzas ordered in each transaction.

**order_date:** Date of the order.

**order_time:** Time of the order.

**unit_price:** Price per unit for the pizza.

**total_price:** Total price of the order.

**pizza_size:** Size of the pizza (e.g., Small, Medium, Large).

**pizza_category:** Category of the pizza (e.g., Veg, Non-Veg).

**pizza_ingredients:** List of ingredients used in the pizza.

**pizza_name:** Name of the pizza.

### Ingredients Dataset

This dataset includes information on the ingredients required for each pizza type:

**pizza_name_id:** Identifier for the pizza name.

**pizza_name:** Name of the pizza.

**pizza_ingredients:** Ingredients used in the pizza.

**Items_Qty_In_Grams:** Quantity of each ingredient required (in grams).

## Detailed Workflow

### 1. Data Preprocessing

#### Handling Missing Values:

Filled missing values in pizza_name_id, pizza_category, and pizza_ingredients using mappings and existing data relationships.

#### Duplicate Analysis:

Removed duplicates to ensure data integrity.

#### Merging Datasets:

Combined sales and ingredient datasets on pizza_name_id for feature enrichment.

#### Feature Engineering:

Extracted temporal features like day, month, year, and categorized weekends vs. weekdays.
Created time-based metrics, such as working hours and time periods, to identify patterns.

### 2. Exploratory Data Analysis (EDA)

**Sales Trends:**

Visualized sales patterns over time and identified seasonality and weekly trends.

**Pizza Performance:**

Identified top-selling pizzas, popular pizza sizes, and categories using bar charts and distribution plots.

**Seasonality Analysis:**

Highlighted sales peaks during weekends and specific months.

**Ingredient Usage:**

Analyzed ingredient consumption for each pizza type to optimize inventory planning.

### 3. Predictive Modeling

Multiple models were implemented and compared based on performance:

#### Traditional Models:

**ARIMA and SARIMA:** Time-series models capturing trends and seasonality.
Prophet: Robust forecasting model designed for business time-series data.

#### Machine Learning Models:

**Linear Regression:** Baseline regression for temporal features.
**XGBoost:** Gradient boosting for robust predictions.

#### Deep Learning:

**LSTM Neural Network:** Leveraging sequential data for time-series forecasting.

### 4. Forecasting and Purchase Order Generation
   
**Sales Forecasting:**

Predicted weekly sales for different pizza types.

**Ingredient Calculation:**

Mapped sales forecasts to ingredient requirements.

**Purchase Order Creation:**

Generated detailed purchase orders, listing quantities of ingredients required for the forecasted period.

**Key Findings**

**Best Model: SARIMA (1,0,1)x(2,0,0,7) demonstrated the lowest MAPE (0.1507)**, capturing seasonal trends effectively.

**Ingredient Insights:**

High-demand ingredients include chicken, red onions, and capocollo.

**Pizza Insights:**

Large-sized specialty pizzas (e.g., Spicy Italian, Thai Chicken) showed the highest demand.

## Results

**Sales Forecast:** Predicted total sales of 3,566 pizzas for the next week.

**Ingredient Requirements:** Calculated specific ingredient quantities needed to meet the forecasted demand.

**Model Performance:**

SARIMA: MAPE = 0.1507

Linear Regression: MAPE = 0.1906

LSTM: MAPE = 0.2379

![ingredients 1](https://github.com/user-attachments/assets/a913133e-049c-47b1-a8ab-f59d03610eff)
![ingredients 2](https://github.com/user-attachments/assets/52d1a6b8-5027-4354-aa1d-4d00509c0687)


## Conclusion

This project demonstrates the effective use of time-series forecasting and machine learning to optimize inventory management and improve supply chain decisions. The SARIMA model stands out as the most reliable for weekly sales predictions.

## Future Scope

1.Incorporate external variables like weather, promotions, and events into forecasting models.

2.Expand to real-time predictions for dynamic inventory adjustments.

## Deliverables

1.Cleaned and preprocessed datasets.

2.Exploratory Data Analysis (EDA) reports.

3.Predictive models with evaluation metrics.

4.Weekly sales forecast and detailed purchase orders.

5.Source code and documentation (GitHub repository).
