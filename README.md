# rotifer-tool

label, cx, cy, w, h = line
cx = float(cx) * IMG_WIDTH
cy = float(cy) * IMG_HEIGHT
w  = float(w)  * IMG_WIDTH
h  = float(h)  * IMG_HEIGHT

IMG_WIDTH  = 1920
IMG_HEIGHT = 1080

重み
EX/EX1/train1/weights/best.pt

https://github.com/ultralytics/ultralytics/issues/1429
NVIDIA docker  pytorch:22.12-py3
 - torch 1.14.0a0+410ce96
 - torchvision             0.15.0a0
 - opencv                  4.6.0
 - CUDA 11.8
 - cudnn 8.7.0
