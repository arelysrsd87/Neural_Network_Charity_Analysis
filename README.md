# Neural_Network_Charity_Analysis
# Overview of the analysis
With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.
## Purpose of this analysis
Using your knowledge of Pandas and the Scikit-Learn’s StandardScaler(), we’ll need to preprocess the dataset in order to compile, train, and evaluate the neural network model. Using our knowledge of TensorFlow, we’ll design a neural network to create a binary classification model that can predict if an Alphabet Soup–funded organization will be successful based on the features in the dataset. Once we’ve completed that step, we’ll compile, train, and evaluate the binary classification model to calculate the model’s loss and accuracy. Using our knowledge of TensorFlow, we'll optimize the model in order to achieve a target predictive accuracy higher than 75%. 
# Results
## Data Preprocessing
- The  variable IS_SUCCESSFUL is considered the target for this analysis model.
- The following variables are considered the features for this analysis model:
	- ORGANIZATION
	- STATUS
	- INCOME_AMT
	- SPECIAL_CONSIDERATIONS
	- ASK_AMT
	- APPLICATION_TYPE
	- AFFILIATION
	- CLASSIFICATION
	- USE_CASE
- The following variables are neither target nor features for this model:
	- NAME
	- EIN
## Compiling, Training, and Evaluating the Model
- For the initail neural network model I selected the following parameters:
	- number_input_features = 43
	- hidden_nodes_layers1 = 80
	- hidden_nodes_layers2 = 30
	- 1st hidden layer activation function = relu
	- 2nd hidden layer activation funtion = sigmoid
	- output layer activation function = sigmoid  
I started with relu as the first activation function as it does better with nonlinear data. Subsequently, I selected the sigmoid funtion because it is used to add non-linearity in a machine learning model, in simple words it decides which value to pass as output and what not to pass. I decided to add two layers to allow the second layer to reweight the inputs from the first layer. Here are the preformance metrics of this model.
- This model acheived a 72.9% accuracy, so the target performance was not met.
![original_nn](https://github.com/arelysrsd87/Neural_Network_Charity_Analysis/blob/main/Images/original_nn.jpg)  
- Steps taken to increase the model performance were:
	- Changing the 2nd hidden layer activation funtion from sigmoid to relu. This model achieved the same accuracy from the original neural network model, 72.9%.
	![attempt1_nn](https://github.com/arelysrsd87/Neural_Network_Charity_Analysis/blob/main/Images/attempt1_nn.jpg)  
	- A third hidden layer was added with 10 neurons and a sigmoid activation funtion. This model achieved an accuracy of 73%.   
	![attempt2_nn](https://github.com/arelysrsd87/Neural_Network_Charity_Analysis/blob/main/Images/attempt2_nn.jpg)  
	- The number of input layers was changed from 43 to the length of len(X_train_scaled[0]). This model achieved an accuracy of 73%, as well.
	![attempt3_nn](https://github.com/arelysrsd87/Neural_Network_Charity_Analysis/blob/main/Images/attempt3_nn.jpg)  
# Summary
After four attempts, I was unable to create a model that could preform a 75% accuracy rating. This is potential becasue I got rid of too many columns, I did not use the correct activation function, or I did not have hte right amount of layers and neurons. These were the main areas I continued the change with little to no improvement. Next time, I would research more about activation functions to make sure that I am always choosing the right one based on the data.