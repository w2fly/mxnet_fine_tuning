# mxnet models fine tuning
my experiments with fine tuning ONNX and pre-trained models on MXNET and one bug fixing<br>

how to use same pretrained models for building your own convolution neural network<br>

## 1. Import models from ONNX format.
Base example is here:<br>
https://mxnet.apache.org/versions/1.5.0/tutorials/onnx/fine_tuning_gluon.html<br>
But when i tried to load other model, a had runtime error in <br>
**out=net(in)**<br>
like next:<br>
**RuntimeError: Parameter 'resnetv15_batchnorm0_running_mean' has not been initialized...**<br>
After some experiments i found solution. Look at **ONNX_tuning.ipynb**<br>
Before using this notebook download onnx file from:<br>
https://github.com/onnx/models/tree/master/vision/classification/resnet/model

## 2. Import models from saved checkpoint
It's like previous task, but source model loading from saved checkpoint.<br>
Look code in **pretrained_tuning.ipynb**
