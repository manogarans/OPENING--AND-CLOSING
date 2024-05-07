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
Give the input text using cv2.putText()
### Step3: 
Perform opening operation and display the result
### Step4 
Similarly, perform closing operation and display the result
## Program:
### Developed By : MANOGARAN S
### Reg No : 212223240081
# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Datascientist',(5,70), font,2,(255),5,cv2.LINE_AA)
```
# Create the structuring element
```
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```

# Use Opening operation
```
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```


# Use Closing Operation
```
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```


## Output:

### Display the input Image
![Screenshot 2024-05-07 195452](https://github.com/manogarans/OPENING--AND-CLOSING/assets/139331782/bda90f79-1efc-439f-8cd1-4db6d8f687da)

### Display the result of Opening
![Screenshot 2024-05-07 195502](https://github.com/manogarans/OPENING--AND-CLOSING/assets/139331782/8c9507b3-14ef-4d77-b257-242f87ae6586)


### Display the result of Closing
![Screenshot 2024-05-07 195509](https://github.com/manogarans/OPENING--AND-CLOSING/assets/139331782/e0846745-cc54-41ee-91de-f82de4915594)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
