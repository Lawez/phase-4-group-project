# phase-4-group-project

![house.jpg](https://github.com/Lawez/phase-4-group-project/blob/main/house.jpg)

## BUSINESS OVERVIEW INTRODUCTION

Zillow is a leading online real estate marketplace that provides valuable services and tools for home buyers, sellers, renters, and real estate professionals.

The real estate investment firm is seeking to leverage data-driven insights to identify the best zip codes for real estate investment. The firm aims to make strategic investment decisions based on accurate forecasts of future real estate prices. By investing in the right locations, the company intends to maximize profitability and mitigate risk. The goal is to provide clients with attractive investment opportunities and generate sustainable returns.

We will be forecasting real estate prices of various zip codes using data from Zillow Research. The Zillow real-estate investment firm has tasked us with finding out which zip codes align with the investment firm's objectives and strategy.

### CHALLENGES

- In conducting the analysis, we had to determine how to best go about it given the ambiguity of the data. Finding out what would be the best method to go about the project in order to garner the best results. The major challenges were whether to direct the results towards maximizing profit, minimizing loss and risk and what time horizon would best fit for the project
- Model Selection and Performance Evaluation:

Selecting an appropriate time series forecasting model can be challenging due to the diverse nature of real estate data. There are several models available, such as ARIMA, SARIMA, Prophet, or machine learning algorithms, each with their strengths and limitations. Determining the most suitable model and optimizing its performance requires careful consideration and thorough evaluation using appropriate evaluation metrics.

### PROBLEM STATEMENT

*The firm wants to maximize profitability while considering the associated risks and the time horizon for the investment.*

### OBJECTIVES

The objective of this project is:

1. To provide a recommendation for the top 5 best zip codes for a real estate investment firm to invest in.
2. What are the historical trends and patterns in real estate prices for different zip codes?
3. What are the key factors that influence real estate prices in each zip code?
4. How do different zip codes compare in terms of risk and return on investment?

#### DATA

This dataset was obtained from [Zillow Research](https://www.zillow.com/research/data/). The dataset was from April 1996 to April 2018. It has 14273 rows and 272 columns.

### DATA GROCERY

| Column     | Description                                        |
| ---------- | -------------------------------------------------- |
| RegionID   | Unique index for each region                       |
| RegionName | Unique zip code for each region                    |
| City       | City in which the zip code is located              |
| State      | State in which the zip code is located             |
| Metro      | Metropolitan area in which the zip code is located |
| CountyName | County in which the zip code is located            |
| SizeRank   | Numerical rank of the size of the zip code         |

#### RECORDING THE EXPERIMENTAL DESIGN

* Data Exploration: Begin by exploring the provided dataset, zillow_data.csv, to gain insights into the real estate market. Understand the variables, their meanings, and the structure of the data. This exploration will guide the selection of predictors for real estate price forecasting.
* Definition of "Best Investment": Clarify the investment firm's objectives, risk tolerance, and investment strategy. Consider the desired profitability, time horizon, and any specific constraints or preferences. This definition will guide the selection of evaluation metrics and the criteria for identifying the top 5 zip codes.
* Data Preprocessing and Feature Engineering: Clean the dataset, handle missing values, and preprocess the features for modeling. Explore the possibility of incorporating external data sources, such as economic indicators or demographic data, to enhance the forecasting models. Feature engineering techniques may be applied to extract meaningful information from the available variables.
* Time Series Modeling: Select an appropriate time series forecasting model based on the characteristics of the data and the defined objectives. Popular models for time series forecasting include ARIMA, SARIMA, Prophet, or machine learning algorithms like LSTM or XGBoost. Train the chosen model using historical real estate price data.
* Model Evaluation: Evaluate the performance of the time series model using appropriate metrics, such as mean squared error (MSE), mean absolute error (MAE), or root mean squared error (RMSE). Compare the model's accuracy against baseline models or other approaches to assess its effectiveness in predicting real estate prices.
* Risk Assessment: Assess the risk associated with each zip code by analyzing historical price volatility, market trends, and external factors that may impact the real estate market. Consider factors such as economic stability, population growth, crime rates, and the availability of amenities. Quantify the risk using suitable risk evaluation techniques.
* Profitability Analysis: Calculate profitability metrics for each zip code, such as return on investment (ROI), cash flow, or rental yield. Consider factors like property appreciation, rental demand, vacancy rates, and potential income streams. This analysis will provide insights into the potential financial gains from investing in each zip code.
* Final Recommendation: Synthesize the findings from the risk assessment, profitability analysis, and model performance to make a recommendation on the top 5 best zip codes for investment. Present a rationale that incorporates key insights from the data analysis and supports the recommendation with quantitative and qualitative justifications.

##### Data Exploration

* **The data exploration was done using the following steps:**

  * Going through the data understanding. Knowing what each column means and what each represents.
  * We saw that the main target of the project, that is Zipcodes, is represented by the RegionID column.
  * The City, State and County are columns that describe the general locations for the dataset. That is, a general to specific approach to the exact locations.
  * Metro is a likely representation of the subway systems within these locations.
* This helps us to know what columns would be fitting for us to move foward with and understand the values contained within.
* The rest of the columns are dates that are filled with values in a wide format for readability.
* The Zillow dataset is sure to make more sense after modelling when we use these values in a long format

##### Best Investment

* Definition of "Best Investment" needed a better understanding of the data and what would be best for the firm. This would necessitate looking at the investment firm's objectives, risk tolerance, and investment strategy. What would be best in terms of profitability for the organization or would they rather minimize losses? How would they tolerate risk given downward trend in the data?
* The need for some of these metrics such as return on investment has brought a need to do feature engineering for the dataset.

##### Preprocessing and Feature Engineering

- For preprocessing the data, as well as feature engineering, the data is made into a usable dataset that can be used for modelling. This is where the data is converted into the long format from the wide format. This is to fit all the date-time columns into a single column and contain their values in a similar corresponding column.
- This is a part of feature engineering for easier and more sensible workability of the data especially for modelling.
  - The convertion of the columns into a date-time column with corresponding value columns allows us to be able to analyse the trends and seasons.
- The creation of the ROI and ROI2 columns also serves as a process of feature engineering as these columns will be used to perform evaluation at the end of the modelling section.

##### Modeling

* In this section, our cleaned data will modeled to predict what may be a future trend. It is also assessed for any trends as well as seasonality.

##### Metric of Success

* This is where we use measures such as return on investments (ROI) as well as risk assesment to determine whether the project has met the requirements.
* Return on investments measures the returns against the initial cost. The higher the difference the more beneficial the investment is. The aim is to have a high value as possible here in  order to maximize profitability
* Another measure is risk assesment as we need to determine the investments with the least risks because this will translate to higher returns. The lower the probable risks the better for our data

##### Evaluation

* The cleaned and modeled data is evaluated and measured against the success metrics so as to determine the efficacy of the results. Some questions can be asked such as:
  * Does the project fit the firm's needs?
  * Is the advise given sound?
  * What is the result and has the metric of success defined previously been met successfully?
