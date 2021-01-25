# pyradox
This python library helps you with implementing various state of the art neural networks in a totally customizable fashion using Tensorflow 2
___
## Installation

    pip install git+https://github.com/Ritvik19/pyradox.git
___

## Usage

### Modules

Module | Description | Input Shape | Output Shape | Usage
---|---|---|---|---
Rescale | A layer that rescales the input: `x_out = (x_in -mu) / sigma` | Arbitrary | Same shape as input | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/Rescale/Rescale.md)
Convolution 2D | Applies 2D Convolution followed by Batch Normalization (optional) and Dropout (optional) | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/Convolution2D/Convolution2D.md)
Densely Connected | Densely Connected Layer followed by Batch Normalization (optional) and Dropout (optional) | 2D tensor with shape (batch_size, input_dim) | 2D tensor with shape (batch_size, n_units) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/DenselyConnected/DenselyConnected.md)
DenseNet Convolution Block | A Convolution block for DenseNets | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/DenseNetConvolutionBlock/DenseNetConvolutionBlock.md)
DenseNet Convolution Block | A Convolution block for DenseNets |4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/DenseNetConvolutionBlock/DenseNetConvolutionBlock.md)
DenseNet Transition Block | A Transition block for DenseNets | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/DenseNetTransitionBlock/DenseNetTransitionBlock.md)
Dense Skip Connection | Implementation of a skip connection for densely connected layer | 2D tensor with shape (batch_size, input_dim) | 2D tensor with shape (batch_size, n_units) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/DenseSkipConnection/DenseSkipConnection.md)
VGG Module | Implementation of VGG Modules with slight modifications, Applies multiple 2D Convolution followed by Batch Normalization (optional), Dropout (optional) and MaxPooling | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/VGG-Module/VGG-Module.md)
Inception Conv | Implementation of 2D Convolution Layer for Inception Net, Convolution Layer followed by Batch Normalization, Activation and optional Dropout |  4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/InceptionConv/InceptionConv.md) 
Inception Block | Implementation on Inception Mixing Block | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/InceptionBlock/InceptionBlock.md) 
Xception Block | A customised implementation of Xception Block (Depthwise Separable Convolutions) | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/XceptionBlock/XceptionBlock.md)
Efficient Net Block | Implementation of Efficient Net Block (Depthwise Separable Convolutions) | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/EfficientNetBlock/EfficientNetBlock.md)
Conv Skip Connection | Implementation of Skip Connection for Convolution Layer | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/ConvSkipConnection/ConvSkipConnection.md)
Res Net Block | Customized Implementation of ResNet Block | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/ResNetBlock/ResNetBlock.md)
Res Net V2 Block | Customized Implementation of ResNetV2 Block | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/ResNetV2Block/ResNetV2Block.md)
Res NeXt Block | Customized Implementation of ResNeXt Block | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/ResNeXtBlock/ResNeXtBlock.md)
Inception Res Net Conv 2D | Implementation of Convolution Layer for Inception Res Net: Convolution2d followed by Batch Norm | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/InceptionResNetConv2D/InceptionResNetConv2D.md)
Inception Res Net Block | Implementation of Inception-ResNet block | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [block 8](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/InceptionResNetBlock-1/InceptionResNetBlock-1.md) [Block 17](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/InceptionResNetBlock-2/InceptionResNetBlock-2.md) [Block 35](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/InceptionResNetBlock-3/InceptionResNetBlock-3.md)
NAS Net Separable Conv Block | Adds 2 blocks of Separable Conv Batch Norm | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/NASNetSeparableConvBlock/NASNetSeparableConvBlock.md)
NAS Net Adjust Block | Adjusts the input `previous path` to match the shape of the `input` | | |
NAS Net Normal A Cell | Normal cell for NASNet-A | | |
NAS Net Reduction A Cell | Reduction cell for NASNet-A | | |
Mobile Net Conv Block | Adds an initial convolution layer with batch normalization and activation | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/MobileNetConvBlock/MobileNetConvBlock.md)
Mobile Net Depth Wise Conv Block | Adds a depthwise convolution block. A depthwise convolution block consists of a depthwise conv, batch normalization, activation, pointwise convolution, batch normalization and activation | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/MobileNetDepthWiseConvBlock/MobileNetDepthWiseConvBlock.md)
Inverted Res Block | Adds an Inverted ResNet block | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/InvertedResBlock/InvertedResBlock.md)
SEBlock | Adds a Squeeze Excite Block | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/SEBlock/SEBlock.md)

### ConvNets

Module | Description | Input Shape | Output Shape | Usage
---|---|---|---|---
Generalized Dense Nets | A generalization of Densely Connected Convolutional Networks (Dense Nets) | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/GeneralizedDenseNets/GeneralizedDenseNets.md)
Densely Connected Convolutional Network 121 | A modified implementation of Densely Connected Convolutional Network 121 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/DenselyConnectedConvolutionalNetwork121/DenselyConnectedConvolutionalNetwork121.md)
Densely Connected Convolutional Network 169 | A modified implementation of Densely Connected Convolutional Network 169 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/DenselyConnectedConvolutionalNetwork169/DenselyConnectedConvolutionalNetwork169.md)
Densely Connected Convolutional Network 201 | A modified implementation of Densely Connected Convolutional Network 201 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/DenselyConnectedConvolutionalNetwork201/DenselyConnectedConvolutionalNetwork201.md)
Generalized VGG | A generalization of VGG network | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D or 2D tensor | [usage 1](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/GeneralizedVGG-1/GeneralizedVGG-1.md) [usage 2](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/GeneralizedVGG-2/GeneralizedVGG-2.md) 
VGG 16 |  A modified implementation of VGG16 network | 4D tensor with shape (batch_shape, rows, cols, channels) | 2D tensor with shape (batch_shape, new_dim) | [usage 1](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/VGG16-1/VGG16-1.md) [usage 2](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/VGG16-2/VGG16-2.md) 
VGG 19 |  A modified implementation of VGG19 network | 4D tensor with shape (batch_shape, rows, cols, channels) | 2D tensor with shape (batch_shape, new_dim) | [usage 1](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/VGG19-1/VGG19-1.md) [usage 2](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/VGG19-2/VGG19-2.md) 
Inception V3 | Customized Implementation of Inception Net | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/InceptionV3/InceptionV3.md)
Generalized Xception | Generalized Implementation of XceptionNet (Depthwise Separable Convolutions) | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/GeneralizedXception/GeneralizedXception.md)
Xception Net | A Customised Implementation of XceptionNet | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/XceptionNet/XceptionNet.md)
Efficient Net | Generalized Implementation of Effiecient Net | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/EfficientNet/EfficientNet.md)
Efficient Net B0 | Customized Implementation of Efficient Net B0 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/EfficientNetB0/EfficientNetB0.md)
Efficient Net B1 | Customized Implementation of Efficient Net B1 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/EfficientNetB1/EfficientNetB1.md)
Efficient Net B2 | Customized Implementation of Efficient Net B2 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/EfficientNetB2/EfficientNetB2.md)
Efficient Net B3 | Customized Implementation of Efficient Net B3 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/EfficientNetB3/EfficientNetB3.md)
Efficient Net B4 | Customized Implementation of Efficient Net B4 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/EfficientNetB4/EfficientNetB4.md)
Efficient Net B5 | Customized Implementation of Efficient Net B5 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/EfficientNetB5/EfficientNetB5.md)
Efficient Net B6 | Customized Implementation of Efficient Net B6 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/EfficientNetB6/EfficientNetB6.md)
Efficient Net B7 | Customized Implementation of Efficient Net B7 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/EfficientNetB7/EfficientNetB7.md)
Res Net | Customized Implementation of Res Net | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/ResNet/ResNet.md)
Res Net 50 | Customized Implementation of Res Net 50 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/ResNet50/ResNet50.md)
Res Net 101 | Customized Implementation of Res Net 101 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/ResNet101/ResNet101.md)
Res Net 152 | Customized Implementation of Res Net 152 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/ResNet152/ResNet152.md)
Res Net V2 | Customized Implementation of Res Net V2 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/ResNetV2/ResNetV2.md)
Res Net 50 V2 | Customized Implementation of Res Net 50 V2 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/ResNet50V2/ResNet50V2.md)
Res Net 101 V2 | Customized Implementation of Res Net 101 V2 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/ResNet101V2/ResNet101V2.md)
Res Net 152 V2 | Customized Implementation of Res Net 152 V2 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/ResNet152V2/ResNet152V2.md)
Res NeXt | Customized Implementation of Res NeXt | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/ResNeXt/ResNeXt.md)
Res NeXt 50 | Customized Implementation of Res NeXt 50 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/ResNeXt50/ResNeXt50.md)
Res NeXt 101 | Customized Implementation of Res NeXt 101 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/ResNeXt101/ResNeXt101.md)
Res NeXt 152 | Customized Implementation of Res NeXt 152 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/ResNeXt152/ResNeXt152.md)
Inception Res Net V2 | Customized Implementation of Inception Res Net V2 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/InceptionResNetV2/InceptionResNetV2.md)
NAS Net | Generalised Implementation of NAS Net | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/NASNet/NASNet.md)
NAS Net Mobile | Customized Implementation of NAS Net Mobile | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/NASNetMobile/NASNetMobile.md)
NAS Net Large | Customized Implementation of NAS Net Large | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/NASNetLarge/NASNetLarge.md)
MobileNet | Customized Implementation of MobileNet | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [usage 1](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/MobileNet/MobileNet-1.md) [usage 2](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/MobileNet/MobileNet-2.md)
Mobile Net V2 | Customized Implementation of Mobile Net V2 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [usage 1](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/MobileNetV2/MobileNetV2-1.md) [usage 2](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/MobileNetV2/MobileNetV2-2.md)
Mobile Net V3 | Customized Implementation of Mobile Net V3 | 4D tensor with shape (batch_shape, rows, cols, channels) | 4D tensor with shape (batch_shape, new_rows, new_cols, new_channels) | [usage 1](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/MobileNetV3/MobileNetV3-1.md) [usage 2](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/MobileNetV3/MobileNetV3-2.md)

### DenseNets

Module | Description | Input Shape | Output Shape | Usage
---|---|---|---|---
Densely Connected Network | Network of Densely Connected Layers followed by Batch Normalization (optional) and Dropout (optional) | 2D tensor with shape (batch_size, input_dim) | 2D tensor with shape (batch_size, new_dim) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/DenselyConnectedNetwork/DenselyConnectedNetwork.md)
Densely Connected Resnet | Network of skip connections for densely connected layer | 2D tensor with shape (batch_size, input_dim) | 2D tensor with shape (batch_size, new_dim) | [check here](https://github.com/Ritvik19/pyradox-doc/blob/main/usage/DenselyConnectedResnet/DenselyConnectedResnet.md)
