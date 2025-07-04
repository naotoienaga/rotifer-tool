# Rotifer-tool
This repository contains annotated dataset, trained model, and tracking visualization code of the following paper:
> Naoto Ienaga, Toshinori Takashi, Hitoko Tamamizu, Kei Terayama. Rotifer detection and tracking framework using deep learning for automatic culture systems, _Smart Agricultural Technology_, vol.9, 100577 (2024). [https://doi.org/10.1016/j.atech.2024.100577](https://doi.org/10.1016/j.atech.2024.100577)

## Datset and trained model
You can download them [here](https://app.box.com/s/7a5l9mkoiciaosx2i7s3wmv743ua3sh2).
- IDX.mp4: Videos
- IDX_bbox: Annotations for videos
- weight.pt: Trained model

### Annotation format
Annotation format follows YOLO. That is, each line represents ```class, x, y, w, h```  
For ```class```, 0 represents _rotifer_, 1 represents _fertilized_, and 2 represents _ciliate_.  
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
The code for visualization of tracking result can be run on Google Colab so that the environment setup is not needed.  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](http://colab.research.google.com/github/naotoienaga/rotifer-tool/blob/main/visualize_tracking.ipynb)
