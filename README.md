# MNIST-with-Logistic-Regression-from-Scratch
Implementing Logistic Regression on MNIST dataset from scratch

## Project Description:

Implement and train a logistic regression model from scratch in Python for the MNIST dataset (no PyTorch). The logistic regression model should be trained on the Training Set using stochastic gradient descent. It should achieve 90-93% accuracy on the Test Set. For full credit, submit via Compass (1) the code and (2) a paragraph (in a PDF document) which states the Test Accuracy and briefly describes the implementation. Due Monday, January 28 at 5 PM.

## Implementation

In my code, I first initialize a random set of parameters, and then I use stochastic logistic regression algorithm to train the model with data replacement. Then I test the data based on the training dataset to get a accuracy scores.

I also tested the model for 100 times with random initialization and plotted the histogram of accuracy scores to see the accuracy of my model.

Note that the number of iterations is 100000, and I implemented a learning rate schedule as follows:
$$
\alpha_0(\text{base rate})=0.01\\
\alpha^{(l)}=\begin{cases} 
      \alpha_0 & x\leq \frac{100000}3 \\
      \alpha_0\times10^{-1} & \frac{100000}3\lt x\leq \frac{200000}3 \\
      \alpha_0\times10^{-2} & \frac{200000}3\lt x\leq 100000
   \end{cases}
\
$$
I wrote 6 functions including `softmax(z)`, `gradient(w, x, y)`, `initialize(num_outputs,num_inputs)`, `model(X_train, Y_train, num_iterations, learning_rate)`, `predict(w, x)`, `testing(model, X_test, Y_test)` to handle initialization, model fitting and testing.

## Test Accuracy 

The test accuracy are shown as follows. Note that all 100 tests have achieved 90% accuracy and the majority of tests have accuracy scores of around 91%.
![Alt text](assets/Figure_1.png/?raw=true "Accuracy Scores in 100 Test")

