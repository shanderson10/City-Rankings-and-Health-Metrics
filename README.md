# City-Rankings-and-Health-Metrics

![City-Rankings-and-Health-Metrics](https://github.com/user-attachments/assets/2f852d04-3c1c-4f23-b6e4-72ff46d1d8ac)


## Introduction
This project explores the relationship between city rankings, happiness levels, and health metrics such as obesity and life expectancy. It aims to uncover patterns and insights that can guide urban planning and public health initiatives.

## About the Dataset
Key Features and Relationships:
1.  Rank vs. Happiness Levels:
- Explore how city rankings (e.g., economic or social rankings) correlate with overall happiness scores.
- Consider using data such as GDP per capita, unemployment rates, or other social metrics to enrich your analysis.
2.  Obesity Levels vs. Life Expectancy:
- Investigate the relationship between obesity prevalence and its impact on average life expectancy.
- Identify trends across different regions or demographics to uncover patterns in health disparities.
3.  Relationships:
  - Rank vs. Happiness: Examine how societal factors, such as access to education or healthcare, affect happiness rankings. Use scatterplots or regression models to visualize correlations.
  - Obesity Levels vs. Life Expectancy: Apply correlation analysis to quantify the strength of this relationship. A negative correlation might indicate the health impact of higher obesity rates.
    
Modeling for Predictions
- Combine the above features (e.g., rank, happiness, obesity levels, life expectancy) to build a predictive model.
- Use machine learning techniques like regression analysis or classification models to predict overall quality of life and health outcomes.

## Questions Answered on city rankings and health metrics:
1.  Are higher-ranked cities consistently happier?
2.  What impact do rising obesity rates have on average life expectancy across different cities?
3.  What combination of factors (e.g., rank, happiness, obesity rates) best predicts overall quality of life?
4.  Do cities in certain regions consistently perform better or worse in these metrics?

5.  What interventions could cities prioritize to improve quality of life and health outcomes?

   ## Leveraged Colab 
   By utilizing Colab, I handle tasks like importing:
   - Datasets
   - Processing data
   - Conducting numerical computations
   - Creating visualizations

 ## Import Libraries and Load Data
 Importing necessary libraries and loading dataset- Pandas as pd
    
Range Index: 44 entries, 0 to 43
Data columns (total 12 columns):
 #   Column                                  Non-Null Count  Dtype  
---  ------                                  --------------  -----  
- 0   City                                    44 non-null     object 
- 1   Rank                                    44 non-null     int64  
 -2   Sunshine hours(City)                    44 non-null     object 
 3   Cost of a bottle of water(City)         44 non-null     object 
 4   Obesity levels(Country)                 44 non-null     float64
 5   Life expectancy(years) (Country)        44 non-null     float64
 6   Pollution(Index score) (City)           44 non-null     object 
 7   Annual avg. hours worked                44 non-null     object 
 8   Happiness levels(Country)               44 non-null     float64
 9   Outdoor activities(City)                44 non-null     int64  
 10  Number of take out places(City)         44 non-null     int64  
 11  Cost of a monthly gym membership(City)  44 non-null     object 
dtypes: float64(3), int64(3), object(6)
memory usage: 4.2+ KB

![City-Rankings-and-Health-Metrics- Pandas as pd ](https://github.com/user-attachments/assets/6d70796f-0dbf-48b6-9b55-ddb9086ea673)
