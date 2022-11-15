# Face-Detection-in-the-dark
A Face Detection model Using TinaFace, EnlightenGAN and Multi-Stage Progressive Image Restoration.

## Description 
A UG2+ 2021 Track1.2 challange in CVPR 21.
Official Website: http://www.ug2challenge.org/

## Method
- The input image is first "light enhanced" using a GAN based network named EnlightenGAN.More information can be found here https://github.com/VITA-Group/EnlightenGAN. The implementation of this step can be in `Enlightning_Dark_Images.ipynb`.
- The image from the last step is then passed through a Multi-Stage Progressive Image Restoration module for denoising the image. More information can be found here https://github.com/swz30/MPRNet.git. The implementation of this step can be in `Denoising.ipynb`.
- Finally the image is input to the TinaFace model. More information can be found here https://github.com/Media-Smart/vedadet/tree/main/configs/trainval/tinaface. The implementation of this step can be in `Tina_Nikhil.ipynb`.

## Postscript
This network after training for ~ 40 hours(which is the 20% of the total training time according to the authors of tinaFace) gave a mAP of 0.58. The best model in the challange gave close to 0.74 [leaderboard](http://cvpr2021.ug2challenge.org/leaderboard21_t1.html).
I couldn't Tain the model completely because of the lack of resources. Feel free to use the codes if you have multiple Good GPUs.

