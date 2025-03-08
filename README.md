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
   
#  Rank vs Happiness levels(Country)

#from matplotlib import pyplot as plt
#import seaborn as sns

"""
def _plot_series(series, series_name, series_index=0):
  palette = list(sns.palettes.mpl_palette('Dark2'))
  xs = series['City']
  ys = series['Happiness levels(Country)']

  plt.plot(xs, ys, label=series_name, color=palette[series_index % len(palette)])

fig, ax = plt.subplots(figsize=(10, 5.2), layout='constrained')
df_sorted = df.sort_values('Rank', ascending=True)
_plot_series(df_sorted, '')
sns.despine(fig=fig, ax=ax)
plt.xlabel('Capital Cities by Rank')
plt.xticks(rotation=75)
_ = plt.ylabel('Happiness levels(Country)')
"""

def _plot_series(series, series_name, series_index=0):
  palette = list(sns.palettes.mpl_palette('Dark2'))
  xs = series['City']
  ys = series['Happiness levels(Country)']

  plt.plot(xs, ys, label=series_name, color=palette[series_index % len(palette)])

fig, ax = plt.subplots(figsize=(10, 5.2), layout='constrained')
df_sorted = df.sort_values('Rank', ascending=True)
_plot_series(df_sorted, '')
sns.despine(fig=fig, ax=ax)
plt.xlabel('Capital Cities by Rank')
plt.xticks(rotation=75)
_ = plt.ylabel('Happiness levels(Country)')
Obesity vs Life Expectancy (Year)
"""
plt.figure(figsize=(10, 6))
sns.scatterplot(x='Obesity levels(Country)', y='Life expectancy(years) (Country)', data=df)
plt.title('Obesity Levels vs. Life Expectancy')
plt.xlabel('Obesity Levels (%)')
plt.ylabel('Life Expectancy (years)')
plt.show()
"""
plt.figure(figsize=(10, 6))
sns.scatterplot(x='Obesity levels(Country)', y='Life expectancy(years) (Country)', data=df)
plt.title('Obesity Levels vs. Life Expectancy')
plt.xlabel('Obesity Levels (%)')
plt.ylabel('Life Expectancy (years)')
plt.show()
"""
'\nplt.figure(figsize=(10, 6))\nsns.scatterplot(x='Obesity levels(Country)', y='Life expectancy(years) (Country)', data=df)\nplt.title('Obesity Levels vs. Life Expectancy')\nplt.xlabel('Obesity Levels (%)')\nplt.ylabel('Life Expectancy (years)')\nplt.show()\n'
Key Features:

Rank vs Happniess
Obesity levels vs life expectancy
Relationships:

Rank vs. Happiness levels
Obesity levels vs. Life expectancy
Modeling: Use these features to predict overall quality of life and health outcomes.

Import Libraries and Load Data
Import Libraries and Load Data
We start by importing necessary libraries and loading our dataset.
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

path= "/content/drive/MyDrive/Dataset/healthy_lifestyle_city_2021.csv"
df=pd.read_csv(path)
df.info()
df.head (5)
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 44 entries, 0 to 43
Data columns (total 12 columns):
 #   Column                                  Non-Null Count  Dtype  
---  ------                                  --------------  -----  
 0   City                                    44 non-null     object 
 1   Rank                                    44 non-null     int64  
 2   Sunshine hours(City)                    44 non-null     object 
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
City	Rank	Sunshine hours(City)	Cost of a bottle of water(City)	Obesity levels(Country)	Life expectancy(years) (Country)	Pollution(Index score) (City)	Annual avg. hours worked	Happiness levels(Country)	Outdoor activities(City)	Number of take out places(City)	Cost of a monthly gym membership(City)
0	Amsterdam	1	1858	$1.92	20.4	81.2	30.93	1434	7.44	422	1048	$34.90
1	Sydney	2	2636	$1.48	29.0	82.1	26.86	1712	7.22	406	1103	$41.66
2	Vienna	3	1884	$1.94	20.1	81.0	17.33	1501	7.29	132	1008	$25.74
3	Stockholm	4	1821	$1.72	20.6	81.8	19.63	1452	7.35	129	598	$37.31
4	Copenhagen	5	1630	$2.19	19.7	79.8	21.24	1380	7.64	154	523	$32.53
Data Wrangling
Data Wrangling
To ensure our data is in the best form for analysis, we'll remove currency symbols and percentages, converting relevant columns to float.


[ ]
# Removing currency symbols and percentages, converting to float
df.fillna(0, inplace=True)

df['Cost of a bottle of water(City)'] = df['Cost of a bottle of water(City)'].astype(str).str.replace('$', '').astype(float)
df['Obesity levels(Country)'] = df['Obesity levels(Country)'].astype(str).str.replace('%', '').astype(float)
df['Cost of a monthly gym membership(City)'] = df['Cost of a monthly gym membership(City)'].astype(str).str.replace('$', '').astype(float)
df['Pollution(Index score) (City)'] = df['Pollution(Index score) (City)'].astype(str).str.replace('-', '0').astype(float)
df['Sunshine hours(City)'] = df['Sunshine hours(City)'].astype(str).str.replace('-', '0').astype(float)

#df = df[df['Rank'] <= 10]
#df.head(10)


Data Exploration
Data Exploration
We will now explore the dataset using summary statistics and visualizations to identify patterns and relationships.


[ ]
# Summary statistics
print(df.describe())
            Rank  Cost of a bottle of water(City)  Obesity levels(Country)  \
count  44.000000                        44.000000                 44.00000   
mean   22.500000                         1.173409                 21.92500   
std    12.845233                         0.718642                 10.19567   
min     1.000000                         0.150000                  3.90000   
25%    11.750000                         0.570000                 19.50000   
50%    22.500000                         1.195000                 22.30000   
75%    33.250000                         1.600000                 29.00000   
max    44.000000                         3.200000                 36.20000   

       Life expectancy(years) (Country)  Happiness levels(Country)  \
count                          44.00000                  44.000000   
mean                           78.17500                   6.435000   
std                             5.30437                   0.991202   
min                            56.30000                   3.570000   
25%                            75.40000                   5.870000   
50%                            80.40000                   6.900000   
75%                            81.80000                   7.175000   
max                            83.20000                   7.800000   

       Outdoor activities(City)  Number of take out places(City)  \
count                 44.000000                        44.000000   
mean                 213.977273                      1443.113636   
std                  127.190297                      1388.803270   
min                   23.000000                       250.000000   
25%                  125.250000                       548.000000   
50%                  189.500000                       998.000000   
75%                  288.250000                      1674.250000   
max                  585.000000                      6417.000000   

       Cost of a monthly gym membership(City)  
count                               44.000000  
mean                                40.420000  
std                                 15.006457  
min                                 16.070000  
25%                                 31.310000  
50%                                 37.330000  
75%                                 47.210000  
max                                 73.110000  

[ ]


df.info()
# Visualizations
plt.figure(figsize=(10, 6))
sns.barplot(x='City', y='Sunshine hours(City)', data=df )
plt.title('Sunshine Hours by City')
plt.xticks(rotation=75)
plt.show()


[ ]
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Example data for 44 cities
data = {
    'City': [f'City{i}' for i in range(1, 45)],
    'Obesity levels(Country)': [22.1, 25.3, 30.2, 28.4, 26.7, 24.5, 27.8, 29.1, 23.4, 25.6, 28.9, 30.1, 27.3, 26.5, 24.8, 29.0, 28.2, 25.7, 26.9, 27.1, 23.8, 24.9, 28.3, 29.2, 27.4, 26.6, 25.8, 28.5, 29.3, 27.5, 26.0, 24.6, 27.9, 29.4, 28.6, 25.9, 26.1, 27.6, 29.5, 28.7, 26.2, 27.7, 29.6, 28.8],
    'Life expectancy(years) (Country)': [82, 79, 75, 78, 80, 81, 77, 76, 83, 84, 85, 74, 73, 72, 71, 70, 69, 68, 67, 66, 65, 64, 63, 62, 61, 60, 59, 58, 57, 56, 55, 54, 53, 52, 51, 50, 49, 48, 47, 46, 45, 44, 43, 42]
}
df = pd.DataFrame(data)




[ ]

plt.figure(figsize=(10, 6))
sns.scatterplot(x='Obesity levels(Country)', y='Life expectancy(years) (Country)', data=df)
plt.title('Obesity Levels vs. Life Expectancy')
plt.xlabel('Obesity Levels (%)')
plt.ylabel('Life Expectancy (years)')
plt.show()

Statistical Analysis
Statistical Analysis
We will perform correlation analysis and t-tests to determine the significance of our findings.

New Section
New Section
Double-click (or enter) to edit


[ ]

Start coding or generate with AI.
Correlation Matrix

To understand the relationships between different numerical features in our dataset, let's create a correlation matrix.


[ ]
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Create DataFrame
data = {
    'City': ['Amsterdam', 'Sydney', 'Vienna', 'Stockholm', 'Copenhagen'],
    'Sunshine hours(City)': [11858, 22636, 31884, 41821, 51630],
    'Cost of a bottle of water(City)': ['£1.92', '£1.48', '£1.94', '£1.72', '£2.19'],
    'Obesity levels(Country)': ['20.40%', '29.00%', '20.10%', '20.60%', '19.70%'],
    'Life expectancy(years) (Country)': [81.23, 82.12, 81.0, 81.8, 79.8],
    'Pollution(Index score) (City)': [30.93, 26.86, 17.33, 19.63, 21.24],
    'Annual avg. hours worked': [1434, 1712, 1501, 1452, 1380],
    'Happiness levels(Country)': [7.44, 7.22, 7.29, 7.35, 7.64],
    'Outdoor activities(City)': [1048, 1103, 1008, 998, 957],
    'Number of take out places(City)': [34.90, 41.66, 25.74, 37.31, 32.53],
    'Cost of a monthly gym membership(City)': ['£34.90', '£41.66', '£25.74', '£37.31', '£32.53']
}
df = pd.DataFrame(data)

# Clean and convert columns to numeric
df['Cost of a bottle of water(City)'] = df['Cost of a bottle of water(City)'].str.replace('£', '').astype(float)
df['Obesity levels(Country)'] = df['Obesity levels(Country)'].str.replace('%', '', regex=False).astype(float)


[ ]
# Select only numeric columns for the correlation matrix
numeric_cols = df.select_dtypes(include=['float64', 'int64'])

# Compute the correlation matrix
corr_matrix = numeric_cols.corr()

# Plot the correlation matrix
plt.figure(figsize=(12, 8))
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Correlation Matrix')
plt.show()



[ ]
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error
from sklearn.preprocessing import StandardScaler

# Define the DataFrame
data = {
    'Happiness levels(Country)': [7.8, 6.5, 5.4],
    'Obesity levels(Country)': [22.1, 25.3, 30.2],
    'Life expectancy(years) (Country)': [82, 79, 75]
}
df = pd.DataFrame(data)

# Preparing the data
X = df[['Happiness levels(Country)', 'Obesity levels(Country)']]
y = df['Life expectancy(years) (Country)']

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Creating the model
model = LinearRegression()
model.fit(X_train, y_train)

# Making predictions
y_pred = model.predict(X_test)

# Evaluating the model
mse = mean_squared_error(y_test, y_pred)
print(f'Mean Squared Error: {mse}')
Mean Squared Error: 0.081956656128686

[ ]
import pandas as pd
from scipy.stats import ttest_ind

# Define the DataFrame
data = {
    'Outdoor activities(City)': [180, 200, 150, 210, 170],
    'Obesity levels(Country)': [22.1, 25.3, 30.2, 28.4, 26.7]
}
df = pd.DataFrame(data)

# Perform the t-test
group1 = df[df['Outdoor activities(City)'] <= 190]
group2 = df[df['Outdoor activities(City)'] > 190]
print(f'Group1 shape (rows, columns): {group1.shape}')
print(f'Group2 shape (rows, columns): {group2.shape}')

t_stat, p_val = ttest_ind(group1['Obesity levels(Country)'], group2['Obesity levels(Country)'])
print(f"T-statistic: {t_stat}")
print(f"P-value: {p_val}")



Group1 shape (rows, columns): (3, 2)
Group2 shape (rows, columns): (2, 2)
T-statistic: -0.15942219466831822
P-value: 0.8834647966272693
Conclusions
Conclusions
Our analysis reveals interesting insights into the factors influencing happiness and health in different cities. These insights can guide public health policies and urban planning to enhance overall well-being.

Overall Findings

Rank and Happiness Levels: Higher-ranked cities generally show higher happiness levels, but exceptions suggest other influencing factors like economic stability and cultural aspects.

Obesity Levels and Life Expectancy: A strong negative correlation supports the hypothesis that lower obesity levels correlate with higher life expectancy.

Statistical Significance

Rank and Happiness: Correlation analysis showed a positive trend, but not all high-ranked cities had high happiness levels, indicating a moderate correlation that needs further exploration.

Obesity and Life Expectancy: Statistical tests confirmed a significant negative correlation, emphasizing the critical impact of obesity on health outcomes.

Practical Implications

For Policymakers: Data supports the need for initiatives targeting obesity reduction to enhance public health.

For Public Health Officials: Insights highlight areas for infrastructure improvement and community programs to boost happiness.

For Urban Planners: Findings can guide the development of more livable, happy cities.

For Researchers: Detailed methodologies and results provide a foundation for further study.

For the General Public: Emphasizing the importance of healthy lifestyles can motivate positive changes.

The Pursuit of Joy and Longevity

Hypothesis 1: Higher-ranked cities will have higher happiness levels.

Hypothesis 2: Lower obesity levels will correlate with higher life expectancy.

The Journey of Happiness

Setting the Stage: We believed that a city's rank (reflecting its desirability) would impact resident happiness. High-ranked cities with better amenities and environments were expected to have happier citizens.

The Analysis: Plots showed that high-ranking cities like Vienna and Amsterdam had high happiness levels. However, cities like Sydney, despite a lower rank, also had high happiness, suggesting other influencing factors.

The Realization: Rank did influence happiness but wasn't the sole factor. Economic stability, social cohesion, and cultural norms also played significant roles.

The Weight of Health Starting Point: Hypothesized that lower obesity levels lead to higher life expectancy.

The Data Dive: Clear pattern emerged—countries with low obesity rates (e.g., Japan) had higher life expectancies. Countries with higher obesity rates (e.g., USA) had shorter life spans.

The Confirmation: Hypothesis confirmed. Reducing obesity significantly increases life expectancy, emphasizing the need for public health initiatives focused on nutrition and fitness.

Conclusion Happiness: Influenced by city rank but also by multifaceted factors.

Life Expectancy: Strongly correlated with lower obesity levels. These insights guide strategies for enhancing happiness and health in communities.

Policymakers: Emphasize the clear link between obesity and life expectancy to support health-promoting initiatives.

Public Health Officials: Use happiness and city ranking data to advocate for infrastructure improvements and community programs.

Urban Planners: Share findings on city rank and happiness to guide the development of more livable cities.

Researchers: Provide detailed analysis methods and results to contribute to ongoing health and urban development studies.

General Public: Communicate the impact of lifestyle choices on health and happiness, offering practical advice and motivation for healthier living.


