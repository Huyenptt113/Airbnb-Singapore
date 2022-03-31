# Prediction of Airbnb listing price per night in the Central Region of Singapore

# Problem & motivation:
* Nowadays, the dominance of the Internet and booking platforms is growing year by year since more and more tourists book their hotels online. Airbnb is a booking platform for listing and renting local homes. Since both hosts and travelers can easily exchange services on Airbnb, a good pricing strategy could create a competitive advantage for hosts.
* This report aims to help the listing owner set a reasonable price by predicting the price per night based on host information and the room/flat information and using different machine learning models.

# Dataset:
The raw dataset of the project is the detailed listing data in Singapore that are publicly available data from the Airbnb website (http://insideairbnb.com/get-the data.html). The dataset has been updated since 26th December 2021.

# Aim of study:
The project aims to answer the question: how much could an Airbnb host charge per night in the Central Region of Singapore?

# Project plan:  

## Data preprocessing:  
* Choose listings in Central Region
* Remove empty rows, retain important 17 columns  
* Correct data type    
* Save the data  

## Data visualization (EDA)  

* Draw histogram, boxplot, scatterplots
* Create correlation table, draw heatmap
  
## Modeling  

* Apply Linear Regression model with k-fold  
* Hyperparameter tuning for Polynomial Regression model with Ridge Regression as Regularization
 
## Model validation and comparison

* Compare train and test sets of each model  
* Find the best model
* Apply the optimal model on test set  

# Results

* For the Linear Regression model, the training mean absolute error was 97.023. The validation mean absolute error of the linear model when tested against the validation set was 98.4137.
* For the polynomial Regression Model, the optimal alpha for the regularization is 0.0616. The polynomial regression model with a degree of 3 has the lowest validation loss of 94.69.
* The mean absolute error for the final model and the test data is roughly 92.14.

# Limitations on the analysis:

* The project focused on the regression model, so the full potential of other models for predictions in the data set at hand should be explored in future research endeavors, such as Decision Tree Regressor or Deep Learning methods.
* Other methods of feature selections, such as PCA or Lasso, could be tried in this problem since there were a total of 17 features, but they only have little correlation to the label values. 
* The model's performance was also affected by the limitation of the dataset. The data need to be gathered more to improve the models' performance.
