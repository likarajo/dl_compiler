# Compile TensorFlow model with TVM

## Setup TVM

https://tvm.apache.org/docs/install/from_source.html

## Setup TensorFlow

https://www.tensorflow.org/install/

## Get Model

1. Dowload and extract existing model

http://download.tensorflow.org/models/mobilenet_v1_2018_02_22/mobilenet_v1_1.0_224.tgz

```python3
import tensorflow as tf
cat 'models/mobilenet_v1_1.0_224/mobilenet_v1_1.0_224_info.txt'
```
Model: mobilenet_v1_1.0_224
Input: input
Output: MobilenetV1/Predictions/Reshape_1

There should be a **.pb** file that is to be used for compilation.

2. Create own toy model

Run **cnn.py**

```python3
python3 cnn.py
```

The trained model will be saved to a **cnn.pb** file

## Compile the model into TVM IR

Run **compiler.py** 

```python3
python3 tvm_compiler.py
```

This generates .json and .params

## Refernce

https://github.com/starmee/AI-Notes/blob/master/%E6%B7%B1%E5%BA%A6%E5%AD%A6%E4%B9%A0/%E9%83%A8%E7%BD%B2%E6%A1%86%E6%9E%B6/TVM/TVM%E9%83%A8%E7%BD%B2.md#build-tensorflow

