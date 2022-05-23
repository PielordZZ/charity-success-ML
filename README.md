# Deep Learning for Donation Efficiency Using TensorFlow

AlphabetSoup (AS) is a loan company targiting charity orginizations.  Charity loans are relatively high risk since the goal of any charity is not to make money meaning the risk of default is much higher than in other industies.  To make sure loan defaults are kept to a minimum AS is implementing machine learning models to make predictions on loans from application statistics.  Tensorflow is an open source easy to use library that creates Neural Network models and will be used for the machine learning model.

### Implementing a Neural Network (NN)

To allow a NN to make predictions the data must be converted from categorical data to numerical data in one way or another.  The approach used here was to bin categories with low rates of occurence together then use pandas get_dummies function to create boolean representations for each category.  

### Refining a Neural Network

To properly refune the models hyperparameters an auto tuner was used to predict the best shape of the model.  