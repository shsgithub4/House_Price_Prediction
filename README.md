# Project Name
Surprise: US-based housing company - Advanced regression model for the prediction of price of houses in the Australian market.

## Table of Contents
* [General Info](#general-information)
* [Conclusions](#conclusions)

## General Information
A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. For the same purpose, the company has collected a data set from the sale of houses in Australia. The data is provided in the CSV file, train.csv.

The company is looking at prospective properties to buy to enter the market and wants to know:
--> Which variables are significant in predicting the price of a house, and
--> How well those variables describe the price of a house.

Also, determine the optimal value of lambda for ridge and lasso regression.

Business Goal:
Build a regression model using regularisation in order to predict the actual value of the prospective properties with the available independent variables and decide whether to invest in them or not. This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.

## Conclusions
Important features selected after following Linear Regression using RFE, Ridge & Lasso are as follows:
	LotFrontage - Linear feet of street connected to property
	LotArea - Lot size in square feet
	OverallQual - Rates the overall material and finish of the house
	OverallCond - Rates the overall condition of the house
	MasVnrArea - Masonry veneer area in square feet
	BsmtFinSF1 - Type 1 finished square feet
	1stFlrSF - First Floor square feet
	2ndFlrSF - Second Floor square feet
	LowQualFinSF - Low quality finished square feet (all floors)
	GrLivArea - Above grade (ground) living area square feet
	BsmtFullBath - Basement full bathrooms
	FullBath - Full bathrooms above grade

Features that are positively increasing the sales price:
1 LotFrontage
2 LotArea
3 OverallQual
4 OverallCond
5 MasVnrArea

Features that are negatively influencing the sales price:
1 SaleCondition: Alloca --> Allocation - two linked properties with separate deeds, typically condo with a garage unit
2 SaleType: Con --> Contract - 15% Down payment regular terms
3 GarageQual: Garage quality
4 GarageFinish: Interior finish of the garage
5 GarageType: Garage location

### Evaluation Results:
Alpha --> Ridge = 3 | Lasso = 100

| R2 Score   | Linear Regression      | Ridge Regression   | Lasso Regression   |
| ---------- | ---------------------- | ------------------ | ------------------ |
| `Train`    | 0.878618857696672      | 0.8718507878152617 | 0.8689176078722685 |
| `Test`     | -1.493302343420395e+21 | 0.8382464361790748 | 0.8439859315028525 |

### Outcome:
Lasso regressin model is giving decent R2 scores in both Train & Test data, so, it's advisable to go with this model due to following reasons:
1) The error terms are normally distributed
2) There is a linear relationship between the selected features
3) All the selected features are independent
4) Error terms are randomly distributed and homoscedastic in nature

## Contact
Created by [@shsgithub4] - feel free to contact me!
