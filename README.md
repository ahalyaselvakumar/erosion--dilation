# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Create a blank image.

### Step2:
Create a structuring element (5x5 rectangular)

### Step3:
Erode the image.

### Step4:
Dilate the image.

### Step5:
End the program.

 
## Program:

``` Python
import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'AHALYA' ,(5,70),font,4,(255),2,cv2.LINE_AA)


# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)

# Display the results
plt.figure(figsize=(12, 5))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')

```
## Output:

### Display the input Image
<img width="438" height="142" alt="image" src="https://github.com/user-attachments/assets/7ad4077b-1a50-4d8a-8a1c-d775567f2d14" />


### Display the Eroded Image

<img width="417" height="140" alt="image" src="https://github.com/user-attachments/assets/794e47c8-6f15-4dc7-9c3d-e8c8ccc22e2a" />



### Display the Dilated Image
<img width="415" height="155" alt="image" src="https://github.com/user-attachments/assets/c2fa55a4-a1be-4674-945c-17fee72cdf3e" />



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
