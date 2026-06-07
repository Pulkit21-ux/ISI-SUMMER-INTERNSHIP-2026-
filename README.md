# ISI-SUMMER-INTERNSHIP-2026-
Hi! This repository contains my project for the IDEAS - institute of data engineering, analytics and science foundation summer internship.
The assignment was split into two main machine learning tasks: building a regression model to predict used car prices, and using clustering to group handwritten digits.All the code is inside the notebook uploaded here.

Part 1: Used Car Price Prediction (Regression)
For this part, I worked with a dataset of used cars. Before feeding it into a model, I had to do a decent amount of data cleaning:
a. Cleaning text and numbers: I removed symbols like $ and mi. from the price and mileage columns so the computer could read them as actual numbers.
b. Handling missing data: I standardized all the weird missing values (like dashes or blank spaces) into a single Unknown category.
c. Feature engineering: I created a new car_age column by subtracting the model year from 2026.
d. Dropping rare values: For the transmission and exterior color columns, I grouped any rare categories that made up less than 1% of the data into an 'others' group to keep things clean. I also dropped outliers in the top 1% of prices.
After prepping the data and encoding the text labels, I trained a Random Forest Regressor (with 100 estimators) on an 80/20 train-test split.
My Model Results:

R² Score: 0.7417889067802742

Mean Squared Error (MSE): 357725716.71522313

Mean Absolute Error (MAE): 9983.115037783375

Part 2: MNIST Digit Recognition (Clustering)
The second task was a shift to unsupervised learning. I loaded the classic MNIST digits dataset from sklearn.
I used a K-Means Clustering model (set to 10 clusters) to see if it could naturally group the images of handwritten numbers (0-9) based purely on their features.
To check if the clustering actually worked, I mapped each random cluster to whatever the most frequent true label was inside that group, and calculated the F1 score.
Clustering Result:
Macro-averaged F1 score: 0.8627854786352394
How to run this
If you want to run the code yourself, just clone this repo, make sure you have the used_cars.csv dataset in the same folder, and run the 15-Used_Car_Price_Prediction_Summer_2026.ipynb notebook cell by cell.

Thank you
