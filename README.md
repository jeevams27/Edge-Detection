# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.
<br>


### Step2:
Read the image and cconvert into gray image.
<br>

### Step3:
Remove the noise of the image using gaussian operator.
<br>

### Step4:
Find the sobel edge,laplacian edge,canny edge using the built in modules available in opencv.
<br>

### Step5:
Plot the edged image using matplotlib.


<br>

 
## Program:

``` Python
# Import the packages
import cv2
import matplotlib.pyplot as plt


# Load the image, Convert to grayscale and remove noise
img=cv2.imread("flowers.jpg")
gray=cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray,(3,3),0)



# SOBEL EDGE DETECTOR
sobelx = cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
sobely = cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
sobelxy = cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
plt.subplot(2,2,1),plt.imshow(img,cmap = 'gray')
plt.title('Original'), plt.xticks([]), plt.yticks([])
plt.show()
plt.figure(1)
plt.subplot(2,2,1),plt.imshow(sobelx,cmap = 'gray')
plt.title('soblex'), plt.xticks([]), plt.yticks([])
plt.show()
plt.figure(1)
plt.subplot(2,2,1),plt.imshow(sobely,cmap = 'gray')
plt.title('sobley'), plt.xticks([]), plt.yticks([])
plt.show()
plt.axis()
plt.figure(1)
plt.subplot(2,2,1),plt.imshow(sobelxy,cmap = 'gray')
plt.title('soblexy'), plt.xticks([]), plt.yticks([])
plt.show()


# LAPLACIAN EDGE DETECTOR
laplacian = cv2.Laplacian(img,cv2.CV_64F)
plt.figure(1)
plt.subplot(2,2,1),plt.imshow(laplacian,cmap = 'gray')
plt.title('laplacian_operator'), plt.xticks([]), plt.yticks([])
plt.show()



# CANNY EDGE DETECTOR
canny_edges = cv2.Canny(img, 120, 150)
plt.figure(1)
plt.subplot(2,2,1),plt.imshow(canny_edges,cmap = 'gray')
plt.title('canny_operator'), plt.xticks([]), plt.yticks([])
plt.show()





```
## Output:
### SOBEL EDGE DETECTOR
![](./1.jpg)
<br>
<br>
<br>
<br>
<br>
<br>


### LAPLACIAN EDGE DETECTOR
![](./2.jpg)
<br>
<br>
<br>
<br>
<br>
<br>


### CANNY EDGE DETECTOR
![](./3.jpg)
<br>
<br>
<br>
<br>
<br>
<br>

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
