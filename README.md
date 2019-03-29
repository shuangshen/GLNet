# GLNet for Memory-Efficient Segmentation of Ultra-High Resolution Images

[![Language grade: Python](https://img.shields.io/lgtm/grade/python/g/chenwydj/ultra_high_resolution_segmentation.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/chenwydj/ultra_high_resolution_segmentation/context:python) [![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

We will provide a complete usage pretrained models for our paper very soon.

Collaborative Global-Local Networks for Memory-Efﬁcient Segmentation of Ultra-High Resolution Images

Wuyang Chen*, Ziyu Jiang*, Zhangyang Wang, Kexin Cui, and Xiaoning Qian

In CVPR 2019 (Oral).

## Overview

Segmentation of ultra-high resolution images is increasingly demanded in a wide range of applications (e.g. urban planning), yet poses signiﬁcant challenges for algorithm efficiency, in particular considering the (GPU) memory limits.

We propose collaborative **Global-Local Networks (GLNet)** to effectively preserve both global and local information in a highly memory-efficient manner.

* **Memory-efficient**: **training w. only one 1080Ti** and **inference w. less than 2GB GPU memory**, for ultra-high resolution images of up to 30M pixels.

* **High-quality**: GLNet outperforms existing segmentation models on ultra-high resolution images.

<p align="center">
<img src="https://raw.githubusercontent.com/chenwydj/ultra_high_resolution_segmentation/master/docs/images/deep_globe_acc_mem_ext.jpg" alt="Acc_vs_Mem" width="900"/></br>
<b>Inference memory v.s. mIoU</b> on the <a href="https://arxiv.org/abs/1805.06561">DeepGlobe dataset</a>.
</br>
GLNet (red dots) integrates both global and local information in a compact way, contributing to a well-balanced trade-off between accuracy and memory usage.</br>
</p>

<p align="center">
<img src="https://raw.githubusercontent.com/chenwydj/ultra_high_resolution_segmentation/master/docs/images/examples.jpg" alt="Examples" width="450"/></br>
<b>Ultra-high resolution Datasets</b>: <a href="https://arxiv.org/abs/1805.06561">DeepGlobe</a>, <a href="https://arxiv.org/abs/1710.05006">ISIC</a>, <a href="https://ieeexplore.ieee.org/document/8127684">Inria Aerial</a>
</p>

## Methods

<p align="center">
<img src="https://raw.githubusercontent.com/chenwydj/ultra_high_resolution_segmentation/master/docs/images/glnet.png" alt="GLNet" width="600"/></br>
<b>GLNet</b>: the global and local branch takes downsampled and cropped images, respectively. Deep feature map sharing and feature map regularization enforce our global-local collaboration. The final segmentation is generated by aggregating high-level feature maps from two branches.
</p>

<p align="center">
<img src="https://raw.githubusercontent.com/chenwydj/ultra_high_resolution_segmentation/master/docs/images/gl_branch.png" alt="GLNet" width="600"/></br>
<b>Deep feature map sharing</b>: at each layer, feature maps with global context and ones with local fine structures are bidirectionally brought together, contributing to a complete patch-based deep global-local collaboration.
</p>

## Acknowledge
The work of Z. Wang is in part supported by the National Science Foundation Award RI-1755701. The work of X.Qian is in part supported by the National Science Foundation Award CCF-1553281. We also thank Prof. Andrew Jiang and Junru Wu for helping experiments.

<!--
## Citation
If you use this code for your research, please cite our papers.
```
@inproceedings{chen2019GLNET,
  title={Collaborative Global-Local Networks for Memory-Efﬁcient Segmentation of Ultra-High Resolution Images},
  author={Chen, Wuyang and Ziyu Jiang and Zhangyang Wang and Kexin Cui and Xiaoning Qian},
  booktitle={Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition},
  year={2019}
}
```
-->