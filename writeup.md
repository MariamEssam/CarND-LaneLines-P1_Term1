# **Finding Lane Lines on the Road** 
---

**Finding Lane Lines on the Road**

Thesteps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Extrapolate Lines 


[//]: # (Image References)

[image1]: ./test_images_output/solidWhiteCurve.png "Detected Lines"
[image2]: ./test_images_output/Extrapolationresult.png "Detected Lines after Extrapolation"
---

### Reflection

### 1. Pipeline Description

As a first step is trying to detect the lane without any enhancement, here's the steps followed:
* Find the grayscale image
* Reduce Noise by blurring the image using Gaussian filter, the filter size is 5
* Detect edges using Canny function
* Mask/Crop the interseting image section
* Apply Hough Transform on the image to find connected lines.
* Draw the lines on the original image

![alt text][image1]


### 2. Enhancing the Current Detected Lines 


By averaging the right points and the left points and
calculating from them the slope of the new line one for left and one 
for right with their starts and ends.

![alt text][image2]

### 3. Possible improvements to the pipeline

As a possible improvement is to draw the lane not as staright lines but as curve 
to handle the case of exiting curve lane.
