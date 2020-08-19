

[Home](https://vsislab.github.io/Matterport3D-Layout/)|[Leader Board](#leader-board)|[Datasets](#dataset)|[Submit Result](#submit-your-result)|[References](#references)|[Contact Us](#contact-us)|[Liscense](#license)


# Welcome to Matterport3d-Layout Dataset website.
<p align="justify">
We construct a new [Dataset](#dataset) for layout estimation, which contains pixel-wise depth label for the dominant planes of the room images. Our [dataset](#dataset) uses the indoor images and depth maps from the Matterport3D dataset [1], which has large-scale RGB-D data in indoor scenes. All the images have the resolution of 1024x1280.
</p>
<p align="justify">
The original Matterport3D dataset includes 90 distinct buildings. we randomly split the dataset by the buildings. The training set includes 64 buildings with a total of 4939 images. The validation set includes 6 buildings with 456 images. The testing data includes the rest 20 buildings with a total of 1965 images. The dataset contains the following data field: 
</p>

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



# Dataset Download

<p align="justify">
You should first request access to [Matterport3D dataset](https://niessner.github.io/Matterport/) as our dataset is based on Matterport3D. Please fill and sign the [Terms of Use](http://kaldir.vc.in.tum.de/matterport/MP_TOS.pdf) agreement form and send it to matterport3d@googlegroups.com to request access to Matterport3D dataset. If your request is approved, please send us their reply email to get access to our dataset.
</p>

# Submit Your Result

The testing set contains only (1) Color image and (6) Intrinsic matrix of the camera. Please submit your layout estimation result of the testing set to email <info@vsislab.com> or <chluzhre@gmail.com> for performance evaluation. Please note to keep your information correct. 

### What to submit
A matlab structure containing the following fields:

- **point** (u, v, Z) coordinates of the layout corners. u and v are the pixel coordinates with the oringin in the top-left of the image. Z is the depth. 

- **layout** The room layout segmentation mask.

- **depth** The depth map of the surfaces.

The result should be a single file in HDF5 format (the default format from “save” function in Matlab).


# References

[1] Angel Chang, Angela Dai, Thomas Funkhouser, Maciej Halber, Matthias Niessner, Manolis Savva, Shuran Song, Andy Zeng, and Yinda Zhang. Matterport3d: Learning from rgb-d data in indoor environments. International Conference on 3D Vision (3DV), 2017.

# Contact Us

Email | <info@vsislab.com>, <chluzhre@gmail.com>, <yindaz@gmail.com>

# License

The original data from Matterport3D dataset is released under [Terms of Use](http://kaldir.vc.in.tum.de/matterport/MP_TOS.pdf)  agreement.

The part of our annotation and generated layout data is under [MIT Liscence](https://raw.githubusercontent.com/vsislab/Matterport3D-Layout/master/LICENSE.txt)

Copyright © 2019VSISLab. 

