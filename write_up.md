# **Finding Lane Lines on the Road** 


### Reflection

Overview
---

When we drive, we use our eyes to decide where to go.  The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle.  Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.

In this project you will detect lane lines in images using Python and OpenCV. 


The pipeline
---
1] Read test_image and convert it into grayscale image.

2] Define a kernel size as 7 ( A larger kernel_size implies averaging, or smoothing, over a larger area), and apply Gaussian smoothing for gray scale images to get good results while Edge detection.

3] Define low threshold & high threshold parameters which perform the "Double Thresholding" step inside Canny edge detection to get egdes of the image.

4] Determine the Region of the interest and mask the image using cv2.fillPoly().

5] Define Hough Tranform lines parameters Hough tranform.Run on masked edge-detected image.

6] Drawn line segments and extroplated from line segments.

7] Combined line image with original image to see accurate line annotation.

8] Read and Save the test_image from the specified folder.

9] Rectified the overwritting problem of the output file by clearing of the previous output contents.


Potential shortcomings with current pipeline
---
One potential shortcoming would be in the challenge video when the car is moving through the curved area along the lanes determined.
Though the path detection funcytion is happening many other lines on the barriers and sideways we are getting detected, so still the lane detection is improper.

Another shortcoming could be finding the vertices in the test image has been made manually instead of taking it automatically.


Possible improvements
---
A possible improvement would be to use some machine learning/deep learning algorithm like Linear Regression , Logistic Classifier etc.So that the continuous white line or yellow line will be detected. 

Another potential improvement could be to find the vertices from the images by calculation of a some specified ratio in the test image.
