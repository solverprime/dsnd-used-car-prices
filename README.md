# Used Car Analysis
The main purpose of this project is to tease out how the price of used cars is driven by its features, such as its vintage year, its odometer reading etc. We build a model to predict the price of a car based on its features. The predicted price can be compared to the listed price of a new car to determine whether it is overpriced or underpriced.

This repo contains [Craiglist's Used Cars]( https://www.kaggle.com/austinreese/craigslist-carstrucks-data) dataset.

# Blog post
See the blog post on [Medium](https://witty-latte-bat-528.medium.com/what-drives-the-pricing-of-used-cars-88a1215122c3).

# Installation
The notebook uses Python Python 3.7.10. The following libraries are used within the notebook:
* scikit-learn==0.22.2.post1
* pandas==1.1.5
* seaborn==0.11.1
* numpy==1.19.5
* google==2.0.3
* missingno==0.4.2
* matplotlib==3.2.2

The notebook is organized into chapters. The main sections are loading and cleaning data and then building and predicting car prices using a linear regression model.

# Business Understanding
The dataset is a very large database of used cars available for sale that provides not just the price but also important attributes of each car: manufacturer, mileage, type of car etc. This dataset is large enough to make useful models on how used cars are priced and gain important insights of how each of the car's attributes impact its price. 

# Data Understanding
The [Craiglist's Used Cars]( https://www.kaggle.com/austinreese/craigslist-carstrucks-data) dataset contains relevant information on car sales on Craigslist. The dataset contains 458,213 cars and 24 columns about each listing. The main column of interest is the price of a car that we model in this analysis. Other relevant numerical columns include year and odometer reading of the car. Relevant categorical columns include manufacturer, condition, cylinders etc.

# Prepare Data
Data cleaning is done in several stages, as described in the Jupyter Notebook of this repo.
On a high-level: filtering is done in order of the usefulness of each column for our modeling prices. Important numerical columns are visualized and filtered according to what seems like obvious bad or missing data. For example, _price_ or _odometer_ readings containing zero are assumed to be bad data and filtered out.

Besides filtering out bad data, data that is considered as outliers is filtered out as well. For example, we filter out cars before the year 2000 because of two reasons: 
1. Bulk of the dataset contains cars from 2000 to 2020
2. There are a significant number of cars from the 1960s, 1970s etc. eras which are although "used cars" fall more in the category of "vintage cars" and more useful as "collectors items" for buyers rather for daily usage. They are less important and in fact make modeling of **used car** prices less effective as these vintage cars are often priced very differently (they increase in value the older they are opposed to decreasing prices of used cars). For example, we have a 1972 Ferrari 246 GT Dino listed for $389,500 which makes it more a collector's item rather than a typical used car.

# Data Modeling
I have used LinearRegression and test_and_split methods and used R-squared as the metric to maximize and find the optimal fit. The best model yields a very consistent 75.03% fit on test for a 75.10% R-squared on the training data. Further improvements in the fit can be achieved by splitting data by manufacturer, category (cylinders and type) of cars.   

# Files Description
The files included in this project are: 
* Use_car_price_prediction.ipynb - Jupyter Notebook including the main project code.
* vehicles.csv - used cars dataset

# Key Observations
1. The price of a car decreases by $ 912.8 each year, given that all other factors remain the same
2. The price of a car decreases by $ 44.1 for each 1,000 miles a car driven, given that all other factors remain the same
3. The car's manufacturer and the number of cylinders it has caused the largest variability in the price of a car.
4. Other variables that impact the car have low variability in their size.
