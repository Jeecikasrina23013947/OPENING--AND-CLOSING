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
cv2.putText(img, "Kamesh", (5, 150), font, 3, (255), 5, cv2.LINE_AA)
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

### Display the input Image
![WhatsApp Image 2025-11-17 at 11 04 25 AM (2)](https://github.com/user-attachments/assets/ef95ece7-2785-4916-9885-121d2dc8143f)


### Display the result of Opening
![WhatsApp Image 2025-11-17 at 11 04 25 AM (1)](https://github.com/user-attachments/assets/296cf431-232b-4184-a2d7-fbf26e010760)



### Display the result of Closing
![WhatsApp Image 2025-11-17 at 11 04 25 AM](https://github.com/user-attachments/assets/b9c3dc1f-1b81-4792-816b-b62f31a7a69c)




## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
