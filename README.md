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

_ML models are solved based on mathematical equations which means the data should be in numbers. The dataset will not always be numerical. The data might contain categorical or text data also. These data need to be converted to numerical before loading into ML model._

 * The categorical variable of independent features (Company) is encoded by using OneHotEncoder class from scikit learn.
 * The categorical variable of dependent feature (Purchased) is encoded by using LabelEncoded class from scikit learn.
 * Why these two are used are mentioned in the code.

5. __Dataset split into train and test set__

 * The algorithms of Machine learning learn from the data and predict the respective outcomes. 
 * For this, the data is splitted into training and testing data. The algorithm is applied to the training dataset for the model to learn and then the model is validated by predicting on the testing data. From this the metrics are evaluated.
 * In python, model_selection object from scikit_learn class splits the data into training and testing data. The testing data is specified as 20% of the data and remaining 80% for training data.
 * More the data for training, the machine will get to learn efficiently.

6. __Feature Scaling__

We use standard scaler as the scaling method. This is mainly to avoid higher weightage being assigned to the feature of higher magnitude.

Why StandardScaler?

In our dataset, we can see that Age feature is in a magnitude range < 50 and Salary have a magnitude range of ten thousands. These variables do not contribute equally to the model fitting and might end up in bias. To deal with this problem, standardization is done where the feature will be assigned in the range of values with mean = 0 and std = 1.

Mathematical formula

<img src="https://latex.codecogs.com/gif.latex?$z = \frac{x - \mu}{\sigma}$, where $\mu$ represents meand and $\sigma$ represents standard deviation of the feature./>


