

[Home](https://vsislab.github.io/Matterport3D-Layout/)|[Leader Board](#leader-board)|[Datasets](#dataset)|[Submit Result](#submit-your-result)|[References](#references)|[Contact Us](#contact-us)|[Liscense](#license)


# Welcome to Matterport3d Layout Dataset website.

We construct a new [Dataset](#dataset) for layout estimation, which contains pixel-wise depth label for the dominant planes of the room images. Our [dataset](#dataset) uses the indoor images and depth maps from the Matterport3D dataset [1], which has large-scale RGB-D data in indoor scenes. All the images have the resolution of 1024x1280.

The original Matterport3D dataset includes 90 distinct buildings. we randomly split the dataset by the buildings. The training set includes 64 buildings with a total of 4939 images. The validation set includes 6 buildings with 456 images. The testing data includes the rest 20 buildings with a total of 1965 images. The dataset contains the following data field: 

(i) color image; 

(ii) depth map representing the layout; 

(iii) 2D segmentation; 

(iv) original depth map containing indoor objects; 

(v) visible region annotation; 

(vi) intrinsic matrix of the camera; 

(vii) the parameters for each surface; 

(viii) (u,v,Z) coordinates of the layout corners. 

![Matterport3D](https://raw.githubusercontent.com/vsislab/Matterport3D-Layout/master/image.jpg)

# Leader Board

Method | e<sub>pixel</sub>(%) | e<sub>corner</sub>(%) | e<sub>3Dcorner</sub>(%) | RMS | REL | log10 | &delta;&lt;1.25 | &delta;&lt;1.25<sup>2</sup> | &delta;&lt;1.25<sup>3</sup>
**Ours** | **5.67** | **4.36** | **13.85** | **0.516** | **0.131** | **0.052** | **0.864** | **0.972** | **0.993**



# Dataset

[Training set on BaiduNetdisk](https://pan.baidu.com/s/1UOzlB6IKvxM90dXFJk_9zg) with password av17.

[Testing set on BaiduNetdisk](https://pan.baidu.com/s/1AbbPWaga2NPudP8_a999Lg) with password 4hv4.

[Validation set on BaiduNetdisk](https://pan.baidu.com/s/1LEbVzz0ERYp2jBYuP_uTnA) with password hhqw.

[Training set on Google Drive](https://drive.google.com/open?id=1k6tFoLpIwj1_vCHYPOSQDbpH4LrTyR8F).

[Testing set on Google Drive](https://drive.google.com/open?id=1xLRAn-9RII-jQ-8WBEF3_xBNP4YgYcva).

[Validation set on Google Drive](https://drive.google.com/open?id=1uDROzKBaJucNxGpzQeZ3tY4bc50s0rHU).


# Submit Your Result

After you finished your training and predicting your model, you can submit your result with yours by email <info@vsislab.com>. Please note that keep your information correct.

### What to submit
A matlab structure containing the following fields:

- **point** (u, v, Z) coordinates of the layout corners. u and v are the pixel coordinates with the oringin in the top-left of the image. Z is the depth. 

- **layout** The room layout segmentation mask.

- **depth** The depth map of the surfaces.

The result should be a single file in HDF5 format (the default format from “save” function in Matlab).


# References

[1] Angel Chang, Angela Dai, Thomas Funkhouser, Maciej Halber, Matthias Niessner, Manolis Savva, Shuran Song, Andy Zeng, and Yinda Zhang. Matterport3d: Learning from rgb-d data in indoor environments. arXiv preprint arXiv:1709.06158, 2017. 5

# Contact Us

Email | <info@vsislab.com>


# License

[MIT Liscence](https://raw.githubusercontent.com/vsislab/Matterport3D-Layout/master/LICENSE.txt)

Copyright © 2019VSISLab. 
