# Backpropagation
Code to implement the backpropagation algorithm for neural networks

The backpropagation algorithm is one of the cornerstones of training neural networks and hence machine learning. However, it is still widely treated as a blackbox by most machine learning practitioners. In this particular work, I have tried to understand the intricacies of the algorithm, some common problems and tried to design a neural network from scratch using **numpy** only. For understanding the performance of the network, I have used the **MNIST** data for testing. The goal of this project is not to achieve accuracy (I have already achieved an accuracy of **99.57%** using a simple **CNN**). I have listed below a list of challenges that I faced while designing the network and some links which I found extremely useful.

- Initializing the network is important- I have used **He Initializer** (refer https://cs231n.github.io/neural-networks-2/ and also this wonderful lecture by Prof. Andrew Ng https://www.youtube.com/watch?v=s2coXdufOzE)
- **Vectorized** implementation leads to much faster code. In this respect **broadcasting** technique of numpy comes to aid
- Due to **10 classes** in the final output layer, **softmax** activation had to be used. It suffered from the **overflow** problem. A very elegant fix to the problem was found at https://timvieira.github.io/blog/post/2014/02/11/exp-normalize-trick/
- **ReLU** activation does not work well for unnormalized inputs

Using a simple network of **2 hidden layers with 784 neurons** each, after training for **50 epochs**, a **training accuracy of 97.94%** could be achieved. **Validation accuracy was 96.20%**. On the **test set**, an **accuracy of 96.06%** was achieved.

Details of working can be found at https://drive.google.com/drive/u/0/folders/1b0vA483dy9l9gNAZt8v8b2i2frjEQ3Os (**for my own reference**)
