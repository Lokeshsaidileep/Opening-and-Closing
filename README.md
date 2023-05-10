# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:
Import the necessary packages.

### Step 2:
Create the Text using cv2.putText.

### Step 3:
Create the structuring element.

### Step 4:
Use Opening operation.

### Step 5:
Use Closing Operation.

### Step 6:
Print the output and end the program.

PROGRAM:
~~~
/*
Developed by   : S.LOKESH SAI DILEEP
Register Number: 212221230111
*/
~~~
~~~
# Import the necessary packages

# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'LOKESH',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation
image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()

# Use Closing Operation
image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()
~~~
## Output:

### Display the input Image
![image](https://github.com/Lokeshsaidileep/Opening-and-Closing/assets/94883079/bbe368c5-4659-4d4f-8dc8-43151c08edb0)

### Display the result of Opening
![image](https://github.com/Lokeshsaidileep/Opening-and-Closing/assets/94883079/c59353a1-682c-450f-92bf-38428f31acd5)

### Display the result of Closing
![image](https://github.com/Lokeshsaidileep/Opening-and-Closing/assets/94883079/e62a1d8f-f40a-4b33-9296-10ce7a6be2ef)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
