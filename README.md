
# King County Residential Real Estate Bargain Hunting

## Table of Contents
* [General Info](#general-info)
* [Technologies](#technologies)
* [Insights and Business Recommendations](#insights-and-business-recommendations)
* [Further Studies](#further-studies)

## General Info
This project was assigned as the final project for Module 2 (Statistics and Linear Regression) in Flatiron School's Immersive Data Science Program. My self-defined goal of the project is to analyze home sale data over a two year period (2015 and 2016) and find out how a savvy residential real estate investor can gain a foothold in this hot market. 

Housing prices in King County, WA have been exploding over the past decade due to many factors including the availability of great jobs, a rich culture, and a plethora of outdoor recreation opportunities in the surrounding areas. It is now harder than ever for house hunters to find a bargain in what seems like is a perpetual sellers' market.

My goal in this project to determine where and what types of house are still available at decent prices and develop a multiple linear regression model capable of giving the patient investor an indication whether or not he may be looking at a bargain. Meeting this goal will require careful data cleaning, exploratory data analysis capable of answering questions relating to our goal, thoughtful feature engineering, and finally an iterative approach to mutliple regression modelling.

With a median home value of $472k (during the 2015-2016 time period, adjusted for inflation) prices are high but there are still deals to be found. 

![Home Value Distribution](home_value_distribution.png)

## Technologies
This project was created using the following languages and libraries. An environment with the correct versions of the following libraries will allow re-production and improvement on this project. 

* Python version: 3.6.9
* Matplotlib version: 3.0.3
* Seaborn version: 0.9.0
* Pandas version: 0.24.2
* Numpy version: 1.16.2
* Statsmodels version: 0.9.0
* Scipy version: 1.2.1
* Sklearn version: 0.20.3

## Insights and Investment Recommendations

### Buy During the Right Time of Year
ZZ **xx** yy

![Month Sold vs. Sale Price](month_sold_vs_sale_price.png)

### Buy the Right Size Home
xyz

![Top Prodcuers](top_producers.png)

### Shop in the Right Neighborhoods
xyz

![Median Home Value by Zip](median_home_value_by_zip.PNG)

## Final Regression Model
In summary I am somewhat pleased with our final model though there are clearly unseen factors at play here which contribute to home valuation.

**The good**

1. Our final model has an r-squared-adjusted value of 0.79 and utilizes 22 features. Furthermore, using only the top 6 features, our model has an r-squared-adjusted value of 0.77 which means that we may explain 77% of the variance in home prices in the King County area using just those six features which is quite impressive.
2. Our model performs more or less equally well with both test and train datasets implying we have certainly not overfit our model.
3. Normality and homoskedasticity of residuals assumptions are met.

**The bad**

1. Our RMSE is $127k USD! This is not very confidence inspiring considering that the median home value of our analyzed dataset is $472k USD.
2. We eliminated quite a bit of outliers to create a model capable of performing well with our remaining dataset. Our final, trimmed dataset contained only 91% of the original values and our model's accuracy is only proven below the $1.8MM USD price point. However, for our purposes and our price range for investments this is perfectly acceptable. 

## Further Studies
As with all data science projects there is always more work to do. Most notably I've been considering the following. 

### Look at the School Districts
Many wealthy parents are willing to pay more in housing expenses in order to send their kids to top schools. I would be interested in finding data regarding highest rated school districts in the King County area and relate those to our zip code data. We could then create a feature such as 'public_schools' which would assign a rank Tier 1, Tier 2, etc. to each zip code based on the quality of it's public school system.

### Where Are the High Paying Jobs Moving
The city of Seattle is becoming less business friendly with tax increases and it may begin to lose larger companies which will seek offices in locations with lower taxes. With that said I suspect many companies, existing and new, will begin to establish headquarters in more business friendly districts such as Bellevue and Redmond as companies such as Amazon and Microsoft have done. I would be curious to investigate this further.

### Analyze a Longer Time Frame
I would be very interested in seeing the housing prices over a longer time period. For example, it would be very interesting to be able to see housing price trends over a geographic area over a period of time. This could help answer questions such as which areas of King County are beginning to trend upwards.

### Utilize Advanced Regression Methods for Final Model
More advanced models exist which may prove to be more accurate in determing home values. For example, gradient boosted regressors could improve our models accuracy. Furthermore, we were never really risking overfitting our model so it could be helpful to test those boundaries by introducing more features and/or polynomials to our model, test for overfitting, and then attempt to use a regularized model such as ridge or lasso regression. Another option would be to not eliminate the outliers and use robust regression - this would be especially useful if we needed to create a model which will help predict outlier datapoints as well. The options for further analysis in this regard are plentiful.
