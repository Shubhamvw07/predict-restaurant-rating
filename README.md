# predict-restaurant-rating 
Predicting Restaurant Ratings using Machine Learning Algorithms

Dataset link : https://drive.google.com/file/d/15ZOqfBTam2MlGjQ8HF1NVrH8UaOnZoay/view?usp=drivesdk
Report in IEEE Format : https://drive.google.com/file/d/1VLq1Svyedk-prm9M4bHYtJ1wny0OSkua/view?usp=sharing

Nowadays, starting a restaurant project in a given location requires a large investment by investors and effort. To start a new restaurant, you need funding from investors, who look at a lot of things before deciding to fund your restaurant. A few of those criteria are location, menu, rating of similar restaurants, etc. To help restaurant startups in Bangalore, we decided to experiment with the Zomato Bangalore Restaurants database, to see if we could draw conclusions about how location, food type, etc could affect the ratings of a restaurant.

Description of the dataset : The dataset consists of 51717 rows and 17 columns. Column Description : url : Contains the url of the restaurant in the Zomato website. address : Contains the address of the restaurant in Bangalore. name : Contains the name of the restaurant. online_order : Whether online ordering is available in the restaurant or not. book_table : Table book option available or not. rate : Contains the overall rating of the restaurant out of 5. votes : Contains the total number of rating for the restaurant as of the mentioned date. phone : Contains the phone number of the restaurant. location : Contains the neighbourhood in which the restaurant is located. rest_type : Restaurant type. dish_liked : Dishes people liked in the restaurant. cuisines : Food styles, seperated by comma. approx_cost(for two people) : Contains the approximate cost for a meal for two people. reviews_list : List of tuples containing reviews for the restaurant, each tuple consists of two values, rating and review by the customer. menu_item : contains list of menus available in the restaurant. listed_in(type) : type of meal. listed_in(city) : Contains the neighbourhood in which the restaurant is listed.

Data Preprocessing : Our data consisted of quite a few null values. To solve the problem of missing values, we followed the following steps : (i) First we removed all rows containing null values in the ‘cuisines’ column. (ii) For the second step, since the ‘address’, ‘phone’, ‘url’, ‘listed_in(city)’ columns had a lot of null values, we dropped these 4 columns. (iii) The third step was renaming the ‘approx_cost(for two people)’ and ‘listed_in(type)’ columns as ‘average_cost’ and ‘listed_type’

After performing a few visualizations to understand our data better, we split the data into 80% training data and 20% test data. Next, we used Machine Learning models to fit the data.

The various regression algorithms used to build the model are : linear regression, random forest regression algorithm, ridge regression, lasso regression, KNN algorithm, Support vector regression (SVR) and Bayesian regression.

Linear regression : Simple linear regression involves only one dependent and one independent variable. It can be represented as :

Y = a + bX (1)

where X is the independent variable and Y is the dependent variable. b represents the slope of the line and a is the intercept.

Random forest regression : The random forest regression algorithm combines the decisions and forms a sequence of base models. The model is formulated as follows :

g(x)=f0(x)+f1(x)+f2(x)+... (2)

where g is the sum of the base models fi.

Ridge Regression : Ridge regression is a variation of linear regression. It is used to solve multicollinearity in multiple regression. The equation for ridge regression is written as :

Y = XB + e (3)

where, Y is the dependent variable, X is the independent variable, B represents the regression coefficients to be estimated and e represents the errors.

Lasso Regression : It is a variation of linear regression that involves shrinkage.

KNN Regression : A simple implementation of KNN regression is to calculate the average numerical target of the K nearest neighbours.

Support Vector Regression(SVR) : SVR is similar to support vector machines with insignificant variance. Eventually, the error is reduced by individualizing the margin.

Bayesian Regression : Another variation of linear regression which uses probability rather than point estimates. The model is constructed as follows :

P(β|y, X) = P(y|β, X) * P(β|X)/P(y|X) (4)

After modelling the data, we found that Random Forest regressor fit the best. But to increase the regression score, we used one hot encoding and got a regression score of 93.22.
