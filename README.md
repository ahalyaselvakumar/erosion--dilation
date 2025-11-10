# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Create a black image of size 100x600 pixels.

### Step2:

Use a specified font to write the word "Lifestyle" on the image at a defined position
### Step3:

Show the image containing the text without axis labels.

### Step4:
Define a structuring element for morphological operations (e.g., a cross-shaped kernel)

### Step5:
Apply erosion to the image using the defined structuring element to reduce the size of white regions.
### step 6:

 Apply dilation to the original image using the same structuring element to increase the size of white regions.
## Program:

# Name: AHALYA S
# Regno: 212223230006

```
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
img = np.zeros((100, 600, 3), dtype='uint8')  # Black background (RGB: 0, 0, 0)
font = cv2.FONT_HERSHEY_COMPLEX
text_color = (255, 255, 255)  # White text (RGB: 255, 255, 255)
cv2.putText(img, 'Pavithra S', (60, 70), font, 2, text_color, 5, cv2.LINE_AA)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.axis('off')
plt.show()


# Create the structuring element
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)


# Erode the image
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')


# Dilate the image
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')

```
## Output:

### Display the input Image
<img width="459" height="84" alt="Screenshot 2025-11-02 210651" src="https://github.com/user-attachments/assets/49149362-1b85-45b2-986b-4ee2813b2cc4" />


### Display the Eroded Image
<img width="534" height="114" alt="Screenshot 2025-11-02 210659" src="https://github.com/user-attachments/assets/8f1f97a4-9dff-4681-8426-df50be3758b0" />



### Display the Dilated Image

<img width="490" height="112" alt="Screenshot 2025-11-02 210705" src="https://github.com/user-attachments/assets/2341da5f-0a87-4f1f-a8c6-edbc643d094b" />

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
