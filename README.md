# Honda-Analysis
This project is part of my data science portfolio and was created to showcase some of the skills I have learned since I started my journey into programming and data science!

### Introduction
The purpose of this project is to create a prediction algorithm using a Linear Regression for used Honda cars in the United States. 
Specifically, prices will be predicted based on data from vehicles such as mileage, year, MPG, fuel type, and more.
Metrics will be used to determine how well the model predicts, such as accuracy and how much error the predicted values have.

### Methods Used
* Data Visualization
* EDA (Exploratory Data Analysis)
* Data Cleaning
* Linear Regression
* Scaling, Standardization, One Hot Encoding
* Feature Selection
* Metrics (Accuracy, Error)
* Regularization

### Technologies
* Pandas
* Python
* Matplotlib
* Jupyter Notebook
* SkLearn
* Seaborn
* GridsearchCV
* Lasso Regularization


### Project Description
The .csv file was obtained from Kaggle at this address: `https://www.kaggle.com/datasets/omartorres25/honda-data`. The file contains data on listed used honda cars with 25 total columns after creation of the dataframe. Some of the columns include: Year, Price, Mileage, VIN, Drivetrain, Consumer rating, Interior and Exterior Color. A few columns are not useful for the regression, such as VIN, because this can't be used to predict the price of the vehicle. Data cleaning will be necessary for imputing null values, removing unnecessary columns, and modifying incorrect data types.

Summary statistics and graphs will be used to get a sense of how the variables influence the price, and how much correlation they have. This will be important for feature selection even before running any analysis. 

Once the data is ready for analysis, a multiple linear regression will be created with the final variables. The accuracy will be calculated using the built-in function for LinearRegression from Sklearn, and compared as the model is revised. Other metrics such as root mean square error (RMSE) and Mean Absolute Eror (MAE) will give a sense of how far off the predictions are with respect to the actual values.
The MAE will provide a number in the same unit as Price ($), so it can be interpreted as how far from the actual value the prediction is on average. 

### Conclusion

The main goal of the project was reached, and the linear regression has a good score (around 0.80 for the train and test data), with a reasonable MAE and RMSE.
The MAE of the final model was 3273, meaning on average, the price predicted was $3273 from the actual value. With the average price of a vehicle in the dataset being $33,600, this means that for any given prediction, there would be about +/- 10% error.

Given this amount of error, the regression could be used as a tool to predict how much a vehicle's value should be based on the characteristics. Although it won't be able to predict the price exactly, this model could be used to give an average, with a range for any specific vehicle.

Improvement could certainly be made by doing some of the following:

- Increasing the amount of data points, with more kinds of vehicles if possible, and older vehicles specifically
- Using some of the features that were dropped, such as color and different ratings
- Feature engineering to combine some features into a new distinct feature
