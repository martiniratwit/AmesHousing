# Introduction
The project was primarily undertaken to improve upon analyzing data and optimizing regression models. 
The purpose of this project was to predict housing prices using the Ames housing dataset often used as an alternative to the Boston housing dataset. 
This dataset was chosen for its abundance of analysis potential.

# Selection of Data
The dataset originally contained 81 features and 1460 samples. 
The Ames housing dataset was retrieved from Kaggle along with a file describing each of the features. 
Features of the data included “Id”, “MSSubClass”, “MSZoning”, “LotFrontage”, “LotArea”, “Street” and etc. 
The data contained numerous missing values and required to be cleaned. 
The features "Alley", "MiscFeature", "Fence","PoolQC" contained a majority of missing values and were therefore discarded. 
While the feature “Id” only counted the entries and was not useful for performing regression.

The remaining rows containing missing values were dropped rather than replaced. 
The “Sales Price” was stored into y while the remaining data was stored into X with categorical features converted using one-hot encoding. 
This increased the size of the data.

# Methods
The project contained a variety of technologies and libraries utilized in class, including NumPy, Pandas, Matplotlib, Seaborn, and Scikit-learn.
OneHotEncoder and ColumnTransformer were utilized from Scikit for feature engineering.
Linear_model with train_test_split was also utilized from Scikit to train the models and mean_squared_error with r2_score to evaluate them.
The data analysis portion utilized mostly bar plots and scatter plots from matplotlib and seaborn along with a correlation matrix.

# Results
The project allows predictions to be performed either through a csv or by manual input from the user.
The optimal model turned out to be lasso regression with a slightly higher R2 score of 0.829 from linear regression’s score of 0.815.
Observing the predicted price to the actual price, a linear relationship between the model and test data  of linear regression is observable.
Other insights were noted in data analysis such as outliers all consisting of the same “MSZoning” or collinearity between features such as “YearBuilt” and “OverallCondition”.

# Discussion
Although numerous techniques have been utilized, it was difficult to raise the R2 score of the models beyond 0.829. 
Removing outliers and features with high colinearity were considered to optimize the model, however these generally seemed to remove too much data. 
The R2 score was likewise increased by adding back “LotFrontage” which I had initially removed from cleaning. 
I believe too much data was removed and making further efforts in data imputation may increase the accuracy of the model. 
Similar models on the kaggle site utilized numerous other methods such as  Ridge, ElasticNet, XGB, etc. achieving closer scores to 90.

# h1 Summary
Overall the project was successful in creating predictions of housing prices using the techniques discussed in class. 
It served as good practice in processing and plotting data. 
The model can be utilized either by passing a csv file of all the features into it or by entering all the inputs manually via the script in the last cell. 
