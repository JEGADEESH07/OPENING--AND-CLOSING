# EX 10 OPENING AND CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
- Step1: Import the necessary packages
- Step2: Give the input text using cv2.putText()
- Step3: Perform opening operation and display the result
- Step4: Similarly, perform closing operation and display the result
## Program:
```
NAME: JEGADEESH S
REG.No: 212222230055
``` 
# Import the necessary packages
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```python
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Data Scientist',(4,70), font,1,(255),5,cv2.LINE_AA)
```
# Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Use Opening operation
```python
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```
# Use Closing Operation
```python
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:
### Display the input Image
![image](https://github.com/JEGADEESH07/OPENING--AND-CLOSING/assets/113497131/359c224d-a117-416c-b2e9-40d4cffb8753)
### Display the result of Opening
![image](https://github.com/JEGADEESH07/OPENING--AND-CLOSING/assets/113497131/b1d13cce-fbbd-4c3d-babd-a4bb0cd5f64a)
### Display the result of Closing
![image](https://github.com/JEGADEESH07/OPENING--AND-CLOSING/assets/113497131/361f93f7-6816-4bd5-82f6-a3dc716f2b93)
## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
