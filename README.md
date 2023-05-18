# Rotifer-tool
This repository contains the public code, the trained model, and the annotated dataset of the following paper:
> (Under review. After the acceptance, information about the paper will be written.)

## Datset and trained model
You can download them [here](https://app.box.com/s/7a5l9mkoiciaosx2i7s3wmv743ua3sh2).
- IDX.mp4: Videos
- IDX_bbox: Annotations for videos
- weight.pt: Trained model

### Annotation format
Annotation format follows YOLO. That is, each line represents class, ```x, y, w, h```  
Using the size of video (in this dataset, 1080px high and 1920px wide), you can convert them as follows:
```
x of bbox center = x * video width
y of bbox center = y * video height
width of bbox    = w * video width
height of bbox   = h * video height
```

### Tracking model
See [original site](https://github.com/ultralytics/ultralytics/issues/1429) for instructions on how to use the tracking model.  
We have trained the model in the following environment.  
- NVIDIA docker image: pytorch:22.12-py3
    - torch: 1.14.0a0+410ce96
    - torchvision: 0.15.0a0
    - opencv: 4.6.0
- CUDA: 11.8
- cuDNN: 8.7.0

## Code
This code can be run on Colab so that the environment setup is not needed. If the link below doesn't work, just download and upload it to your Google Drive.
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](http://colab.research.google.com/github/naotoienaga/rotifer-tool/blob/master/.ipynb)
