# mxnet models fine tuning
my experiments with fine tuning ONNX and pre-trained models on MXNET and one bug fixing

how to use same pretrained models for building your own convolution neural network

## 1. Import models from ONNX format.
Base example is here:
https://mxnet.apache.org/versions/1.5.0/tutorials/onnx/fine_tuning_gluon.html
But when i tried to load other model, a had runtime error in **out=net(in)**
like next:
**RuntimeError: Parameter 'resnetv15_batchnorm0_running_mean' has not been initialized...**
After some experiments i found solution. Look at **ONNX_tuning.ipynb**

## 2. Import models from storing checkpoint
