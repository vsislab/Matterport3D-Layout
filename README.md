

[Home](https://vsislab.github.io/Matterport3D-Layout/)|[Leader Board](#leader-board)|[Datasets](#dataset)|[Submit Result](#submit-your-result)|[References](#references)|[Contact Us](#contact-us)|[Liscense](#license)


# Welcome to Matterport3d-Layout Dataset website.

We construct a new [Dataset](#dataset) for layout estimation, which contains pixel-wise depth label for the dominant planes of the room images. Our [dataset](#dataset) uses the indoor images and depth maps from the Matterport3D dataset [1], which has large-scale RGB-D data in indoor scenes. All the images have the resolution of 1024x1280.

The original Matterport3D dataset includes 90 distinct buildings. we randomly split the dataset by the buildings. The training set includes 64 buildings with a total of 4939 images. The validation set includes 6 buildings with 456 images. The testing data includes the rest 20 buildings with a total of 1965 images. The dataset contains the following data field: 

(1) Color image;

(2) Depth map of the planar surfaces;

(3) 2D segmentation of layout;

(4) Original depth map containing indoor objects;

(5) Visible region annotation;

(6) Intrinsic matrix of the camera;

(7) Surface parameters for each plane p, q, r;

(8) The coordinates of the layout corners (u,v,Z);

(9) Original surface normal.

![Matterport3D](https://raw.githubusercontent.com/vsislab/Matterport3D-Layout/master/image.jpg)

# Leader Board

|Method | e<sub>pixel</sub>(%) | e<sub>corner</sub>(%) | e<sub>3Dcorner</sub>(%) | RMS | REL | log10 | &delta;&lt;1.25 | &delta;&lt;1.25<sup>2</sup> | &delta;&lt;1.25<sup>3</sup>|
|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
|**Ours** | **5.24** | **4.36** | **12.82** | **0.456** | **0.111** | **0.047** | **0.892** | **0.975** | **0.994**|



# Dataset

[Training set on BaiduNetdisk](https://pan.baidu.com/s/1UOzlB6IKvxM90dXFJk_9zg) with password av17.

[Testing set on BaiduNetdisk](https://pan.baidu.com/s/1AbbPWaga2NPudP8_a999Lg) with password 4hv4.

[Validation set on BaiduNetdisk](https://pan.baidu.com/s/1LEbVzz0ERYp2jBYuP_uTnA) with password hhqw.

[Training set on Google Drive](https://drive.google.com/open?id=1k6tFoLpIwj1_vCHYPOSQDbpH4LrTyR8F).

[Testing set on Google Drive](https://drive.google.com/open?id=1xLRAn-9RII-jQ-8WBEF3_xBNP4YgYcva).

[Validation set on Google Drive](https://drive.google.com/open?id=1uDROzKBaJucNxGpzQeZ3tY4bc50s0rHU).

[Surface normal of the Training set](https://1drv.ms/u/s!AvnwLMcAl2NUigfDUbHWLM-vTw3P?e=etX7Il).

[Surface normal of the Testing set](https://1drv.ms/u/s!AvnwLMcAl2NUigb6rAUlJdD99RoU?e=p2214j).

[Surface normal of the Validation set](https://1drv.ms/u/s!AvnwLMcAl2NUigVC8rN5HG8zVosC?e=vyQXiF).


# Submit Your Result

The testing set contains only (1) Color image and (6) Intrinsic matrix of the camera. Please submit your layout estimation result of the testing set to email <info@vsislab.com> or <chluzhre@gmail.com> for performance evaluation. Please note to keep your information correct.

### What to submit
A matlab structure containing the following fields:

- **point** (u, v, Z) coordinates of the layout corners. u and v are the pixel coordinates with the oringin in the top-left of the image. Z is the depth. 

- **layout** The room layout segmentation mask.

- **depth** The depth map of the surfaces.

The result should be a single file in HDF5 format (the default format from “save” function in Matlab).


# References

[1] Angel Chang, Angela Dai, Thomas Funkhouser, Maciej Halber, Matthias Niessner, Manolis Savva, Shuran Song, Andy Zeng, and Yinda Zhang. Matterport3d: Learning from rgb-d data in indoor environments. arXiv preprint arXiv:1709.06158, 2017. 5

# Contact Us

Email | <info@vsislab.com>, <chluzhre@gmail.com>, <yindaz@gmail.com>


# License

[MIT Liscence](https://raw.githubusercontent.com/vsislab/Matterport3D-Layout/master/LICENSE.txt)

Copyright © 2019VSISLab. 
