# facial based neural network for mood recognition.
Communication is key in every aspect! In this era where online conferencing is increasingly being accepted as the new normal, it can be necessary to know people's emotion during communications so that we can ensure everyone is onboard. To do this, I developed an NN model to detect emotions from facial expressions. I managed to achieve an accuracy of 65.35% and 62.22% for the training and validation respectively with a learning rate of 0.01.

I developed a Convolutional neural network (CNN) model for multi-class classification using Keras Sequential model in Keras. The model implemented used supervised learning to train and predict the seven emotions (anger, sad, happy, neutral, disgust, fear, surprise). Four (4) convolutional layers were used with Relu activation function. Each convolutional layer has a max pooling layer followed by a dropout layer which randomly switches off 50% of the neurons to prevent overfitting. The model can be summarized as Convolutional2D – Relu, Maxpooling – Dropout, different filter numbers were used for each convolutional layer. The convolutional layers were used for feature extraction. The output from the fourth convolutional layer was passed through a flatten layer to convert the3D feature maps into a 1D feature vector.Three (3) fully connected layers were used, with the output layer having seven neurons to classify the seven emotions into their respective correct classes. The two hidden layers of the fully connected layer uses the Relu activation function, and the output layer uses the SoftMax activation function. The CNN was compiled and trained using a variable learning rate, epoch of 250, SGD and Adam as the optimizer and categorical cross entropy as the loss function. I also used two different datasets, the FER2013 dataset and CK plus each having seven class of emotions. The emotions were labelled 0 to 6. I splitted the dataset into 80% train data and 20% validation data.

The shortcoming of using the FER2013 dataset was its inability to obtain a high accuracy for the validation accuracy and the model tends to overfit despite the different learning rate, batch size and CNN model used. The reason could have been that the features provided for each class of emotion could not best describe the emotions accurately. With implementing the CNN model with the CK plus dataset, the model performed very well getting the highest accuracy of 87.77% for training and 92.39% for the validation. However, the model took a long computational time to achieve this performance.
