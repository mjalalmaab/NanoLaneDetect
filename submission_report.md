# **Finding Road Lane Lines** 

Finding road lanes from camera images is a crucial task for self-driving vehicles. Computer vision plays an improtant role for this feature. Accordingly, multiple image processing techniques should be applied to the recieved images from camera to detect properly the road lanes. 

In this project, NanoLaneDetect, a lane detection based on Canny technique, Hough lines, and region of interests is developed.

## 1. Pipeline 
The main steps of image processing for lane detection in this project are the following:
* Gray-scale conversion
* Canny algorithm to detect high gradient color changes
* Filtering-out out of the region of interest image data
* Hough line detection from canny algo outputs


In order to draw a single line on the left and right lanes, I modified the draw_lines() function by:
* fiding the slope for each line
* filtering the lines with too horizental slopes (less than 20 deg)
* extending the lines to reach to the botton of the image


![alt text][image1]



[//]: # (Image References)

[image1]: ./test_images_output/solidWhiteRight.jpg "Extended Line Drawing"

---





## 2. Pipleline shortcomings


One potential shortcoming would be what would happen when the curve is too much.

Another shortcoming could be having too much shadow.


## 3. Possible improvements to this pipeline

A possible improvement would be to finding a solution to handle the curves and shadow.