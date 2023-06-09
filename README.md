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
This model will predict the seller churn, defined as sellers with 1>= orders placed
after june 01 2021, that did not placed an order after may 28 2023.   

```

### Walkthrough Demo

...
...
...

### Project Flowchart

...
...
...

### Project Organization

...
...
...

* `data` 
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
    - joblib dump of final model / model object

* `notebooks`
    - contains all final notebooks involved in the project

* `reports`
    - contains final report which summarises the project

* `references`
    - contains papers / tutorials used in the project

* `src`
    - Contains the project source code (refactored from the notebooks)

* `.gitignore`
    - Part of Git, includes files and folders to be ignored by Git version control

* `capstine_env.yml`
    - Conda environment specification

* `Makefile`
    - Automation script for the project

* `README.md`
    - Project landing page (this page)

* `LICENSE`
    - Project license

### Dataset

...
...
...

### Credits & References

...
...
...

--------
