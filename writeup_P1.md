# **Finding Lane Lines on the Road** 

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

My pipeline consisted of 5 steps. 
1. converted the images to grayscale
2. I applied a 5x5 Gaussian to smooth the image
3. Canny method is used to find all the edges
4. Hough transform and quadrilateral are used to find lane lines at the front of the self-driving car
5. Draw lane lines

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by evaluating the slope ((y2-y1)/(x2-x1)) to decide which segments are part of the left line vs. the right line.

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the lane lines are  too blur or bright

Another shortcoming could be that if the road curve is too high or the car is steering, the detection will be problem.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to integrate HSV color model.

Another potential improvement could be to modify the 1-order fitpoly to 2-order or higher.
