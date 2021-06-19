# CartoonImageOpenCV
>Cartooning an image using Open CV python module
-In order to get the basic cartoon effect, we just need the bilateral filter and some edge detection mechanism. We use a Gaussian pyramid for the images to be weighted down (down-sampling) using a Gaussian average (Gaussian blur) and scaled down. Each pixel containing a local average corresponds to a neighborhood pixel on a lower level of the pyramid. This technique is used especially in texture synthesis.
-The bilateral filter will reduce the color palette, which is essential for the cartoon look and edge detection is to produce bold silhouettes. The basic idea underlying bilateral filtering is to do in the range of an image what traditional filters do in its domain. Two pixels can be close to one another, that is, occupy nearby spatial location, or they can be similar to one another, that is, have nearby values, possibly in a perceptually meaningful fashion.
-We are going to use openCV python library to convert an RGB color image to a cartoon image.

>Algorithm
Firstly apply the bilateral filter to reduce the color palette of the image.
Then convert the actual image to grayscale.
Now apply the median blur to reduce image noise in the grayscale image.
Create an edge mask from the grayscale image using adaptive thresholding.
Finally combine the color image produced from step 1 with edge mask produced from step 4.

