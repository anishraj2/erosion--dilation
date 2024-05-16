# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>


### Step2:
<br>Import the necessary pacakages



### Step3:
<br>Create the text using cv2.putText



### Step4:
<br>
Create the structuring element


### Step5:
<br>
Erode the image


 
## Program:

# Import the necessary packages
```
import io
import os
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img = np.zeros((100,400), dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,"REVERIE!",(5,70),font,2,(255,255,255),5,cv2.LINE_AA)
```



# Create the structuring element
```
kernel = np.ones((5,5), np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```


# Erode the image

```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode, cmap = 'gray')
plt.axis("off")
```


# Dilate the image

```

img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate, cmap = 'gray')
plt.axis("off")
```
## Output:

### Display the input Image


![Screenshot 2024-04-29 215525](https://github.com/Aravindsamy04/erosion--dilation/assets/113497037/eec5606d-bdb5-42c8-ab02-027ec9399141)


### Display the Eroded Image
![Screenshot 2024-04-29 215532](https://github.com/Aravindsamy04/erosion--dilation/assets/113497037/06085f42-74e2-4bb0-849a-b02929d84149)


### Display the Dilated Image

![Screenshot 2024-04-29 215541](https://github.com/Aravindsamy04/erosion--dilation/assets/113497037/218aee74-33bc-4c43-985c-511ccded7b0e)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
