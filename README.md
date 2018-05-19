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
You can view the full videos of our results [here](https://drive.google.com/open?id=0B5hRAGKTOm_KNUV4R3lkTzVHY1U)

<img src="assets/videos/tshirt1.gif" width="280" /> <img src="assets/videos/umbrella.gif" width="280" /> <img src="assets/videos/pillow.gif" width="280"  />
<img src="assets/videos/banana.gif" width="280" /> <img src="assets/videos/file.gif" width="280" /> <img src="assets/videos/onion.gif" width="280"  />
<img src="assets/videos/kleenex.gif" width="280" />


Semantic Segmentation
------------

**We used the accumulated object models to train
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


Instance Segmentation using Mask R-CNN
------------

**We also used the accumulated models to train object detector using
[Mask RCNN](https://github.com/matterport/Mask_RCNN) for instance
segmentation.**

Plot showing the training loss and accuracy of Mask RCNN detector
trained using the object models accumulated using our method.

<img src="assets/mask-rcnn/accuracy.png" width="49%"/> <img src="assets/mask-rcnn/loss.png" width="49%" /> 

Visualization of instance detection and segmentation.

<img src="assets/mask-rcnn/readme/mask_rcnn_resnet50_dataset_benchmark_20180519_040732.jpg" width="30%" /> <img src="assets/mask-rcnn/readme/mask_rcnn_resnet50_dataset_krish_20180519_040639.jpg" width="30%" /> <img src="assets/mask-rcnn/readme/mask_rcnn_resnet50_dataset_itemdata_20180519_040543.jpg" width="30%" />



