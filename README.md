Deep Comparison and Segmentation Network (DCASN)
====================================
DCASN is used for tracking and segmenting handheld objects in
real-time. This repository provides the details of DCASN architecture,
the dataset and trained models. The evalution results are also
provided.

Note
------------
We will make our dataset and trained models publicly available once
our work has been published.

------------

Requirements
------------
- [ROS Indigo or higher](http://wiki.ros.org/kinetic)
- [CUDA (7.5 or higher)](https://developer.nvidia.com/cuda-downloads)
- [OpenCV 3.0 or higher](https://github.com/opencv/opencv)
- [image_view](https://github.com/ros-perception/image_pipeline)
- [Caffe](https://github.com/BVLC/caffe) 


Downloading the Package
------------
```bash
$ git clone https://github.com/iKrishneel/dcasn.git
$ cd dcasn
$ git pull --all
```

Handheld Object Dataset
------------
Coming soon

Trained Models
------------
Coming soon

Videos
------------


Detection Results
------------

**1. We used the accumulated object models to train
[FCN](https://github.com/shelhamer/fcn.berkeleyvision.org) network for
semantic segmentation.**

Plot showing the performace of FCN trained using our models and the
benchmark FCN trained using the manually annotated ground truth
datasets

<img src="assets/arc/apc_accuracy.png" width="50%" height="50%"/>

------------

**Training and Validation Plots**
The training and validation plot of FCN trained using the models
accumulated using our models.
![](assets/arc/fcn_train.png)

------------

Visualization of the cluttered bin segmentation task.
<img src="assets/arc/fcn_result.jpg" width="100%" height="100%"/>

------------

**2. We also used the accumulated models to train object detector using
[Mask RCNN](https://github.com/matterport/Mask_RCNN) for instance
segmentation. **

Plot showing the training loss and accuracy of Mask RCNN detector
trained using the object models accumulated using our method.

<img src="assets/mask-rcnn/accuracy.png" width="50%"/> <img src="assets/mask-rcnn/loss.png" width="50%" /> 





