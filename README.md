# Convolutional_Neural_Network_for_COVID_19_Classification
This project involves training models to classify images as either COVID-19 or healthy. The project uses a dataset containing images of COVID-19 and healthy cases. Two different approaches are used for training the models.

The first approach involves building a custom convolutional neural network (CNN) model from scratch. The model consists of convolutional layers, max pooling layers, dropout layers, and dense layers. It is trained using an image data generator to preprocess the images and generate batches of augmented data for training. The model is compiled with the Adam optimizer and binary cross-entropy loss, and its performance is evaluated using accuracy. After training, the model weights are saved to disk.

The second approach utilizes transfer learning with the VGG19 model. The VGG19 model is pre-trained on the ImageNet dataset and its weights are loaded. A new top model is added on top of the VGG19 base model. The top model includes global average pooling, dense layers, and dropout layers. The combined model is then trained using the same image data generator and evaluated. The model weights are saved after training.

Finally, the trained models are used to make predictions on new test images. An example image is loaded, preprocessed, and fed into each model. The output scores are then compared to a threshold of 0.5 to determine whether the image is classified as COVID-19 or healthy. The predictions are displayed as output.
