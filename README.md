# Team 6: Kobe Bryant Shot Detection

## Main Structure

The main pipeline of this project can be found in the `Sklearn_Pipeline.ipynb`. It contains all the preprocessing steps done on the dataset, the visualizations created, the training and results of each model, and finally a ROC curve for our most accurate model. While there are many other ipython notebooks in this repository, this is the most important one as it contains our final solution.

The other important notebook to look at is `Time_Series.ipynb`. After dropping unnecessary columns, this notebook trains a Gradient Boosted model and a Neural Network iteratively on the data. The models are trained on each game, and after going through the dataset, the evaluation metrics are run. These model instances in particular only predict whether or not Kobe Bryant made the shot based on the games already played, not based on all the games in the dataset, meaning games that occur in the future are not influential.

## Other Notebooks in the Repository

- Kobe.ipynb
  - One of our first files created. This file produced our main visualization we referred to when we began preprocessing the dataset. This visualization shows the correlation between the many features of the dataset, making it easier to see which features were redundant.
  
- All_Pyspark.ipynb
  - Contains our Logistic Regression and Gradient Boosted models with the Pyspark ML library (different than Pyspark ML Lib library) along with some Sklearn metrics of both.
  
- sklearn.ipynb
  - Test notebook to see how difficult or easy it would be to convert our previous models into models using the Sklearn library. Evaluation metrics were run on two sets of data, the preprocessed data with one-hot encoding and with ordinal encoding. All that needs to change is line 2, where the CSV file is being read in.
  
- predict.ipynb
  - Previous file used for created, training, and testing our models when we were using the Pyspark ML Lib library.
  
## CSV Files

- data.csv
  - The main dataset is stored here. This file is imported and preprocessed in almost every ipython notebook.
  
- preprocessed.csv
  - Contains the dataset after one-hot encoding was conducted on categorical features

- preprocessedNN.csv
  - Contains the dataset after ordinal encoding was conducted on categorical features
  
*All other preprocessing tasks on the dataset are performed in each notebook. The preprocessed and preprocessedNN CSVs are only used inside sklearn.ipynb to make it easier when deciding which encoding should be used moving forward.*

- kaggle.csv
  - Only contains shot_ids and shot_made_flag values.
  
- sample_submission.csv
  - This is the CSV file we would submit to Kaggle if we were participating in the competition.
