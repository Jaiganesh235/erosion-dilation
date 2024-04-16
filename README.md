# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary libraries (OpenCV and NumPy).

### Step2:
Use cv2.putText to add the text to the img1 image at specific coordinates.

### Step3:
Define two kernels (kernel and kernel1) for morphological operations.

### Step4:
Display the eroded image using cv2.imshow.

### Step5:
Use cv2.waitKey(0) to wait for a key press indefinitely.
 
## Program:
```
DEVELOPED BY: S.JAIGANESH
REG NO: 212222240037
```
### Import the necessary packages
```
import cv2
import numpy as np
```
### Create the Text using cv2.putText
```
img1=np.zeros((100,400),dtype="uint8")
font=cv2.FONT_HERSHEY_PLAIN
cv2.putText(img1,"S JAIGANESH",(5,70),font,2,(255),5,cv2.LINE_AA)
cv2.imshow("image",img1)
cv2.waitKey(0)
```
### Create the structuring element
```
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
### Erode the image
```
cv2.erode(img1, kernel)
image_erode = cv2.erode(img1,kernel1)
plt.imshow(image_erode)
plt.axis('off')
```
### Dilate the image
```
image_dilatel=cv2.dilate(img1,kernel1)
plt.imshow(image_dilatel)
plt.axis('off')
```
## Output:

### Display the input Image



### Display the Eroded Image



### Display the Dilated Image



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
