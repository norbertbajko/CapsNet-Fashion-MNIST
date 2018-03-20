# CapsNet-Fashion-MNIST
[![License](https://img.shields.io/github/license/mashape/apistatus.svg?maxAge=2592000)](https://github.com/XifengGuo/CapsNet-Keras/blob/master/LICENSE)

A Keras implementation of CapsNet in the paper:   
[Sara Sabour, Nicholas Frosst, Geoffrey E Hinton. Dynamic Routing Between Capsules. NIPS 2017](https://arxiv.org/abs/1710.09829)

This code is adopted from [CapsNet-Keras](https://github.com/XifengGuo/CapsNet-Keras.git) to test
the performance of CapsNet on [Fashion-MNIST](https://github.com/zalandoresearch/fashion-mnist) by **Xifeng Guo** and improved by **Norbert Bajko**

**Contacts**  
[Norbert Bajko](https://www.linkedin.com/in/bajkonorbert/)  
E-mail `norbert.bajko94@gmail.com`

[Xifeng Guo](https://xifengguo.github.io/)  
E-mail `guoxifeng1990@163.com` or WeChat `wenlong-guo`.


## Usage

**Step 1.
Install [Keras](https://github.com/keras-team/keras)
with [TensorFlow](https://github.com/tensorflow/tensorflow) backend**
```
pip install tensorflow-gpu
pip install keras
```

**Step 2. Clone this repository to local**
```
git clone https://github.com/norbertbajko/CapsNet-Fashion-MNIST.git
cd CapsNet-Fashion-MNIST
```

**Step 3. Train a CapsNet on Fashion-MNIST**  

Training with default settings:
```
$ python capsulenet.py
```
Data preprocessing:
- scale pixel values to `[0,1]`
- shift 2 pixels and horizontal flipping augmentation

**Step 4. Test a pre-trained CapsNet model**

###### *My pre-trained model is not available at the moment, but will come soon.*

Suppose you have trained a model using the above command, then the trained model will be
saved to `result/trained_model.h5`.  
Now just launch the following command to get test results:
```
$ python capsulenet.py --is_training 0 --weights result/trained_model.h5
```
It will output the testing accuracy and show the reconstructed images.
The testing data is same as the validation data. It will be easy to test on new data,
just change the code as you want.


## Results

**Accuracy**   

###### *Will come soon.*

<!-- Test Accuracy: `93.62%`

Losses and accuracies:   
![](result/log.png) -->

**Training Speed**  

About `175s / epoch` on a single Titan X (Pascal) GPU.   

**Reconstruction results**  

Top 5 rows are real images from Fashion-MNIST and
Bottom are corresponding reconstructed images.

![](real_and_recon.png)
