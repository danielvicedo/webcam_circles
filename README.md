# Webcam Circles

Initial Fork from: https://github.com/beta-robots/webcam_circles

## The Hough Transform

The Hough Transform is an image analysis algorithm which can detect simple forms. It is mostly used in computer analysis and image processing. Initially this transform was created to detect lines but with years later it expanded its borders onto circles and ellipses.

### Parameters

**MIN_RADIUS and MAX_RADIUS**

Those parameters limit the minimum and maximum radius of which the circles can have. Too big of a MIN_RADIUS and some small circles might not be detected. Same happens with too small of a MAX_RADIUS, where some bigger circles might be missed.

**MIN_CIRCLE_DIST**

This parameter limits the minimum distance between circles. More precisely, the center of those circles. If the number is too small more than one circle may be detected from the same center-point of a circle.

![ScreenShot](https://github.com/danielvicedo/webcam_circles/blob/master/media/MIN_CIRCLE_DIST.png)

**HOUGH_ACCUM_RESOLUTION**

This parameter determines how close the detection is in comparison to the real image. It is related to the inverse of the resolution of the image.

**CANNY_EDGE_TH**

This parameter is related to the Canny algorithm. It is used to detect edges inside the image. If it is too small it will falsely detect some extra circles.

![ScreenShot](https://github.com/danielvicedo/webcam_circles/blob/master/media/CANNY_EDGE.png)

**HOUGH_ACCUM_TH**

This parameter is used as a threshold where above it the code will search for a circle. If it is too small, false circles may be detected around the true center of the original circle.

![ScreenShot](https://github.com/danielvicedo/webcam_circles/blob/master/media/HOUGH_ACCUM_TH.png)


- **Bibliography**

- https://docs.opencv.org/2.4/doc/tutorials/imgproc/imgtrans/hough_circle/hough_circle.html
- https://www.pyimagesearch.com/2014/07/21/detecting-circles-images-using-opencv-hough-circles/
