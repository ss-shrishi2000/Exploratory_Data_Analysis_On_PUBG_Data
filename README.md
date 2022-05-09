# PUBG Finish Placement Prediction Data

<h3 align = "left" >A prediction model built with the help of Exploratory Analysis to be used for predicting the final placement of a list of PUBG Players using their previous game statistics.  <br> </h3>
  <div align = "left" padding = 100px fontsize=40px color="blue" >
  
 **1. Exploratory Data Analysis On the dataset.**   <br> 
 **2. Feature Or Attribute Study Of the data.**  <br>
 **3. Contributions of data attribute to the final placement of the PUBG Player.** <br>
  **4. Prediction Model Based On Random Forests.**   <br>
  **5. Determining the Winning Percentile of All Players In The Game.**  <br>
  <br>
  </div>
  
  ![alt text](https://github.com/ss-shrishi2000/Exploratory_Data_Analysis_On_PUBG_Data/blob/main/pubg-pic-1.jpg)

# Base Machine Learning Models

## Loss Function
Mean Absolute Error (MAE) measures the average magnitude of the errors in a set of predictions, without considering their direction.

For example, a MAE of 0.04 signifies that the average magnitude difference from the prediction to the true value is 0.04. In context of our dataset, this would typically mean that the average error is off by 4 placements. This loss functions provides an appropriate measure of our model prediction accuracy.

## Models

In our modeling process, we wanted to start off with a basic model to have a benchmark for more complex models. We tried Linear Regression to see if a simple linear relationship could predict effectively for our problem.

Linear Regression becomes inaccurate when many outliers are present in the data, so the first step was to remove these. In our data analysis, we managed to identify outliers like cheaters and custom game modes which made removing these outliers easier. Many of the features we had were also heavily skewed. For example, the distribution of damage done for a player peaks at 0 and decreases as the damage done increases. 
After deskewing these features, we finally had our data properly formatted to run Linear Regression.

Training on the whole dataset, we were able to get a public score of 0.0445. Although this model did not perform very well, we still wanted to see what features the model valued when making predictions. From the below chart, we can see that boosts and heals were the most important features. Three of the top six most important features were also created by us in the feature engineering step, reinforcing that our feature engineering was providing value.
  
  ![alt_text](https://github.com/ss-shrishi2000/PUBG-Finish-Placement-Prediction-Data/blob/main/Correlation.png)
