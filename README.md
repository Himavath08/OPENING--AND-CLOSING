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

``` Python
NAME:Himavath
reg no:212223240053
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
![image](https://github.com/user-attachments/assets/2526abb3-4c19-4c14-8613-f43cdbd3088b)


### Display the result of Opening
![image](https://github.com/user-attachments/assets/e66fdec0-d70f-4184-b882-c88ee1194ac5)

### Display the result of Closing
![image](https://github.com/user-attachments/assets/5cca91f3-de91-4e9f-a08e-da69b2edb97b)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
