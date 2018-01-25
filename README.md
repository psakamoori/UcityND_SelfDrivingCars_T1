## Finding Lane Lines

### Overview
  The script LaneDetect.ipynb is used to detect lane lines in a given test image/video file
 
### Pipeline

1. Reads each image file from a given directory "test_image/"
2. Converts it from RGB to Gray 
3. Follwed by Gaussian filter (smoothing) with specific kernel_size
4. Output of Gaussian Filter is feed into CannyEdge detector (with specific low and hight threshold values)
5. We then select regio of Interest (ROI) (Vertices are predfined/tuned for give test inputs)
6. We then run hough transform (which converts points in image place to lines in hough plane), which is heart of
   detecting lane lines in a give image/frame
7. Finally get left and right lanes point corrdinates (w.r.t vertices reference) and draw the lines (using cv2.line)

Note:
-> I am using python2.7
-> Extrapolation of lane points are pending
-> Challenge.mp4 was a real challenge to detec lanes in that. (Need to find tune my parameters)
  
