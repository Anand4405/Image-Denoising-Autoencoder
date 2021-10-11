# Image-Denoising-Autoencoder
## Dataset:
MNIST dataset used for training a model. 
MNIST contains 60000 training exhamples and 10000 testing exhamples.

## Architecture Of Model

Convolutional Neural Network (CNN) used for creating a model. This model contains 6 layers in which 3 are of encoder and 3 of decoder.
For encoder used Conv2d filter and it takes parameter as Con2d(input_channels,output_channels,kernal_size,stride,padding)
For decoder used ConvTranspose2d  filter and it takes parameters as ConvTranspose2d(input_channels,output_channels,kernel_size,stride,padding,output_padding)
 
Model Consists of following sequence of Layers:
Layer 1: Conv2d(1,16,3,stride=2,padding=1)
Layer 2: Conv2d(16,32,3,stride=2,padding=1)
Layer 3: Conv2d(32,64,5)

Layer 4: ConvTranspose2d(64,32,5)
Layer 5: ConvTranspose2d(32,16,3,stride=2,padding=1,output_padding=1)
Layer 6: ConvTranspose2d(16,1,3,stride=2,padding=1,output_padding=1)
## Activation Functions
ReLU and Sigmoid activation Functions are used to bring non-linearity in model.

## Loss Function and Optimization:
Mean Square Loss (MSE) function is used to calculate loss. 
ADAM Optimizer is used for optimization of model with learning rate 0.001

## Noise Added
Random noise added via torch.randn() such that we can change noise by changing noise factor. We can also add Gaussin noise,salt noise and many more types of noises.

## OUTPUT
Original Images:
![image](https://user-images.githubusercontent.com/87741857/136757927-3a27e71d-1864-4c7c-8d51-a606e97dde09.png)

Noisy Images:
![image](https://user-images.githubusercontent.com/87741857/136758112-8d4f62ad-5d6d-48b7-96be-1e80700673e0.png)

Reconstructed Images:
![image](https://user-images.githubusercontent.com/87741857/136758167-1b79f3cf-0edb-4df0-a6b9-64f676543931.png)


