# Data-Mining-Project

This project was created for my Fall 2019 Data Mining Class at California State Polytechnic University, Pomona.

## The Objective

To determine key features that lead to highly rated products within the brewing industry through the data anlysis 
of over 1,000,000 reviews from the review aggregator site, BeerAdvocate. The dataset was sourced from [Kaggle](https://www.kaggle.com/rdoume/beerreviews).

## The Process
In order to pull actionable information out of this data set we decided to use Multiple Linear Regression to determine
key features that determine what factors contribute to a highly rated product. We also used cluster analysis to 
determine what kinds of divisions there were among the products. 

### Data Cleaning 
In order to properly use our data set we will need to clean it and normalize it for Regression Analysis.
Our dataset is large, so unless there are a large number of empty features, dropping a smaLL number of rows will
have an insignificant impact on our results. Next we will work on model specific cleaning and normalization.

In order to handle the two models we will be creating We need to create two dataframes, one for regression
and one for clustering. We take a 50% sample of our dataset to improve processing times of our regression model. 
Sampling the data set has little affect on our overall results. We also drop columns that have no meaning 
to our regression analysis, in this case identifying information and classifification data. Finally we divide our
data into training and testing data and normalize it.

Our clustering model has differnt parameters. The clustering model does not need identifying information so we 
drop the columnscontaining any information that identifies the profile of the reviewer, the brewery, the beer, 
and the time whenthe review was submitted. Finally we aggregate the data by the means of the columns and group
by whatever categorical data is leftover and normalize our data.

### Regression Analysis
For our multiple regression anaylsis we defined functions to automate model selection. The best model came out 
to be our 3rd of 5 models tested. The results gave us an Adjusted R-Squared of .67 and 3 coefficients that
indicate the 3 key features to highly rated product, Review Pallette, Review Taste, and ABV.

### Cluster Analysis
For our cluster analysis we tested with two models, K-Means and hierarchical. We determined the appropriate number
of clusters to be 3 clusters using the elbow methodology. The three clusters we ultimately determined as high quality
tase, average taste, and low quality taste. 
