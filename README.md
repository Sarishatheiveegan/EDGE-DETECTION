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
#### DONE BY:MARINO SARISHA T
#### REG NO:212223240084
## PROGRAM
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```python
image = cv2.imread('house.png')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=3)  
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=3)  
sobel_edge = cv2.magnitude(sobel_x, sobel_y)
```
```python
plt.imshow(sobel_edge, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
plt.show()
```
![Screenshot 2025-04-30 115108](https://github.com/user-attachments/assets/6761d4fd-20f5-480e-bbb5-5027d8fc47e2)

```python
laplacian_edge = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian_edge, cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis('off')
plt.show()
```
![Screenshot 2025-04-30 115117](https://github.com/user-attachments/assets/dcb1329e-6148-4bb9-a2c9-ec3b2bd871cd)

```python
canny_edge = cv2.Canny(gray_image, 100, 200)
plt.imshow(canny_edge, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis('off')
plt.show()
```
![Screenshot 2025-04-30 115130](https://github.com/user-attachments/assets/785a2e17-295e-4fca-b40b-12251fa4dda5)

## Output:
### SOBEL EDGE DETECTOR
![Screenshot 2025-04-30 115108](https://github.com/user-attachments/assets/dc53eb07-c273-4f68-b959-bac1dd008bd9)

### LAPLACIAN EDGE DETECTOR
![Screenshot 2025-04-30 115117](https://github.com/user-attachments/assets/11a5b534-dfdb-4192-8ec8-5fbc87c8beb3)


### CANNY EDGE DETECTOR
![Screenshot 2025-04-30 115130](https://github.com/user-attachments/assets/7b5c9911-df56-42dc-a20f-144ae75fd964)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
