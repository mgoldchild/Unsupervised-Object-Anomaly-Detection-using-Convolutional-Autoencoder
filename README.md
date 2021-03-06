# Unsupervised-Object-Anomaly-Detection-using-Convolutional-Autoencoder

## References:
- P. Bergmann, S. L ̈owe, M. Fauser, D. Sattlegger, and C. Steger.  Improving Unsupervised Defect Segmentation by Applying Structural Similarity to Autoencoders. 
- P. Bergmann, M. Fauser, D. Sattlegger, and C. Steger. MVTec AD — a Comprehensive Real-World Dataset for Unsupervised Anomaly Detection.

## Dataset source
Free to download at
https://www.mvtec.com/company/research/datasets/mvtec-ad/

## Dependencies
`tensorflow==1.15` <br>
`keras==2.0` <br>
`scikit-image==0.16` <br>
`imgaug==0.4.0` <br>
`matplotlib` <br>
`cv2` <br>

## Features
- Contraction path of the Conv2D autoencoder is inspired from AlexNet architecture, and the expansion path is an exact inverse of an contraction path
- Extremely convenient data augmentation and input noise addition using `imgaug` library !
- SSIM Loss function -> images need to be preprocessed to grayscale for optimal performance
- Segment and visualize the defect using two difference images: SSIM metric & L2 metric

## Room for improvements
- Alexnet seems to be not deep enough as an contraction path, need deeper autoencoder
- Even non-anomalous images give some considerable difference score when compared to the reconsturcted image, need to introduce some robustness

### SSIM difference image between the original (anomalous) and reconstructed image

![Sample visuals of SSIM difference metric](/visuals/1.PNG)


### Scatter plot of difference scores generated from SSIM and L2 metric 
Blue: Non anomlaous tesing image <br>
Green: Anomlaous testing image

![Sample visuals of SSIM difference metric](/visuals/2.PNG)


