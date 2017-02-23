#**Finding Lane Lines on the Road** 

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./images/img.jpg "Pipeline Output"

---

### Reflection

My pipeline consisted of 6 steps. First, I converted the images to grayscale, then I applied canny transformation which will
automatically compute the threshold and apply it. Then I converted yellow lines to white to avoid innacurate
line recognition. Then I applied gaussian blur to the image. After that I have defined the region of interest and drew the lines.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by automatically computing the slope
and intercepts of the line and drawing a new extended line based on the calculated slope and the intercepts.

![alt text][image1]

One potential shortcoming would be what would happen when the roads are hilly or not exactly flat.
Another shortcoming could be that the extended lines would overlap sometimes.
Anotehr shortcoming could be that the right or left lanes depending on what side of the road you drive on, 
would extend when there is an exit ramp because there is a too big of a gap between the lines.

A possible improvement would be to fix the high Y threshold and fix the occasional overlap of extended lines
Another potential improvement could be to improve the recognition on non-flat/hilly roads.
