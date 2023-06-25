## B2B2C Company churn predictor
=========================

### Project Overview

``` 
The project consists on a series of algorithms to predict the seller churn of a Latin
American early stage startup. That operates a B2B2C social commerce marketplace, where 
sellers source products on a mobile app and offer them on social media, while the 
company takes care of the product sourcing, delivery, and payment collection/delivery
thereby eliminating inventory risk in a portfolio of wholesale products.
Due to the nature of the business, seller churn (not placing an order for 30 days)is
quite common. 
This model consists of a churn predictor algorithm that segments sellers who are likely to churn (i.e., not place any orders) each month. This was performed in two (seller retention starting June 2022, y values removed)  iterations, the first one analyzing sellers created after June 2021 and the second one, for sellers created after October 2022. For this document I will focus only on the second one, which is most relevant for the company.

```

### Project Data
   ``` - seller ID:
    		- Type: int
			- seller unique ID
		- total orders:
			- Type: float
			- total orders regardless of the order state
		- effective ratio:
			- Type: float
			- completed, created, in distribution orders / total orders
		- RTO ratio:
			-  Type: float
			- Orders returned to origin (client did not pay in cash on delivery) / total orders	
		- Cancelled ratio:
			- Type: float
			- cancelled orders (either by client, vendor or seller returns) / total orders
		- deparments sold:
			- Type: float
			- number of different departments (regions) where the seller has sold
		- number of clients:
			- Type: float
			- number of different clients per seller
		- avg effective delivery days:
			- Type: float
			- average delivery days for effective orders
		- total effective earnings:
			- Type: float
			- aggregate seller earnings for completed orders (COP)
		- avg effective earnings:
			- Type: float
			- average seller earnings per completed order (COP)
		- avg client price:
			- Type: float
			- average end client price (COP)
		- avg shipment cost:
			- Type: float
			- average end client shipment cost per order
		- total discount:
			- Type: float
			- total amount of discounts used by the seller (COP)
		- avg discount:
			- Type: float
			- average   discount used by the seller per order (COP)
		- order last month:
			- Type: int (binary)
			- target variable
			- Has the seller placed an order in the last month of data
		- has referred:
			- Type: int (binary)
			- has the seller used her referral code to bring new sellers
		- avg cart items:
			- Type: float 
			- number of products per cart item (not necessarily completed orders)
		- avg vendor discount:
			- Type: float
			- average   discount provided by the vendor (COP)
		- number of sold products
			- Type: int
			- total different number of products sold by the seller
		- number of categories
			- Type: int
			- total different number of categories with >=1 order by the seller
		- avg product existence days
			- Type: float
			- avgerage number of days since the product was added in the marketplace until the seller decided to sell it
		- total products shared
			- Type: int
			- total different number of products shared by the seller on social media / e-commerce
		- number of used credits
			- Type: int
			- total number of credits used by the seller

* `model`
    - joblib dump of final model, containing the final XGBoost and Random Forest

* `notebooks`
    - 00 SQL queries to extract the data from the dump
    - 001 Data wrangilng for both iterations
    - 002 EDA for iteration 1
    - 003 Pre-processing notebook
    - 004 Modelling
    - Model evaluation

* `reports`
    - contains final report which summarises the project

* `.gitignore`
    - Part of Git, includes files and folders to be ignored by Git version control

* `capstine_env.yml`
    - Conda environment specification

* `Makefile`
    - Automation script for the project

* `README.md`
    - Project landing page (this page)


### Dataset

Dataset link: https://drive.google.com/drive/folders/1QGwsvxgVX4mRjP8l4jhbcIZhQIKBwCy1?usp=sharing


--------
