# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

### Code:
## Original:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('spyd.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
## SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
## LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
## CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```

## Output:
### Original:
![432611313-e641dfc8-844a-4bf4-8b78-3b68273b3e10](https://github.com/user-attachments/assets/f3bb197f-063c-4f17-9431-2cf33e9c6505)

### SOBEL EDGE DETECTOR
![432611446-97943629-bf83-45e8-893a-c9746f6e2166](https://github.com/user-attachments/assets/edd11151-b92e-4886-a302-e3d0c1784e4b)

### LAPLACIAN EDGE DETECTOR
![432612798-e2d0f3d1-cb0b-408b-8aed-b7d716455083](https://github.com/user-attachments/assets/3111d389-c1f5-4b14-9cdd-21b9ad348c31)

### CANNY EDGE DETECTOR
![432614026-746f27a7-75ab-4114-b93b-c6242492f713](https://github.com/user-attachments/assets/8ce50b0a-7e91-425c-9eec-164573ebf301)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
