# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 7 steps as follows,
1. grayscale the image
2. define kernel size and apply Gaussian smoothing
3. apply Canny edge
4. mask the image
5. Define the Hough transfer parameters, and apply Hough transfermation
6. Draw the line on the blank image
7. Combine the line image with the original image

Modified the draw_lines() function
1. change the line thickness to 4, make it more legible
2. define the y_max to be the hight of the image and y_min to be 65% of the hight
3. sepreate the lines into 2 group (left_lines and right_lines) based on the slope.
4. do the curve fit for all the points of left lines and right lines and find the optimal slope and intercept


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the line are curved 
Another shortcoming could be if there are cars cross the line in the front.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to change the curve fit order, i.e. instead of straight lines, we can define a curved line model

Another potential improvement could be to machine learning algrithm.
