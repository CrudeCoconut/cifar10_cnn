# Cifar10 

Summary
------
CNN with the Keras Library on the Cifar10 dataset and recorded metrics with learning rate over 10 epochs and batch size of 32.
The code is in the jupyter notebook in python above. Below is a summary of findings.

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
### 0.001 Learning Rate
![alt-text-1](https://github.com/CrudeCoconut/cifar10_cnn/blob/master/Learning%20Rate/0.001_Loss.png "Loss 0.001") ![alt-text-2](https://github.com/CrudeCoconut/cifar10_cnn/blob/master/Learning%20Rate/0.001_Acc.png "Accuracy 0.001")


### 0.01 Learning Rate
![alt-text-1](https://github.com/CrudeCoconut/cifar10_cnn/blob/master/Learning%20Rate/0.01_loss.PNG "title-1") ![alt-text-2](https://github.com/CrudeCoconut/cifar10_cnn/blob/master/Learning%20Rate/0.01_Acc.png "title-2")


### 0.1 Learning Rate
![alt-text-1](https://github.com/CrudeCoconut/cifar10_cnn/blob/master/Learning%20Rate/0.1_Loss.PNG "0.1 Loss") ![alt-text-2](https://github.com/CrudeCoconut/cifar10_cnn/blob/master/Learning%20Rate/0.1_Acc.png "0.1 Accuracy")


As the name implies, the bigger the learning rate, the faster the CNN "learns" or trains. I decided to target learning rate as 
a metric because I wanted to test which learning rate would overshoot the minima. 0.01 Learning Rate looks most optimal as the
cross validation, which in the scenario is the test, loss consistenly decreases and accuracy increases. The small learning rate
of 0.01 moves slowly and I think that it might be getting stuck in local minima, while the 0.1 learning rate has its metrics increase
and decrease over epochs, meaning overshooting.


Future Work for This Dataset
-----------------------------
I ideally want to train a model to around 90 percent accuracy and lower loss. This might be able to be done with more epochs, but
I also want to find the optimal paramters for this model. I changed the learning rate manually, but I want to be 
automate changes in different parameters like learning rate, dropout rate, dense layer units, etc, without changing
the actual structure of the CNN and check for overfitting/underfitting to determine paramters automatically instead of 
manually.
