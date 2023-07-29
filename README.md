# IGNet
[![ACM](https://img.shields.io/badge/ACM-MM2023-purple)](https://www.acmmm2023.org/)
[![LICENSE](https://img.shields.io/badge/License-MIT-green)](https://github.com/lok-18/IGNet/blob/master/LICENSE)
[![Python](https://img.shields.io/badge/Python-3.7-blue.svg)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-1.7.0-orange)](https://pytorch.org/)

### *Learning a Graph Neural Network with Cross Modality Interaction for Image Fusion (Accept)*
in Proceedings of the 31st ACM International Conference on Multimedia (**ACM MM 2023**)  
by Jiawei Li, Jiansheng Chen, JinyuanLiu and Huimin Ma  

**Overall performance comparison:**
<div align=center>
<img src="https://github.com/lok-18/IGNet/blob/master/fig/compare.png" width="100%">
</div>  


**Framework of our proposed IGNet:**
<div align=center>
<img src="https://github.com/lok-18/IGNet/blob/master/fig/network.PNG" width="100%">
</div>  

### *Requirements* 
> - python 3.7  
> - torch 1.7.0
> - torchvision 0.8.0
> - opencv 4.5
> - numpy 1.21.6
> - pillow 9.4.0

### *Dataset setting*
> We give 5 test image pairs as examples in [[*TNO*]](https://figshare.com/articles/dataset/TNO_Image_Fusion_Dataset/1008029), [[*MFNet*]](https://www.mi.t.u-tokyo.ac.jp/static/projects/mil_multispectral/) and [[*M3FD*]](https://github.com/JinyuanLiu-CV/TarDAL) datasets, respectively.
> 
> Moreover, you can set your own test datasets of different modalities under ```./test_images/...```, like:   
> ```
> test_images
> ├── ir
> |   ├── 1.png
> |   ├── 2.png
> |   └── ...
> ├── vis
> |   ├── 1.png
> |   ├── 2.png
> |   └── ...
> ```
> 
> Note that if ```./test_images/vis/xxx.png``` is in single-channel L format, you should use ```LtoRGB.py``` to convert it to three-channel RGB format.

### *Test*
> The pre-trained model has given in ```./model/IGNet.pth```.
> Please run ```test.py``` to get fused results, and you can check them in:
> ```
> results
> ├── 1.png
> ├── 2.png
> └── ...

### *Experimental results*
> We compared our proposed IGNet with [[*DIDFuse*]](https://github.com/Zhaozixiang1228/IVIF-DIDFuse), [[*U2Fusion*]](https://github.com/hanna-xu/U2Fusion), [[*SDNet*]](https://github.com/HaoZhang1018/SDNet), [[*TarDAL*]](https://github.com/JinyuanLiu-CV/TarDAL), [[*UMFusion*]](https://github.com/wdhudiekou/UMF-CMGR), [[*DeFusion*]](https://github.com/erfect2020/DecompositionForFusion) and [[*ReCoNet*]](https://github.com/JinyuanLiu-CV/ReCoNet).
> 
> **Fusion results:**
> <div align=center>
> <img src="https://github.com/lok-18/IGNet/blob/master/fig/fusion.png" width="100%">
> </div>
>
> <br>After retaining the fusion results of all methods on [[*YOLOv5*]](https://github.com/ultralytics/yolov5) and [[*DeepLabV3+*]](https://github.com/VainF/DeepLabV3Plus-Pytorch), we compare the corresponding detection and segmentation results with IGNet.</br>
> 
> **Detection & Segmentation results:**
