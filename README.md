# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

### Step1:
Import the necessary pacakages


### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

 
## Program:

```python
#DEVELOPED BY : NITHEESH YEGAVINTI
#Reg No: 212224040370

```


##### Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
##### Create the Text using cv2.putText
``` Python
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'NITHEESH' ,(5,70),font,4,(255),2,cv2.LINE_AA)


```
##### Create the structuring element
``` Python
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

```
##### Erode and dilate  the image
```
img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)

```
#####  Display the results
```
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

<img width="745" height="163" alt="image" src="https://github.com/user-attachments/assets/7307acce-bba1-41f0-9262-191f80a2d037" />


### Display the Eroded Image and Dilated Image

<img width="1324" height="176" alt="image" src="https://github.com/user-attachments/assets/f7a561ea-b87e-4d80-b6e9-e86a8240df91" />



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
