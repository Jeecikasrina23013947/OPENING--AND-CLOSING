# EXP-10-OPENING--AND-CLOSING
### Name - JEECIKASRINA M
### Register Number - 212223100015
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
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img = np.zeros((300, 600), dtype='uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, "JEECIKASRINA", (5, 150), font, 3, (255), 5, cv2.LINE_AA)
cv2.imshow("Original", img)
cv2.waitKey(0)

# Create the structuring element
kernel_open = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
kernel_close = cv2.getStructuringElement(cv2.MORPH_RECT, (11, 11))

# Use Opening operation
opened = cv2.morphologyEx(img, cv2.MORPH_OPEN, kernel_open)
cv2.imshow("Opening", opened)
cv2.waitKey(0)

# Use Closing Operation
closed = cv2.morphologyEx(img, cv2.MORPH_CLOSE, kernel_close)
cv2.imshow("Closing", closed)
cv2.waitKey(0)
```
## Output:

<img width="494" height="91" alt="image" src="https://github.com/user-attachments/assets/4a63b137-0a15-4ef9-a4e3-35dd020f4076" />
<img width="494" height="87" alt="image" src="https://github.com/user-attachments/assets/422fa769-eec1-41b8-b412-f2df8ab18ce8" />
<img width="493" height="88" alt="image" src="https://github.com/user-attachments/assets/ebe717aa-23f7-4693-8e02-d331298e8db4" />

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
