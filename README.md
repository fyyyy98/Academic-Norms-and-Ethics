# Academic Norms and Ethics
A paper reading note-part 1
# Mask R-CNN
Mask R-CNN is an extension of the detection framework Faster R-CNN. It predicts the object mask by adding a branch in parallel with the existing branch for bounding box recognition. It can effectively detect objects in the image and generate high-quality segmentation masks for each instance.

This framework can be easily extended to other tasks, such as human pose estimation.
# Introduction
The rapid development of object detection and semantic segmentation benefits from Fast/Faster R- CNN and full revolutionary network (FCN) respectively. The goal of this paper is to develop a comparable instance segmentation framework.

Instance segmentation is a challenging task because it requires not only the detection of objects, but also the accurate segmentation of each instance. Therefore, it needs to be combined with object detection. The goal is to classify each object and locate the object with a bounding box.

Mask R-CNN extends Faster R-CNN by adding a branch to predict the segmentation mask on each region of interest (ROI) and paralleling the existing branches for classification and bounding box regression.

Improved on the fast r-cnn framework to promote a variety of flexible architecture design;

Mask branch is a small FCN, which only adds a small amount of computing overhead and ensures the training speed.

![image](https://user-images.githubusercontent.com/25840641/144787408-7ef09baa-7473-4b5d-bb02-8d43ac62e3d6.png)

# Mask R-CNN
Mask R-CNN is a very intuitive idea: Faster R-CNN is used for detection. It has two outputs of class and bounding box for each candidate object. On this basis, a branch is added to predict the mask.

The difference between the third branch and the first two branches is that it requires more detailed spatial layout features;

Faster R-CNN lacks alignment function, so Mask R-CNN needs to add pixel to pixel alignment function.

# paper

https://arxiv.org/abs/1703.06870
