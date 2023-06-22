# phase-4-group-project

![housejpg](https://github.com/Lawez/phase-4-group-project/blob/main/Images/house.jpg)

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
   
3. How do different zip codes compare in terms of risk and return on investment?


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

## EDA analysis and Visualization

### Question one

      To provide a recommendation for the top 5 best zip codes/city for a real estate investment firm to invest in.
  
![image3.png](https://github.com/Lawez/phase-4-group-project/blob/main/Images/image3.png)



| Zipcode/city        | Return on Investment |
|-----------------|----------------------|
| Washington_20002 | 0.256557             |
| Washington_20009 | 0.636023             |
| NewYork_11226    | 0.243899             |
| LosAngeles_90046 | 0.694970             |
| NewYork_11230    | 0.039668             |

* Some cities (Washington & New York) have a higher count of properties, suggesting a larger availability and demand for real estate in those areas.
  
* Based on the analysis, it is recommended to consider real estate investment opportunities in Los Angeles (90046) and Washington (20009) due to their higher Return on Investment (ROI) compared to New York (11230). These cities have demonstrated favorable ROI percentages of approximately 69.5% and 63.6% respectively.
  
#### Question two
      What are the historical trends and patterns in real estate prices for different zip codes?


![image2.png](https://github.com/Lawez/phase-4-group-project/blob/main/Images/image2.png)


* In each of the regions `"Washington_20002", "Washington_20009", "NewYork_11226", "LosAngeles_90046", "NewYork_11230"`, we can observe the boom and bust cycle that was previously discussed. The boom and bust cycle refers to the pattern of economic growth followed by a period of decline or recession.

* Some regions fared better than others in weathering the post-2008 lows. This can be seen by comparing the depth of the trough, which represents the lowest point in the economic cycle. Regions that experienced a lower trough were more resilient and recovered faster from the economic downturn.

* However, despite the variations in the severity of the bust cycle, all regions have shown an overall upward trend in recent years. This indicates that the economy in each region has been recovering and growing steadily. The upward trend suggests positive economic conditions and reflects the resilience and strength of these regions in bouncing back from the previous recession.
  
### Question Three

  How do different zip codes compare in terms of risk and return on investment?

| Zipcode/city        | Sharpe Ratio   |
|-----------------|----------------|
| Washington_20002 | 326.298586    |
| Washington_20009 | 518.163312    |
| NewYork_11226    | 502.199697    |
| LosAngeles_90046 | 511.920597    |
| NewYork_11230    | 18.300270     |

* The Sharpe ratio of an investment indicates its return per unit of risk and enables investors to assess returns in relation to the level of risk taken.

* In this context, Washington_20009 exhibits the highest risk-adjusted return among the investments considered. This implies that, relative to the level of risk associated with the investment, `Washington_20009` offers the most favorable returns making it potentially more attractive for investment.

## METHODS



## RESULTS





## CONCLUSION

In conclusion, the analysis of the real estate data provided valuable insights into the property market. Los Angeles (90046) and Washington (20009) stood out as areas with high Return on Investment (ROI) and strong potential for real estate investment. These regions exhibited a significant increase in property values over time, indicating favorable market conditions. Additionally, the geographical distribution analysis revealed the concentration of properties in certain cities, emphasizing the importance of targeted location selection. Considering these findings, it is recommended to further explore investment opportunities in Los Angeles and Washington, while conducting thorough market research, financial analysis, due diligence, and consulting with experts. By following these steps, investors can make informed decisions and potentially capitalize on the high ROI observed in these regions. 

## RECOMMENDATION

- Based on the analysis, it is recommended to consider real estate investment opportunities in Los Angeles (90046) and Washington (20009) due to their higher Return on Investment (ROI) compared to New York (11230). These cities have demonstrated favorable ROI percentages of approximately 69.5% and 63.6% respectively.

- The high ROI in these cities could be attributed to factors such as strong market demand, desirable locations, growing economies, and potential for future property value appreciation.

#### NEXT STEPS

- Conduct in-depth market research: Gather more detailed information about the real estate market in Los Angeles and Washington, including current market trends, rental demand, vacancy rates, and future development plans. This will provide a comprehensive understanding of the market dynamics and potential risks.

- Identify suitable properties: Explore property listings in the recommended areas and evaluate them based on factors such as location, property condition, price, and potential for value appreciation.

- Perform financial analysis: Assess the financial viability of the investment opportunities by calculating potential rental income, expenses (including property taxes and maintenance costs), and projected cash flow. This analysis will help determine the potential return and profitability of the investments.



**Repository Structure:**

```
├── zillow_data.csv                                        <- Data location of our study
├── images                                                 <- images folder of our notebook 
├── presentation.pdf                                       <- PDF version of project presentation 
├── LISENCE.md                                             <- LICENCE of the project
├── README.md                                              <- The top-level README for reviewers of this project                  
└── timeseries.ipynb                                       <- Narrative documentation of analysis in Jupyter notebook
```
