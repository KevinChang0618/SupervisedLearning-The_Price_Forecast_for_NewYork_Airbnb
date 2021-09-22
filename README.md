# Project Goal
- We hope to provide price prediction service for users planning to go to New York and use Airbnb, and predict reasonable prices for them according to customers' requirements, so as to prevent them from choosing inappropriate houses and improve users' experience. Because money is one factors that travelers care about, this project use three different models to predict the price to help people make decision.

# Methods
At first, we tidy the data on cleaning csv file, dropping some missing values, and choosing useful columns. How we choose independent variables? We only use business thinking to select variables which we think it having correlation with price. Later, we use R to run different model to predict Airbnb price. And choose best model by lowest RMSE.  

- Linear Regression: RMSE is 164. We can see the result that minimum nights, number of reviews, neightbourhood group, and room type are all significant variables. According to the model, living in Manhattan is the most expensive choice.
![image](https://user-images.githubusercontent.com/67025904/134411260-218ee73d-9365-47f5-a051-20ceeb1c4574.png)

- Regression Tree: RMSE is 207. According to tree plot, if we want to save money to find lowest price, we should choose "minimum nights < 1.5" which means one night stay at NY and reviews numbers should be greater than 9.  
![image](https://user-images.githubusercontent.com/67025904/134411679-68e51361-eb30-4f5c-9c4d-14d6383762fd.png)

- KNN models: RMSE is 212. We use for-loop to find the best k value to get the lowest RMSE model.
![image](https://user-images.githubusercontent.com/67025904/134413247-835d699f-7b78-42a9-a1b0-af3e477d5ec5.png)

# Conclusion
- During the tests, we found Tree is the most easy model to interpret because we can see the tree plot and answer YES or NO to make the decision. After we compare RMSE during three models (Linear Regression with 164; Regression Tree with 207; KNN model with 212), we choose Linear Regression being our best model to predict price. 

# Resource
Data is from Kaggle.
