---
layout: post
title: Object Detection
---
# Faster R-CNN
This model is a step up from all early attempts of object detection networks. The main idea can be described as:

> 1. A backbone $3\times 3$ CNN would featurize the image
> 2. A region proposal network tell us “where to look”(this information is called *proposal*). It takes the feature map from the backbone CNN and return rectangular boxes
>    that contains object
> 3. We map the proposal back to feature map from the backbone CNN through **RoI Align**. A small Neural network called the Fast R-CNN head would be run on the
> cropped feature which predicts:
> - $K+1$ logits for $K$ class and background
> - refined box(represented by 4 coordinates in the original image) through *bounding box regression*

# Region Proposal Network

