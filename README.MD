# Tensorflow Playground

### 1. [Basics](1_basics.ipynb)
Reproducing the tutorial in book _Pro Deep Learning with TensorFlow_. Modified some code to understand what's going on.

### 2. [Autoencoder](2_autoencoder.ipynb)
Trained an autoencoder on MNIST data. the result is very good considering that the middle layer only has two hidden units. It also produced a projection in the 2D space that makes sense. 

### 3. [WGAN](3_wgan_gradient_penalty.ipynb)
Trained WGAN with gradient penalty on MNIST. Details inside the notebook.

### 4. [CWGAN](4_conditional_wgan.ipynb)
I implemented conditional WGAN by concatenating a vector of 1-hot coded digit with the random vector to feed into the generative network, and added a classification loss to the original WGAN loss function (Details in the notebook). The results are reasonable, but I think there's significant room for improvement. 
The successful training started with alternating the two losses (WGAN loss and classification loss), and tuned down the classification loss mid-way. This is a bit of a hack solution, and the results generated more or less look the same, whereas even the same number should have a degree of variability under WGAN.
