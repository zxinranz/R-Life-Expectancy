# R-Life-Expectancy
Exploring main effective variables of life expectancy（school project）
## Introduction
The average life expectancy of a population is the average number of years a person born during the same period is expected to continue living, holding current mortality rates at different ages constant. Comparative analysis of life expectancy per capita reflects the quality of life in a society, measures the health status of the people in a country (or region), and provides important data for insurance companies dealing with life insurance.<br>
Life expectancy is both one of the most important indicators of the health status of the population and a comprehensive indicator of the level of economic and social development of a country or region. Indicators such as life expectancy are one of the most fundamental research elements for evaluating and predicting the quality of the population, measuring the burden of disease, and evaluating the national economy and the quality of life of the population.<br>
The analysis of the main influencing variables of life expectancy can be of great help in the prediction of life expectancy.

## Data Description
The publicly available dataset provides data for 193 countries spanning from year 2000 to year 2015 and is structured in 2938 rows (data points) which are characterized into a total of 22 columns (features)[here](https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who). The features can be categorized into two groups:

Health factors which are originally provided by the Global Health Observatory (GHO) data repository under the World Health Organization (WHO).
Economic factors which have been collected by the United Nation (UN) website.

The variables used in this report are:

- `Country`: Country name
- `Year`: Year of the date
- `Status`: Country status of developed or developing
- `Adult_Mortality`: Adult Mortality Rates of both sexes (probability of dying between 15 and 60 years per 1000 population)
- `Life_expectancy`: Life_Expectancy in age
- `infant.deaths`:Number of Infant Deaths per 1000 population
- `Alcohol`: Alcohol, recorded per capita (15+) consumption (in litres of pure alcohol)
- `percentage.expenditure`: Expenditure on health as a percentage of Gross Domestic Product per capita(%)
- `Hepatitis.B`: Hepatitis B (HepB) immunization coverage among 1-year-olds (%)
- `Measles`: number of reported cases per 1000 population
- `BMI`: Average Body Mass Index of entire population
- `under.five.deaths`: Number of under-five deaths per 1000 population
- `Polio`: Polio (Pol3) immunization coverage among 1-year-olds (%)
- `Total.expenditure`: General government expenditure on health as a percentage of total government expenditure (%)
- `Diphtheria`: Diphtheria tetanus toxoid and pertussis (DTP3) immunization coverage among 1-year-olds (%)room)
- `HIV.AIDS`: Deaths per 1 000 live births HIV/AIDS (0-4 years)
- `GDP`: Gross Domestic Product per capita (in USD)
- `Population`: Population of the country
- `thinness..1.19.years`: Prevalence of thinness among children and adolescents for Age 10 to 19 (% )
- `thinness.5.9.years`: Prevalence of thinness among children for Age 5 to 9(%)
- `Income.composition.of.resources`: Human Development Index in terms of income composition of resources (index ranging from 0 to 1)
- `Schooling`: Number of years of Schooling(years)

## Conclusion
According to our analysis, we found the best fit model to be 
$$Y = 53.42 +0.94x_1 - 0.43 x_2 -0.02 x_3 +10.69x_4 + 0.02x_5 + 0.03 x_6 - 1.55 x_7 -0.13x_8 -0.04x_9$$
, where Y is the response variable(life expectancy). 
- $x_1$ = `Schooling`
- $x_2$ = `HIV.AIDS`
- $x_3$ = `Adult.Mortality`
- $x_4$ = `Income.composition.of.resources`
- $x_5$ = `Diphtheria`
- $x_6$ = `BMI`
- $x_7$ = `StatusDeveloping`
- $x_8$ = `Alcohol`
- $x_9$ = `thinness.5.9.years`

Schooling, Income composition of resources, BMI and Diphtheria maintain a positive relationship with life expectancy.
**Number of years of schooling is the variable to focus on when determining life expectancy.**
In addition, income composition of resources also has a large impact on life expectancy.

The final model went from 21 predictor variables for the original data to nine predictor variables. adjusted R squared and RMSE were very close, so there was not much loss in removing these variables.
To get a more accurate prediction model to predict life expectancy, more possible variables need to be evaluated.
