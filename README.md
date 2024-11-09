# Attention-Based-CNN-Model-for-Code-Smell-Detection

Model Description:

We have developed a sequential model for code smell classification work to implement the deep neural network. It has 7 layers in total. Below are all 7 layers that we have defined in our model.
-	The first layer of the model is a 1D CNN layer having 128 filters and a kernel size of 1. The activation of the neurons has been done using the activation function ‘ReLU’.
-	Another layer of 1D CNN layer has been used as the second layer in our model. The second layer has 64 filters with kernel size 1. The neurons of this layer have been activated using “tanh” as the activation function.
-	As for the third layer in the model, we have added an attention block. It is a self-attention block that assigns attention weights to different parts of the input. Thus, making some parts of the input data more important than other parts.
-	For the fourth layer, a flatten layer has been used. The purpose of this layer is to connect the convolution layer with the dense layers.
-	The fifth layer of the model is a dense layer. This layer has 64 filters. The neurons of this layer activate using the activation function “ReLU”.
-	In the sixth layer of the model, we have defined a dropout layer. This layer drops out 40% of the neurons to prevent overfitting the model.
-	As for the final layer, we have used dense layer in our model. It is the output layer of our model. So, for this reason, it has only one filter and uses the activation function “sigmoid”. Since our aim is to get a binary prediction.

Model Compilation, Training and Evaluation:

Compilation:
The compilation of the model has been done using the optimizer “adam”. This optimizer helps to set a good learning rate for our model through adjustments during the learning phase. We also used “binary crossentropy” as our loss function. 

Training:
For training the model, fit() function have been used. As for its parameter, we have given the training data, labels of training data, batch size and epochs. For the batch size we have set it to 2 and as for the epoch we have considered it 32. Our model was trained separately for each of the datasets based on these exact parameters.

Evaluation:
After training the model with the training data and its labels, we have made the model to do prediction first on the validation data and then on the testing data. For this, we used the evaluate() function. Thus, we were able to obtain the accuracy of the model.
