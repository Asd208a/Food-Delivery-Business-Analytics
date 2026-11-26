# Food Delivery Business Analytics

An interactive business analytics project built with **Microsoft Power
BI Desktop**, **Power Query**, and **DAX** to analyze food delivery
orders, revenue, restaurant performance, customer ratings, and
operational patterns.

> **Project type:** Business Intelligence / Data Analytics\
> **Primary tool:** Power BI Desktop\
> **Dataset:** Food Delivery Order History (Kaggle)\
> **Author:** Asad Khan

------------------------------------------------------------------------

## 1. Project Overview

This project explores food delivery transaction data to understand order
volume, revenue, customer satisfaction, restaurant performance, and
operational patterns. Data preparation is performed in Power Query,
calculations are created with DAX, and the results are presented in an
interactive Power BI report.

The dashboard examines customer ordering patterns, restaurant
performance, revenue movement, order statuses, customer ratings, kitchen
preparation time (KPT), and delivery distance.

## 2. Project Objectives

-   Measure overall order and revenue performance using KPIs.
-   Identify restaurants with the highest order volume and revenue.
-   Explore monthly revenue patterns and peak ordering hours.
-   Compare average customer ratings across restaurants.
-   Examine order statuses and exception rates.
-   Analyze kitchen preparation time across different hours.
-   Explore the relationship between delivery distance and kitchen
    preparation time.

## 3. Tools and Technologies

  -----------------------------------------------------------------------
  Technology                          Application
  ----------------------------------- -----------------------------------
  Microsoft Power BI Desktop          Data modelling, interactive
                                      reports, and dashboard development

  Power Query                         Data inspection, cleaning, and
                                      transformation

  DAX                                 Measures and calculated columns

  Kaggle dataset                      Source transaction data
  -----------------------------------------------------------------------

## 4. Dataset

**Dataset selected:** Food Delivery Order History

**Dataset source:** [Food Delivery Order History Data – Kaggle](https://www.kaggle.com/datasets/sujalsuthar/food-delivery-order-history-data)

The dataset contains food-delivery order records and fields used in the
analysis, including order identifiers, restaurant names, order
timestamps, order statuses, order totals, delivery distance, customer
ratings, and KPT duration.

The dataset is not included in this repository. Download it from the
original Kaggle page and comply with its licence and usage conditions.

## 5. Data Preparation

Data preparation was carried out in Power Query in Power BI.

-   Reviewed the imported table, column names, and data types.
-   Checked missing values and duplicate order identifiers.
-   Verified numeric fields such as `Total` and `Distance_KM`.
-   Checked the `Order Placed At` date/time field.
-   Retained the combined food-item information as supplied by the
    dataset.
-   Created an `Order Hour` calculated column from the order timestamp
    for hourly analysis.
-   Prepared the table for DAX measures and report visuals.

The original order timestamp was retained; `Order Hour` was added to
group orders by hour of day.

## 6. Key Performance Indicators

  KPI                     Meaning
  ----------------------- ---------------------------------------------
  Total Orders            Count of orders in the dataset
  Total Revenue           Sum of the order `Total` values
  Average Order Value     Average revenue per order
  Delivered Orders        Count of orders whose status is `Delivered`
  Delivery Success Rate   Delivered orders divided by total orders
  Average Rating          Average customer rating
  Average KPT Duration    Average kitchen preparation duration
  Exception Orders        Total orders minus delivered orders
  Exception Rate          Exception orders divided by total orders

**Metric interpretation:** `Exception Orders` means orders not
classified as `Delivered`; it should not be interpreted as cancellations
alone. KPT means **Kitchen Preparation Time**, not the complete time
taken to deliver an order to the customer.

## 7. Dashboard Visualizations

  -----------------------------------------------------------------------
  Visualization                       Business question
  ----------------------------------- -----------------------------------
  Orders by Order Status              How are orders distributed across
                                      the recorded statuses?

  Top Restaurants by Order Volume     Which restaurants receive the most
                                      orders?

  Top Restaurants by Revenue          Which restaurants generate the most
                                      revenue?

  Monthly Revenue Trend               How does revenue vary across the
                                      available months?

  Orders by Hour of Day               At what hours are orders most
                                      frequent?

  Average KPT Duration by Hour        How does kitchen preparation
                                      duration vary by order hour?

  Average Customer Rating by          How do average ratings compare
  Restaurant                          across restaurants?

  Exception Orders by Restaurant      Which restaurants have the largest
                                      number of non-delivered orders?

  Exception Rate by Restaurant        Which restaurants have the highest
                                      exception proportion?

  Delivery Distance vs Kitchen        What pattern is visible between
  Preparation Time                    order distance and KPT?
  -----------------------------------------------------------------------

## 8. Selected Findings from the Dashboard

The following values were observed in the completed Power BI report.
They are dataset-specific and may change if the data or filters change.

  Metric                         Observed value
  ------------------------- -------------------
  Total Orders                Approximately 21K
  Total Revenue                          14.55M
  Average Order Value                    682.62
  Delivery Success Rate                  99.11%
  Average Customer Rating                  4.36

Other observations:

-   **Aura Pizzas** had the highest order volume and revenue among the
    restaurants shown.
-   **Masala Junction** had the highest average customer rating in the
    restaurant comparison.
-   The hourly order chart showed the strongest ordering activity in the
    evening, with the highest bar around 20:00.
-   Average KPT varied by hour; the chart can be used to inspect
    preparation-time patterns during busy periods.
-   The distance-versus-KPT scatter plot showed substantial variation in
    KPT at similar distances. It does not, by itself, establish that
    distance causes a change in preparation time.
-   Absolute exception counts should be interpreted alongside exception
    rates because restaurants have different order volumes.

## 9. How to Open the Project

1.  Install **Microsoft Power BI Desktop**.
2.  Clone or download this repository.
3.  Download the dataset from its original Kaggle source.
4.  Open `Dashboard/Food_Delivery_Dashboard.pbix` in Power BI Desktop.
5.  If Power BI cannot find the source file, edit the source step in
    Power Query and point it to your downloaded dataset.
6.  Apply the changes and select **Refresh**.
7.  Explore the report visuals and any available filters.

## 10. Skills Demonstrated

-   Business analytics and exploratory data analysis
-   Data cleaning and transformation
-   Power Query
-   DAX measures and calculated columns
-   KPI design and monitoring
-   Data visualization and dashboard development
-   Revenue and restaurant performance analysis
-   Customer satisfaction analysis
-   Operational performance analysis
-   Communicating data-driven observations

## 11. Author

**Asad Khan**\
B.Tech Computer Science Engineering \| Minor in Data Science

-   **GitHub:** https://github.com/Asd208
------------------------------------------------------------------------

## Notes

-   KPI values reflect the dataset and filter context used when the
    dashboard was prepared.
-   Revenue is shown in the units and currency represented by the source
    data. Confirm the source dataset's currency before adding a currency
    symbol.
-   The dataset is not redistributed in this repository. Refer to the
    original Kaggle listing for access and licensing information.
