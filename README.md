# Tiny Imagenet Classification using Resnet Architecture

This repository gives a stratagem on how to solve the classification problem for Tiny Imagenet Dataset.

Tiny Imagenet has 200 classes. Each class has 500 training images, 50 validation images, and 50 test images. We have released the training and validation sets with images and annotations. We provide both class labels and bounding boxes as annotations; however, you are asked only to predict the class label of each image without localizing the objects. The test set is released without labels. You can download the whole tiny ImageNet dataset here. Each image is 64 × 64 in size. The Tiny ImageNet dataset comes from ILSVRC benchmark test but with fewer categories and lower resolution. 

[Download Tiny Imagenet Dataset here](http://cs231n.stanford.edu/tiny-imagenet-200.zip "Download Tiny Imagenet Dataset")

Some of the challenging samples for prediction are

![](https://github.com/FaizalSandanampusi/TinyImagenet-200/blob/master/Capture.PNG?raw=true)

The image on the left must be chihuahua which is very similar to teddy bear and the image on right must be football which is very challenging for the network to predict.



I have tried to develop a wider architecture by increasing the number of channels exponentially with each layer and adding a bottleneck after some defined number of layers. I have also encapsulated the concept of Residual architecture which concatenates predominant features at some specific layer before some defined number of layers. 

The flowchart of the architecture can be found in the repository as PNG file.

The model is written in Keras framework and is trained from scratch using the Google colab GPU.

I have been able to achieve an accuracy of 50.9 % validation accuracy with a loss of 1.109 with in 100 epochs without augmentation.

![](https://github.com/FaizalSandanampusi/TinyImagenet-200/blob/master/training%20and%20test%20loss.png?raw=true)
                                   Training and validation loss
![](https://github.com/FaizalSandanampusi/TinyImagenet-200/blob/master/train_and_val_acc.png?raw=true)
                                Training and validation Accuracy
I have uploaded the ipython notebook in the repository which can be used for further improvement.

This could be a starter code for newbies to experiment with. Techniques like CylicLearningRate, Image augmentation, Class weight initialization based on bad predictions could be made. 











