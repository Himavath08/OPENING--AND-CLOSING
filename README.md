# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

## Program:
## NAME:Himavath M
## Reg no:212223240053
```
from IPython import get_ipython
from IPython.display import display

import cv2
import numpy as np
import matplotlib.pyplot as plt

from google.colab.patches import cv2_imshow

img1=np.zeros((300,600),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"Hiamavath",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)

cv2_imshow(img2)

kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(11,11))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(5,5))

img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)

cv2_imshow(img4)

img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)

cv2_imshow(img3)


```
## Output:

### Display the input Image
![image](https://github.com/user-attachments/assets/117be1e1-a9c5-4113-95dd-fd666d90164e)

### Display the result of Opening
![image](https://github.com/user-attachments/assets/cb05f756-9a96-48bd-9511-37b4172587c8)

### Display the result of Closing
![image](https://github.com/user-attachments/assets/6ccb36e7-f2d8-4212-a9ec-8cec0ab7a95d)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
