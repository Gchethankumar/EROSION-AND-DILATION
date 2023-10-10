# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:

### Step1:
Import the necessary packages.

### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring image for dilation/erosion.

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step5:
Plot the images using plt.imshow.
 
## Program:
```
Developed by :G.Chethan Kumar
Register no: 212222240022
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```python
# Create the Text using cv2.putText
text_image = np.zeros((100,600),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX 
cv2.putText(text_image,"Chethan Kumar G",(5,70),font,2,(255),5,cv2.LINE_AA)
cv2.imshow("Chethan's Output",text_image)
```
```python
# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
```python
# Erode the image
image_erode = cv2.erode(text_image,kernel)
cv2.imshow("Erode image",image_erode)
```
```python
# Dilate the image
dilationImage=cv2.dilate(text_image,kernel)
cv2.imshow("Dilated Image",dilationImage)

```
## Output:

### Display the input Image

![Screenshot from 2023-10-10 14-44-16](https://github.com/Gchethankumar/EROSION-AND-DILATION/assets/118348224/07904a9a-551e-4d8e-8f7c-12d0bb00b1fa)


### Display the Eroded Image

![Screenshot from 2023-10-10 14-44-23](https://github.com/Gchethankumar/EROSION-AND-DILATION/assets/118348224/ec4fd673-6e0b-40f9-8944-211c43046dbf)


### Display the Dilated Image

![Screenshot from 2023-10-10 14-44-29](https://github.com/Gchethankumar/EROSION-AND-DILATION/assets/118348224/7c86d826-e15e-4157-a8b1-ab537116114b)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
