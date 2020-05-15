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

My pipeline consisted of 5 steps. 
step 1: converte the images to grayscale.

step 2: use the gaussian function to blur images for reducing the noise.

step 3: use canny function to find edges.

step 4: find interest regions.

step 5: use hough function to find interested lines.


In order to draw a single line on the left and right lanes, I modified the draw_lines() function.

Instead of using many small lines and draw them I choose the method to find the slope and intercpet

of the left and right lines and draw them once. I use the linear regression function to find them and

discard some noise small lines. 

Because there maybe several left or right lines, I filter some lines if they have some differenr slope

than the median slope.


If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]

[image1]: ./examples/grayscale.jpg "Grayscale"


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the line is curved



### 3. Suggest possible improvements to your pipeline

A possible improvement would be to use k-mean algorithm to cluster two lines and then use polynomial function

to model them.


