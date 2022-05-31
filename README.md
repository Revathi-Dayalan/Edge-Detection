# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>
Import the required packages for further process.


### Step2:
<br>
Read the image and convert the bgr image to gray scale image.

### Step3:
<br>
Use any filters for smoothing the image to reduse the noise.

### Step4:
<br>
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step5:
<br>
Display the filtered image using plot and imshow.
 
## Program:

``` Python
# Import the packages

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("dogs.jpeg")

# Load the image, Convert to grayscale and remove noise

gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)

# SOBEL EDGE DETECTOR

# SOBEL X

sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img)
plt.title('Image')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap='Greys')
plt.title("Sobel X")
plt.xticks([])
plt.yticks([])
plt.show()

# SOBEL Y
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img)
plt.title('Image')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap='Greys')
plt.title("Sobel-Y")
plt.xticks([])
plt.yticks([])
plt.show()

# SOBEL XY
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img)
plt.title('Image')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap='Greys')
plt.title("Sobel XY")
plt.xticks([])
plt.yticks([])
plt.show()

# LAPLACIAN EDGE DETECTOR
laplacian = cv2.Laplacian(image,cv2.CV_64F)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img)
plt.title('Image')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap='gray')
plt.title("Laplacian")
plt.xticks([])
plt.yticks([])
plt.show()

# CANNY EDGE DETECTOR
canny_edges = cv2.Canny(image, 120, 150)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img)
plt.title('Image')
plt.subplot(1,2,2)
plt.imshow(canny_edges,cmap='gray')
plt.title("Canny Edges")
plt.xticks([])
plt.yticks([])
plt.show()



```
## Output:
### SOBEL EDGE DETECTOR
![r5](https://user-images.githubusercontent.com/96000574/171097381-f92a06d3-d634-45a1-b954-73e493ca17b8.jpeg)
![r4](https://user-images.githubusercontent.com/96000574/171097453-9dfaa8a1-2e66-4b1b-990b-a8a8c523ec01.jpeg)
![r3](https://user-images.githubusercontent.com/96000574/171097595-dee0d909-b31a-4556-8097-1e409a2497bb.jpeg)


### LAPLACIAN EDGE DETECTOR
![r2](https://user-images.githubusercontent.com/96000574/171097639-2f64fad3-0b15-43d1-a212-d50152a17a29.jpeg)




### CANNY EDGE DETECTOR
![r1](https://user-images.githubusercontent.com/96000574/171097672-782cc816-deea-4b49-9afa-b97505e64060.jpeg)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
