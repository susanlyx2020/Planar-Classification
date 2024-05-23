# Planar Data Classification with One Hidden Layer
## Brief:
In this project, I built and implemented a neural network model with a sinlge hidden layer; use units with a on-linear activation fucntion (tanh); computed the cross entropy loss and implemented forward and backward propagation
## DataSet Used:
The data used looks like a 'flower' with some red (lable y = 0) and some blue (y = 1) points. The goal of this project is to build a model that classifies to define regions as either red or blue.
## Neural Network Model:
**Mathematically**:

For one example $x^{(i)}$:
$$z^{[1] (i)} =  W^{[1]} x^{(i)} + b^{[1]}\tag{1}$$ 
$$a^{[1] (i)} = \tanh(z^{[1] (i)})\tag{2}$$
$$z^{[2] (i)} = W^{[2]} a^{[1] (i)} + b^{[2]}\tag{3}$$
$$\hat{y}^{(i)} = a^{[2] (i)} = \sigma(z^{ [2] (i)})\tag{4}$$
Given the predictions on all the examples, you can also compute the cost $J$ as follows: 
$$J = - \frac{1}{m} \sum\limits_{i = 0}^{m} \large\left(\small y^{(i)}\log\left(a^{[2] (i)}\right) + (1-y^{(i)})\log\left(1- a^{[2] (i)}\right)  \large  \right) \small \tag{5}$$

## Forward Porpagation:
function `forward_propatation()` was implemented using these following equations:
$$Z^{[1]} =  W^{[1]} X + b^{[1]}\tag{1}$$ 
$$A^{[1]} = \tanh(Z^{[1]})\tag{2}$$
$$Z^{[2]} = W^{[2]} A^{[1]} + b^{[2]}\tag{3}$$
$$\hat{Y} = A^{[2]} = \sigma(Z^{[2]})\tag{4}$$

## Cost:
cost is computed as follows:
$$J = - \frac{1}{m} \sum\limits_{i = 1}^{m} \large{(} \small y^{(i)}\log\left(a^{[2] (i)}\right) + (1-y^{(i)})\log\left(1- a^{[2] (i)}\right) \large{)} \small\tag{1}$$

## Results:
The model has an high accuracy of 90% and is able to successfully classify the red and blue regions of the planar shaped data provided. 
