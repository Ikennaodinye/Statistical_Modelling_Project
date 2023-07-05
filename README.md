# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
Project goal is to build capacity on data wrangling and statistical modelling

The objective  is to explore and analyze bike-sharing and points of interest (POIs) data using APIs such as CityBikes, Foursquare, and Yelp

## Process
## STEP 1: was to send request to city bike for details of the stations in the city of Toronto. 669 rows and 4 columns were returned
## STEP 2: Connected to the foursquare and Yelp API, query to retrieve information on restaurants and bars in each of the city bike locations in Toronto.
Analyzed the data obtained from both API such as:
Checked the completeness of information for each POI category
Accessed the accuracy or consistency of the data provided by each API
Checked the availability of additional details
Performed some data wrangling
And compared the quality of information between the 2 APIs
## STEP 3: Joining data
Did left join to merge data obtained from Foursquare API and Yelp API
Then merged the output with city bike data with left join to obtain a new DataFrame
## STEP 4: Created SQL database
Validated it by retrieving columns and checking for duplicates
## STEP 5: Statistical Modelling
Performed  multivariant linear regression statistical modelling


## Results

## Comparative quality of API coverage in your chosen area:  

My city of choice was Toronto. Comparative analysis between both APIs showed that Yelp has more POIs and useful additional details. From the 3 station locations queried, the number of POI were 150 and 30 for Yelp and Foursquare respectively. And the useful addition details such as, ratings, review count, and distance were returned by Yelp API.

## Results of your model:
                            OLS Regression Results                            
==============================================================================
Dep. Variable:        Number of Bikes   R-squared:                       1.000
Model:                            OLS   Adj. R-squared:                  1.000
Method:                 Least Squares   F-statistic:                 5.817e+20
Date:                Tue, 04 Jul 2023   Prob (F-statistic):               0.00
Time:                        16:07:01   Log-Likelihood:                 2830.4
No. Observations:                 150   AIC:                            -5649.
Df Residuals:                     144   BIC:                            -5631.
Df Model:                           5                                         
Covariance Type:            nonrobust                                         
================================================================================
                   coef    std err          t      P>|t|      [0.025      0.975]
--------------------------------------------------------------------------------
const         3.224e+05   1.22e-05   2.65e+10      0.000    3.22e+05    3.22e+05
Latitude     -7832.7029   3.04e-07  -2.58e+10      0.000   -7832.703   -7832.703
Longitude_x   -247.1558   1.38e-08  -1.79e+10      0.000    -247.156    -247.156
distance     -1.714e-13   5.28e-13     -0.325      0.746   -1.21e-12    8.72e-13
review_count  1.817e-13   1.22e-12      0.149      0.882   -2.23e-12    2.59e-12
rating        1.432e-11   2.25e-10      0.064      0.949    -4.3e-10    4.59e-10
==============================================================================
Omnibus:                      133.984   Durbin-Watson:                   0.002
Prob(Omnibus):                  0.000   Jarque-Bera (JB):               21.498
Skew:                          -0.651   Prob(JB):                     2.15e-05
Kurtosis:                       1.679   Cond. No.                     7.35e+07
==============================================================================

Notes:
[1] Standard Errors assume that the covariance matrix of the errors is correctly specified.
[2] The condition number is large, 7.35e+07. This might indicate that there are
strong multicollinearity or other numerical problems.

The R squared and Adj R squared value of  1.000 demonstrates a better fit and 
latitude and longitude which represents specific locations from City bike API, with P>0.05 are considered statistically significant.




## Challenges 
1. Daily limits to the number of times Yelp Api could be queried
2. Finding the best way to merge the different DataFrames
3. Not being able to include categorical variables in the statistical modelling.
4. Limited time do more in-depth analysis


## Future Goals
1. Retrieve and analyze more location data
2. Work on how to include categorical variables into the statistical modelling.
3. Build a more robust data base from the POI data

