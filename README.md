# City-Rankings-and-Health-Metrics-Project

![City-Rankings-and-Health-Metrics](https://github.com/user-attachments/assets/2f852d04-3c1c-4f23-b6e4-72ff46d1d8ac)


## Introduction
This project explores the relationship between city rankings, happiness levels, and health metrics such as obesity and life expectancy. It aims to uncover patterns and insights that can guide urban planning and public health initiatives.

## About the Dataset
Key Features and Relationships
1.  Rank vs. Happiness Levels:
- Explore how city rankings (e.g., economic or social rankings) correlate with overall happiness scores.
- Consider using data such as GDP per capita, unemployment rates, or other social metrics to enrich your analysis.
2.  Obesity Levels vs. Life Expectancy:
- Investigate the relationship between obesity prevalence and its impact on average life expectancy.
- Identify trends across different regions or demographics to uncover patterns in health disparities.
3.  Relationships:
  - Rank vs. Happiness: Examine how societal factors, such as access to education or healthcare, affect happiness rankings. Use scatterplots or regression models to visualize correlations.
  - Obesity Levels vs. Life Expectancy: Apply correlation analysis to quantify the strength of this relationship. A negative correlation might indicate the health impact of higher obesity rates.
    
Modeling for Predictions:
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
 Importing necessary libraries and loading dataset- Using Colab with:
 - Pandas
 - Matplotlib
 - Seaborn

 ![Panda as pd Coding](https://github.com/user-attachments/assets/c877ae6f-887d-4c29-ad9b-63bf3432ba0a)

## Data Wrangling
To ensure our data is in the best form for analysis, removed currency symbols and percentages, converting relevant columns to float.

![Data Wrangling](https://github.com/user-attachments/assets/07a9ae70-c659-4c97-9157-0e789f7000c6)

## Data Exploration
 Explored the dataset using summary statistics and visualizations to identify patterns and relationships.
![Summary statistics](https://github.com/user-attachments/assets/51c86274-f101-4160-b4d1-7aea66d6b4b9)

## Rank vs. Happiness levels (Country)

![City- Rankings- and-Health-Metrics-44 Cities](https://github.com/user-attachments/assets/a0331e41-d4bc-481f-9ccb-74a3e8e38a43)

![pandas core frame DataFrame](https://github.com/user-attachments/assets/bbfa7462-64c6-45a1-a7dc-3ef0e35b11f3)
   
![City-Rankings-and-Health-Metrics- Pandas as pd ](https://github.com/user-attachments/assets/6d70796f-0dbf-48b6-9b55-ddb9086ea673)

![Sunshine hours by City Visualizations](https://github.com/user-attachments/assets/637a2ca6-f880-4533-a815-354820fea985)

## Obesity vs. Life Expectancy

![image](https://github.com/user-attachments/assets/bb6a2e4d-5ee0-43b3-91de-4c141db1013c)

![Obesity Level vs  Life Expectancy Visualization](https://github.com/user-attachments/assets/c54ce3e7-dceb-4f2f-8fcb-b0ef39ac6c37)

## Statistical Analysis
Correlation Matrix
To understand the relationships between different numerical features in the dataset, created a correlation matrix.

![correlation matrix-Create DataFrame](https://github.com/user-attachments/assets/4f9088d7-7cf2-49b0-be5f-becb9555ba54)

![correlation matrix-Compute](https://github.com/user-attachments/assets/37d24afc-1195-4f62-99e6-59fd6398c244)

![correlation matrix-Visualization](https://github.com/user-attachments/assets/db0b9e3c-7f7a-4aa1-b4ce-7f8f317de0e8)

## Mean Squared Error
![import pandas as pd-Define the DataFrame](https://github.com/user-attachments/assets/e0ee3625-7074-40be-b834-a635088a95de)

## T-statistic & P-value
![import pandas as pd-T-statistic](https://github.com/user-attachments/assets/d77e9ca2-f354-43a7-af88-fb9e01bb5cc4)

## Overall Findings
- Rank and Happiness Levels: Higher-ranked cities generally show higher happiness levels, but exceptions suggest other influencing factors like economic stability and cultural aspects.
- Obesity Levels and Life Expectancy: A strong negative correlation supports the hypothesis that lower obesity levels correlate with higher life expectancy.

1. Statistical Significance
- Rank and Happiness: Correlation analysis showed a positive trend, but not all high-ranked cities had high happiness levels, indicating a moderate correlation that needs further exploration.
- Obesity and Life Expectancy: Statistical tests confirmed a significant negative correlation, emphasizing the critical impact of obesity on health outcomes.

2. Practical Implications
- For Policymakers: Data supports the need for initiatives targeting obesity reduction to enhance public health.
- For Public Health Officials: Insights highlight areas for infrastructure improvement and community programs to boost happiness.
- For Urban Planners: Findings can guide the development of more livable, happy cities.
- For Researchers: Detailed methodologies and results provide a foundation for further study.
- For the General Public: Emphasizing the importance of healthy lifestyles can motivate positive changes.

3. The Pursuit of Joy and Longevity
- Hypothesis 1: Higher-ranked cities will have higher happiness levels
- Hypothesis 2: Lower obesity levels will correlate with higher life expectancy.

4. The Journey of Happiness
- Setting the Stage: We believed that a city's rank (reflecting its desirability) would impact resident happiness. High-ranked cities with better amenities and environments were expected to have happier citizens.
- The Analysis: Plots showed that high-ranking cities like Vienna and Amsterdam had high happiness levels. However, cities like Sydney, despite a lower rank, also had high happiness, suggesting other influencing factors.
- The Realization: Rank did influence happiness but wasn't the sole factor. Economic stability, social cohesion, and cultural norms also played significant roles.
- The Weight of Health Starting Point: Hypothesized that lower obesity levels lead to higher life expectancy.
- The Data Dive: Clear pattern emerged—countries with low obesity rates (e.g., Japan) had higher life expectancies. Countries with higher obesity rates (e.g., USA) had shorter life spans.
- The Confirmation: Hypothesis confirmed. Reducing obesity significantly increases life expectancy, emphasizing the need for public health initiatives focused on nutrition and fitness.
- Conclusion Happiness: Influenced by city rank but also by multifaceted factors.
- Life Expectancy: Strongly correlated with lower obesity levels. These insights guide strategies for enhancing happiness and health in communities.

## Conclusions
Through cleaning, exploring, and visualizing data, you can uncover meaningful relationships, such as the impact of obesity on life expectancy or the correlation between happiness and city rankings. These insights not only deepen your analytical expertise but also allow you to contribute actionable findings to real-world challenges, solidifying your journey from a data enthusiast to a committed Data Analyst.
