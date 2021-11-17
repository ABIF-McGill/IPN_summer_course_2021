# IPN_summer_course_2021

## Lesson 6 Quantitative Image Analysis 

This lesson was given over Zoom on August 11th 2021 - no recording is publically available. This lesson is based on our workshop on the basics on image processing and analysis in Fiji, given in May 2020. 

In this repository you will find the images needed for today's interactive activity on image analysis.

<br />

## Download image data and Fiji

**To download the images** click on the green Code button, and then "Download ZIP". Then, you can extract images (ending in .tif) in Windows / OS X.

To download Fiji/ImageJ [click here](fiji.sc)



<br />


## Objective: Learn basics of opening images in Fiji, processing and object segmentation

The following is meant as a general guideline. We will discuss how to do this and why in class.

### Part 1) Loading an image in Fiji

In this section, we'll load an image in Fiji, and get familiarized with Fiji. We'll look at pixel intensity values and coordinates, adjust display contrast and LUTs.


### Part 2) Segment nuclei from an image of Hoechst stained nuclei and measure intensity

1) Open Fiji, then open the Hoechst image (“ESCs_WT_020_Ch2_Hoechst.tif") in Fiji by
dragging the file into the main window.

2) Duplicate the image.

3) Fluorescence images have a bit of noise, so try applying a Median Filter (with a radius of 1
pixel), to filter out some of that noise.

4) Since the staining has high variance, try applying a gaussian blur, to blur out the image a
little bit, to make thresholding easier.

5) Duplicate the gaussian blurred image from Step 4, then try to find a Threshold value which
will clearly delineate nuclei from background. Don’t worry if it’s not perfect - it never is!

6) If you have found a decent threshold value, try applying that threshold to generate a binary
image.

7) If the binary image has holes inside the nuclei, try to find a way to Fill Holes.

8) At this point, the measurements that will be made need to be set in Fiji. Open Set
Measurements, and select measurements which might be interesting, such as the area,
mean intensity, intensity standard deviation, etc.

9) On the binary image, try to create ROIs manually by using the Magic Wand Tool, like the
one in Photoshop, and press “T” to store the ROIs - alternatively, try to get Fiji to find all the
ROIs by using Analyze Particles. Once you have some Regions of Interest, open the U1-
GFP image (“ESCs_WT_020_Ch1_U1GFP.tif”), and use the ROIs that were created with the
Hoechst image to Measure U1-GFP intensity inside each nuclei. 


<br />
