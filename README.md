# retinal-image-processing

Some functions for image pre-processing before training a deep learning model with these images.

### Function 1
To distinguish whether an image is of high enough quality/resolution to be used for training. Two steps were invovled. 
1. Cheking the brightness of the image, as all images below a certain brightness, as was determined, are not suitable
2. Checking if the optic disc (bright spot in all retinal images) can be identified and isolated, as this is the most important part of the image

Whichever image passes both of these tests is suitable to be used to train the model


### Function 2
Crops a retinal image to a square aligned with the edges of the retina, so as to remove unneccesary black space in the picture. Some images contain random white characters (bright colour) on the black space, so this prevented a simple brightness checking function from being used to identify the black space and remove it.
A mask and morphology function needed to be used to ignore the white text and shapes and threshold the regions, and findContours was used to locate the edges of the image so as to crop the image to the appropriate size.

An example of an uncropped and cropped image is shown below:

Uncropped:

<img width="483" alt="Screenshot 2023-07-05 at 12 56 39 PM" src="https://github.com/magichampz/retinal-image-processing/assets/91732309/44c3b788-a73e-4159-b77c-e08311be80da">


Cropped:

![image](https://github.com/magichampz/retinal-image-processing/assets/91732309/1e78cb0f-f03f-4cdf-a5d4-c70255e6e3b4)
