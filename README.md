# Cat vs Dog ImageClassification using CNN and transfer learning 

This is part of the kaggle competition https://www.kaggle.com/competitions/dogs-vs-cats-redux-kernels-edition/leaderboard

As part of training model, ImageDataGenerator from keras image processing library is used from image augmentation and providing input to model

To use image data generator, specific folder structure is required. 

For training:
```
training/dog
    
training/cat
```
Since, this is a cat vs dog classification problem, 2 folders are created with the name of cat and dog. All the images of dogs in the training data are put into "dog" folder and similarly cat image are put into "cat" and both these folders are put into the training folder.

## Transfer learning
Transfer learning using Xception model is used for training the model. Initially all the layers of the model are kept frozen and only the output layer is trained to perform binary classification. After that all the layers of the pre-trained model are unfrozen and trained on the images of cat and dog
- convolutional neural network(CNN) is used as part of the input pipeline
- Binary crossentrophy is used as loss function
- Accuracy is the performance metric

## Results
Using the predictive probabilities a result file is generated from the testing images and kaggle score of 0.089 is obtained (Here low score corresponds to low errors in classification and better accuracy)


