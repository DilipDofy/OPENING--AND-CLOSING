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

```

# Developed By: DILIP M P
# Register No: 212223230048

import cv2
import numpy as np
import matplotlib.pyplot as plt

#i) Create the Text using cv2.putText
img1=np.zeros((300,600),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"DILIP M P",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()

#ii) Create the structuring element
#kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
#kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(11,11))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(5,5))

#iii) Use Opening operation
img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()

#iv) Use Closing Operation
img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()



```
## Output:
 
### Display the input Image

![Screenshot 2025-05-07 083701](https://github.com/user-attachments/assets/2d58a9c5-b451-468c-aba9-44926a19af47)

### Display the result of Opening

![Screenshot 2025-05-07 083811](https://github.com/user-attachments/assets/6aa33a16-610a-49f3-900f-7ce73684a847)

### Display the result of Closing

![Screenshot 2025-05-07 083844](https://github.com/user-attachments/assets/12c1d21e-ba6f-401f-8139-13e485963777)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
