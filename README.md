# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step-1:
Create a black image of size 100x600 pixels.
### Step-2:
Use a specified font to write the word "Lifestyle" on the image at a defined position.
### Step-3:
Show the image containing the text without axis labels.
### Step-4:
Define a structuring element for morphological operations (e.g., a cross-shaped kernel).
### Step-5:
Apply erosion to the image using the defined structuring element to reduce the size of white regions.
### Step-6:
Apply dilation to the original image using the same structuring element to increase the size of white regions.
 
## Program:
```
Developed By: KISHORE.B
Reg.No: 212222110020
```
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt

img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'KISHORE',(80,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
![image](https://github.com/user-attachments/assets/8ce051c3-af76-4cc5-aeef-005ad1b9f064)
```
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
```
# Erode the image

img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
### Display the Eroded Image
![image](https://github.com/user-attachments/assets/055d0572-b867-4f8d-8075-47aec6f9338e)

```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')

```
### Display the Dilated Image
![image](https://github.com/user-attachments/assets/f809a80a-7020-4154-b2d5-abf467953a8c)
## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
