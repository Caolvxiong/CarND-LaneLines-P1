# **Finding Lane Lines on the Road** 

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

---

### Reflection

### 1. Description

My pipeline consisted of 6 steps. 

+ Converted the images to grayscale, applied Gaussian smoothing
+ Applied Canny to images to find edges
+ Masked the erea we interested in
+ Defined Hough parameters and found lines using Hough Transform
+ Drew the lines on the copied image
+ Applied the code on videos

#### About the draw_lines() function:
I spent lot of time on this. 
The basic idea is to find left or right line based on each line's slope. Firstly, I tried to find the left/right most points, and average them to draw the lines. But that didn't work because some points are too far from the lines. So I changed algorithm to find all points's average instead of the most right or left ones. But it made my code so complecated. So finally I found a method `np.polyfit`, which is so greate that saves lot of effort. I used it to find line's params, then calculated points that on the edges of our area.


### 2. Identify potential shortcomings with your current pipeline

It doesn't work well on the challage, I should polish the code and tune the params.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to make the workplace easier to use. Sometimes I have to scoll up and down to find the code and words. 
But it is a great tool in general.
