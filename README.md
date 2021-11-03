# Project Goal
We hope to provide price prediction service for users planning to go to New York and use Airbnb, and predict reasonable prices for them according to customers' requirements, so as to prevent them from choosing inappropriate houses and improve users' experience. Because money is one factors that travelers care about, this project use three different models to predict the price to help people make decision.

# Methods
At first, we tidy the data and clean csv file, and choosing useful columns. How we choose independent variables? We only use business thinking to select variables which we think it having correlation with price. Later, we use R to run different model to predict Airbnb price. And choose best model by lowest MSE.  

- <b>Data Preprocessing</b>  
  
1. Check NA value. Insert 'mean' to those missing value. We also can consider to use median/mode/KNN model prediction.  
2. Check outlier. Outliers are those data points located above or below 1.5*IQR. We separated outliers to other groups. On the other hand, We also can consider deleted them or used binning method to categorized variables that had outliers.  

- <b>Fit models</b>  

1. Linear Regression: MSE is 4453.323. We can see the result that minimum nights, neightbourhood group, and room type are all significant variables.  
2. KNN models: MSE is 2856.387. We use for-loop to tune the best k value 20, and get the lowest MSE model.  
3. Regression Tree: MSE is 2560.49. According to tree plot, if we want to save money to find lowest price, we should choose "minimum nights < 1.5" which means one night stay at NY and reviews numbers should be greater than 9. 


# Conclusion
During the tests, we found Decision Tree is the most easiest model to interpret because we can see the tree plot and answer YES or NO to make the decision. After we compare MSE during three models, we choose Tree to become our best model to predict price. 

# Resource
Data is from Kaggle. 
