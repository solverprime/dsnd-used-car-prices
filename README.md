# Used Car Analysis
The main purpose of this project is to tease out how the price of used cars is driven by its features, such as its vintage year, its odometer reading etc. 
We build a model to predict the price of a car based on its features. The predicted price can be compared to the listed price of a new car to determine whether it is overpriced or underpriced.
This repo contains [Craiglist's Used Cars]( https://www.kaggle.com/austinreese/craigslist-carstrucks-data) dataset.

# Blog post
See the blog post on [Medium](https://witty-latte-bat-528.medium.com/what-drives-the-pricing-of-used-cars-88a1215122c3).

# Installation
The notebook uses Python Python 3.7.10. 
The following libraries are used within the notebook:

* scikit-learn==0.22.2.post1
* pandas==1.1.5
* seaborn==0.11.1
* numpy==1.19.5
* google==2.0.3
* missingno==0.4.2
* matplotlib==3.2.2

The notebook is organized into chapters. The main sections are loading and cleaning data and then building and predicting car prices using linear regression model.

# Data
The  [Craiglist's Used Cars]( https://www.kaggle.com/austinreese/craigslist-carstrucks-data) dataset contains relevant information on car sales on Craiglist. The main column of interest is the price of a car. The other relevant columns include manufacturer, condition and further specifications of the car.

# Files Description
The files included in this project are:
 * Use_car_price_prediction.ipynb - Jupyter Notebook including the main project code.
 * vehicles.csv - used cars dataset 

# Key Observations:
1. The price of a car decreases by $ 912.8 each year, given that all other factors remain the same
2. The price of a car decreases by $ 44.1 for each 1,000 miles a car driven, given that all other factors remain the same
3. The car's manufacturer and the number of cylinders it has cause the largest variability in the price of a car.
4. Other variables that impact the car have low variability in their size.
