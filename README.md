# Deep Learning for Donation Efficiency Using TensorFlow

AlphabetSoup (AS) is a loan company targiting charity orginizations.  Charity loans are relatively high risk since the goal of any charity is not to make money meaning the risk of default is much higher than in other industies.  To make sure loan defaults are kept to a minimum AS is implementing machine learning models to make predictions on loans from application statistics.  Tensorflow is an open source easy to use library that creates Neural Network models and will be used for the machine learning model.

## Implementing a Neural Network (NN)

To allow a NN to make predictions the data must be converted from categorical data to numerical data in one way or another.  The approach used here was to bin categories with low rates of occurence together then use pandas get_dummies function to create boolean representations for each category.  Before running a model variables must be removed to reduce noise from the samples.  The is_successful variable cannot be removes since it is the target for what we want.  The 'other' categories were removed since they can have a wide veriety of different categories which are not all similar to each other.  In addition low income amounts, small affiliation categories, and no special considerations were removed since I believe they may have the least consistent impact on predictions

## Refining a Neural Network

To properly refune the models hyperparameters an auto tuner was used to predict the best shape of the model.  This gave a 5 layer network with sigmoid activation functions with 5-35 nodes per layer.  Despite robust hyperparameter choices this did not substantially improce the model and did not reach my performance criteria.  since an auto fiting function was used attempting to put in more layers or nodes may just cause overfitting and not achieve better results,

## Conclusions

Looking at this model there is clear potential in its use however figuring out a better set of features to train on would be critical to creating a usable model for industrial cases.  Other ML models like logistic regression could work however the potential for over fitting in non advanced methods would be even higher and since that was our biggest problem any model used should first take steps to further reduce noise before implementation.