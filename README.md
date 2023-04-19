# Edge-Linking-using-Hough-Transform
## Aim:
To write a Python program to detect the lines using Hough Transform.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary Python libraries which are required for the program.
<br>

### Step2:
Load a image using imread() from cv2 module.
<br>

### Step3:
Convert the image to grayscale.
<br>

### Step4:
Using Canny operator from cv2,detect the edges of the image
<br>

### Step5:
Using the HoughLinesP(),detect line co-ordinates for every points in the images.Using For loop,draw the lines on the found co-ordinates.Display the image.
<br>


## Program:
## Developed By: Senthil Kumar S
## Reg No: 212221230091
```Python
import cv2
import numpy as np
img=cv2.imread('bankai.jpg',0)
cv2.imshow("gray",img)
edges1 = cv2.Canny(img,100,200)
lines=cv2.HoughLinesP(edges1,1,np.pi/180, threshold=80, minLineLength=20,maxLineGap=20)
for line in lines:
    x1, y1, x2, y2 = line [0] 
    cv2.line(edges1,(x1, y1),(x2, y2),(255, 0, 0),3)
cv2.imshow('hough',edges1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output

### Grayscale image

![bankai1](https://user-images.githubusercontent.com/93860256/233029011-fe08911a-1d41-4bd9-b737-9d07ea795354.png)

### Hough transform

![bankai2](https://user-images.githubusercontent.com/93860256/233028995-0d5d103f-e6be-4a13-9206-c42fa4f72c8e.png)


## Result:
Thus the program is written with python and OpenCV to detect lines using Hough transform. 
