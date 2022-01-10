# Medical vs Recreational Cannabis Classifier
#### Classifying people who use medical vs recreational cannabis using a neural network. 

This repository contains the code developed to create a neural network that classifies people who use cannabis exclusively medically, sometimes medically and exclusively recreationally. Three models are included in the code. In the first model the hyperparameters of the model are hard-coded. In the two subsequent models a model builder is created that accepts variations of certain hyperparameters. The first hypermodel is designed to have the optimal number of units per hidden layer (between 16-256). The second hypermodel is designed to have the optimal number of units plus the optimal activation function per hidden layer (relu, tanh, elu, selu, swish). These optimal hyperparameters are identified on the basis of a Keras Tuner search. Each model is trained on the supplied training data and accuracy metrics logged and compared across the models. Finally, each model is given a novel sample from each category in order to predict likely category membership. 

The code was designed to be used with data from participants who indicated their cannabis use status in the [Global Drug Survey 2017](https://www.globaldrugsurvey.com/). The data cannot be shared publically so a dummy dataset has been created that includes 100 samples of each cannabis use category and is included in this repository. The data has been labelled and category labels are available in another CSV file in this repository. 

To run:
1. Ensure you have all of the relevant libraries installed ([Scikit Learn](https://scikit-learn.org/stable/install.html#:~:text=Installing%20the%20latest%20release%20%C2%B6%20%20%20,%20%20install%20%2018%20more%20rows%20), [Tensorflow](https://www.tensorflow.org/install/), [Keras-Tuner](https://keras.io/keras_tuner/)). 
2. Download the Jupyter notebook and the two CSV files in this repository to your working directory.
3. Open the Jupyter notebook and run all cells. 

Each time a model is trained, loss and accuracy values will be outputted for each epoch. When Keras Tuner searches are run to find optimum hyperparameters for each hypermodel, best hyperparameters will be outputted for each epoch, along with the best loss value so far. When the search ends, the time taken to run the search will be ouputted, followed by the best hyperparameters for each hidden layer. Once every model has been trained, a bar chart comparing accuracy values across the models will be outputted. Finally, each model's predictions for the three novel samples will be outputted, with a probability value. 

Note: Some Mac users may experience problems running this code. If so, the code can be run through Google Colab on any device. 
