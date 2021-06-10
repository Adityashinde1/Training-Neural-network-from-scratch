# Training-Neural-network-from-scratch

Artificial Neural Network uses back propagation technique for training. I am building this Neural network to perform classification problem. For Classification I have used MNIST dataset which has 10 classes. 

## Neural Network Architecture

The dataset available in the sci-kit learn liabrary consist of images 28*28 pixels, in greyscale with pixel-values from 0 to 255. So when we flatten our image we get 784 vectors.
We have an Input layer, 2 hidden layers and an output Layer
S0 our structure looks-
Input Layer        = 784 nodes,
1st hidden layer   = 128 nodes,
2nd hidden layer   = 64 nodes,
Output layer       = 10 nodes (We have 10 classes).

## Training

During training, all the weights and biases are updated after processing mini-batches and the method is called Mini - batch gradient descent. The update rule uses learning rate of 0.1. The code is run for 50 epochs. The first activation function is Sigmoid of the form f(x) = 1 / 1 + exp(-x). Its range is between 0 and 1. It is S — shaped curve. The second activation function is Softmax of the form of f(x) = np.exp(x - x.max()) / np.sum(np.exp(x - x.max()), axis=0). It gives probablity of the classes. The performance of classification is measured using Classification report. The feed_forward function initialize the weights and biases. After training I am ploting the Training loss vs Validation loss and Training Accuracy vs Validation Accuracy. With this architecture we able to achieve 98% Accuracy.
