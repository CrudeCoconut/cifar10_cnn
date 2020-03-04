# Cifar10 

Summary
------
Built a CNN with the Keras Library on the Cifar10 dataset and recorded metrics with learning rate over 10 epochs and batch size of 32.


Model/CNN Layers
-----------------

<img src = "https://github.com/CrudeCoconut/cifar10_cnn/blob/master/cnn_model.PNG">

The summary of the CNN is shown above. 

Two convolution layers of 32 filters with same padding is connected to max pooling and connected to 

another two convolution layers of 64 filters followed up by another max pooling layer. After each pooling step,

a dropout layer of 0.2 is used. These are then flattened and fed into two dense layers with relu and dropout of 0.5.

Finally, these dense layers are finally inputted into a last dense layer to get the output.


Loss/Accuracy and Learning Rate
--------------------------------

![alt-text-1](https://github.com/CrudeCoconut/cifar10_cnn/blob/master/Learning%20Rate/0.001_Loss.png "Loss 0.001") ![alt-text-2](https://github.com/CrudeCoconut/cifar10_cnn/blob/master/Learning%20Rate/0.001_Acc.png "Accuracy 0.001")

