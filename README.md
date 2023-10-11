# OPENING--CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

## Program:
```
Developed By: Dharini PV
Register Number: 212222240024
```
# Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```python
image=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
cv2.putText(image,'Dharini PV',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(image,cmap='gray')
plt.title('Input Text'), plt.xticks([]), plt.yticks([])
plt.show()
```
# Create the structuring element
```python
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Use Opening operation
```python
image2=cv2.morphologyEx(image,cv2.MORPH_OPEN,kernel)
plt.imshow(image2,cmap='gray')
plt.title('OPENING'), plt.xticks([]), plt.yticks([])
plt.show()
```
# Use Closing Operation
```python
image2=cv2.morphologyEx(image,cv2.MORPH_CLOSE,kernel)
plt.imshow(image3,cmap='gray')
plt.title('CLOSING'), plt.xticks([]), plt.yticks([])
plt.show()
```
## Output:

### Display the input Image
![Screenshot from 2023-10-11 18-32-51](https://github.com/DHARINIPV/OPENING--CLOSING/assets/119400845/9e46ff95-eb3d-4ea5-99b0-d5db8a4417a5)

### Display the result of Opening
![Screenshot from 2023-10-11 18-34-09](https://github.com/DHARINIPV/OPENING--CLOSING/assets/119400845/aef05619-21f9-4e5b-90dd-1d8b2e347f97)

### Display the result of Closing
![Screenshot from 2023-10-11 18-35-06](https://github.com/DHARINIPV/OPENING--CLOSING/assets/119400845/be23c3a8-1547-4bdc-b3cc-4661ad513b60)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
