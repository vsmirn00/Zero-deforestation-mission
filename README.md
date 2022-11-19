# Zero-deforestation-mission

### Introduction

The following notebook was made with the purpose of participating in the hackathon held by Nuwe in collaboration with Schneider Electric. The challenge consisted in classifying different images of forests in order to predict and fight deforestation. The climate change is a hefty problem that concerns all of us. Therefore, using Artificial Intelligence to preserve our environment is a necessity. In this context, there were 3 categories to predict each one of them encoded with a number: Plantation, encoded with a 0, Grassland, encoded with a 1, and finally Smallholder Agriculture encoded with a 2. The notebook was runned on google colab.  

### Data preprocessing

2 datasets were presented with the corresponding images in a zip file. The dataframes held the feature "example_path", which was used to access to the corresponding image with its respective label. That, served us to process the data and use Image Data Generator to use a data augmentation technique. The dataset had less than 2000 images to learn from, and they were very much alike. Even though, data augmentation was necessary to add some noise so the model learn how to generalise properly. The train dataset was divided into train and validation, whilst the test was saved for prediction. 

### Building the model

The architecture used for this challenge was constructed mainly on CNNs, batch normalization and dropout layers. Batch normalization layers allow us to have the same mean and standard deviation amongst all the neurons in that layer. This way, we avoid vanishing gradients or exploding gradients problem. Dropout layers on the other hand, help us to avoid overfitting. Since we were training the model on 30 epochs, it was feasible for the model to overfit. As an addition, a reducing learning rate technique was incorporated in the callbacks.

### Evaluating the results

To evaluate the results, we used a Confusion Matrix, a Classification report and plotted the evolution of Accuracy and Validation_accuracy through the epochs of training. The results yielded by the training showed a clear sign that the model was learning the weights slowly but did not overfit. As our main objective was to evaluate the predictions based on F1-Score, the classification report provided us with the value of .

### Conclusion

The results were submitted in both formats, csv and json. For the seek of learning, different architectures could have been used for this project, like VGG16 for instance. However, it was worth the trial to use a homemade neural network which brought impressive results. 
