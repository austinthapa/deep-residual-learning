## Deep Residual Network Implementation from scratch in TensorFlow

Before ResNet, Deep Neural Networks like GoogLeNet and Visual Geometry Groups (VGG) were achieving state-of-the-art performance on ImageNet datasets, but making them deeper caused degradation, that is instead of converging the training error and testing error were high.

But, in theory, deeper networks should be able to model complicated functions, but training became harder due to vanishing gradients. 

With the introduction of ResNet, the skip connections allow gradient to flow directly through layers enabling very deep networks, such as ResNet-152 consisting of 152 layers.

## Architecture Details

1. Basic Residual Blocks (Shallow Networks)
- 2 x Convolutional Layers (3x3 filters) + Batch Normalization + ReLU
- Output = Conv2  skip connection ReLU
- ResNet-18m ResNet-24: Basic Residual Block (no bottleneck)
  
2. Bottle Neck Layers (Very Deep Networks)
- 3 Layers: 1x1, 3x3, 1x1
- First 1x1 reduces dimensions (compression)
- 3x3 process features
- Last 1x1 restores dimensions
- Used in ResNet-50/101/152 to keep computations manageable.
  