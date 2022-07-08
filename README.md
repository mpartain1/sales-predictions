# Predict Store Sales Based on Variety of Factors

## This project analyzed variables such as outlet size, item weight, and more to predict item sales across small, medium, and large stores.

### Author: Marcus Partain

### Business Problem: Aiming to maximize store revenue by finding which combination of variables lead to the highest selling product.

### Data: The data is titled Big Mart Sales Prediction and comes from the website Analytics Vidhya.  It was originally intended to be used in competition.

## Methods:

Prepared data by dropping all duplicate rows, imputing missing item weights with the average item weight, and imputing missing store sizes according to overall sales, assuming higher sales corresponds to larger stores.  I also ensured that column within the same category were consistent.

I then ran some interesting visualizations.  First, I used a correlation plot to see which variables were most correlated among sales, year, MRP, visibility within the store, and weight.  I found that an item's price was most correlated with that particular item's sales.  I also wanted to see how soft drink sales were affected by their visibility within the store using side by side box plots comparing more and less visible soft drinks.  As expected, we found that soft drinks with above average visibility sold more but also had a greater spread of sales than soft drinks with less than average visibility.

## Visualizations Described Earlier:

<img width="435" alt="Screen Shot 2022-07-07 at 7 03 02 PM" src="https://user-images.githubusercontent.com/105669219/177901921-d19fcce1-9f2c-4288-a19b-35918f7a7d86.png">

<img width="486" alt="Screen Shot 2022-07-07 at 7 03 18 PM" src="https://user-images.githubusercontent.com/105669219/177901942-cbcaa262-476d-48cc-a78d-cf0c651cdbc3.png">

## Model

I also tested out a couple machine models (linear regression, decision tree regression) to determine which would be the most effective in predicting sales.  I found the optimal depth for the decision tree and then used this tuned model to obtain an R^2 value of about 0.6 on the testing set.  Between the linear regression and decision tree, the models are not too far off from each other in terms of effectiveness.  From the R^2 values, the decision tree is the strongest model because of the consistency in R^2 values between the training and testing sets, as well as a higher R^2 value in the testing set when compared to the linear regression.  However, the linear regression has a smaller RMSE on both the training and testing sets when compared to the decision tree at about 1/2-1/3 the size for each set.  I feel that R^2 is the more important metric here as it tell us in percentage terms how much of the variation is explained by each model, and because R^2 is higher for the decision tree, I would argue that the decision tree is the model to use.

I hope you enjoy this project!
