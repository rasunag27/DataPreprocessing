# DataPreprocessing

* The data in the real world are generally inconsitent, incomplete and noisy. Feeding this data directly into an ML model will not work. It has to be processed such that the datasets are complete and efficient.
* Data preprocessing is a crucial step before inserting into an ML model.
* In the code, a simple data is used and data preprocessing is done with following steps.
  * Data import
  * Library import
  * Handing missing data
  * Encoding categorical data
  * Splitting the dataset into training and testing data
  * Feature Scaling
* Lets go through the process ony-by-one

Language Used: 

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
</p>

1. __Data import__

 * The dataset present in the code is represented as "data.csv". The data can be loaded directly or from google drive.
 * The data has four columns namely Country, Age, Salary and Purchased with 10 rows/observations.
 * Here, the indepedent variables are Country, Age and Salary and dependent variable is Purchased.
 * The data tells the observation of a customer whether he purchased or not based on customer Country, Age and Salary.

2. __Library Import__

 * Numpy library for mathematical calculations
 * Pandas library for dataframe manipulation
 * Matplotib and seaborn for plotting
 * Scikit learn for data preprocessing and machine learning

3. __Handling missing data__

_Missing values present in the dataset can impact the model performance by creating a bias in the dataset. This has to be properly attained by either filling with proper values or by dropping the observation. But if the observation is dropped, the model might lose its performance._

 * In the present data, the missing data is handled by taking the mean of that particular feature.
 * The Age and Salary had NaN values which is handled by mean of the feature.

4. __Encoding Categorical data__

_ML models are solved based on mathematical equations which means everything should be in numbers. The dataset will not always be numerical. The data might contain categorical or text data also. These data need to be converted to numerical before loading into ML model._



