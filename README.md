# CapsNet

[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg?style=plastic)](https://opensource.org/licenses/Apache-2.0)

A tensorflow implemention of CapsNet in Geoffrey Hinton's paper [Dynamic Routing Between Capsules. NIPS 2017](https://arxiv.org/abs/1710.09829)
![capsnet](capsnet.png)   

A capsule is a group of neurons whose activity vector represents the instantiation parameters of a specific type of entity such as an object or an object part. We use the length of the activity vector to represent the probability that the entity exists and its orientation to represent the instantiation parameters. Active capsules at one level make predictions, via transformation matrices, for the instantiation parameters of higher-level capsules. When multiple predictions agree, a higher level capsule becomes active.

## Requirements
- Python3
- NumPy
- [Tensorflow >= 1.3](https://github.com/tensorflow/tensorflow)

## Usage
**Step 1.** 
Clone this repository with ``git``.

```
$ git clone https://github.com/VectorFist/CapsNet.git
$ cd CapsNet
```

**Step 2.** 
Download the [MNIST dataset](http://yann.lecun.com/exdb/mnist/), extract it into ``MNIST_data`` directory.

**Step 3.** 
Start the training:
```
$ python run_capsnet.py
```

**Step 3.** 
Test capsnet model:
```
$ python run_capsnet.py --run_mode=test
```
