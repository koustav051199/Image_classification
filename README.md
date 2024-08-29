# Image_classification
The repository contains code for some of the renowned neural network architecture for image classification. The details are given below (Check image.jpg for clarification).
## ResNet
Figure A of iamge.jpg represents a single ResNet block. Here, (3x3 Conv2D) denotes a single convolution layer with a filter size of 3×3 for 2D data and (Batch norm(2D)) represents a single Batch normalization, and (ReLU) represents the rectified linear unit activation function. A network comprising 18 such blocks is created and trained it on CIFAR-10. For the image dataset, 2D Convolutions and Batch normalization is used.
## VGG
Figure B outlines the modified VGG architecture. After each pooling layer, the number of channels is reduced by 35%, and the kernel size is increased by 25% (with ceil rounding for float calculations). Here, (Conv n-m) denotes the nth block and mth layer within that block. A VGG network is created and trained it on CIFAR-10 dataset.
Note - A combination between the padding and stride is maintained so the image is retained till the last Conv Layer.
## Inception
Figure C illustrates the configuration of a single inception block, where (n×n (CNA)) denotes a sequence of convolution, batch normalization, and ReLU activation with an n×n convolution filter. A modified inception network comprising 4 such blocks is constructed and trained it on CIFAR-10 dataset.
## Custom Network
A custom network is constructed using the following combination of blocks given below. It is trained on CIFAR-10. 
Network Architecture is given below:
(a)	Input Layer
(b)	Residual Block × 2
(c)	Inception Block × 2
(d)	Residual Block × 1
(e)	Inception Block × 1
(f)	Residual Block × 1
(g)	Inception Block × 1
(h)	Residual Block × 1
(i)	Inception Block × 1
(j)	Classification Network
• A classification network here refers to a combination of either nn.Linear or nn.Conv2d layers that produce logits for the classification task.


