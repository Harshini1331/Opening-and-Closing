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
Create the text image using cv2.putText.

### Step 3:
Then create the structuring element for opening and closing.

### Step 4:
Apply erosion and dilation using cv2.MORPH_OPEN and cv2.MORPH_CLOSE.

### Step 5:
Plot the images using plt.imshow.

## Program:

``` Python
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"Harshini",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')

# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))

# Use Opening operation

image1=cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(image1,'magma')
plt.axis('off')


# Use Closing Operation

image2=cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(image2,'magma')
plt.axis('off')

```
## Output:

### Display the input Image
<img width="281" alt="image" src="https://user-images.githubusercontent.com/75235554/170839938-c1e902b9-a476-4087-8ed4-1f6e4e9b2b8b.png">

### Display the result of Opening
<img width="277" alt="image" src="https://user-images.githubusercontent.com/75235554/170839942-39698bd3-e8d9-40eb-9ed5-7d57bb52cca5.png">

### Display the result of Closing
<img width="283" alt="image" src="https://user-images.githubusercontent.com/75235554/170839947-a9bf6141-7b63-4af0-809f-979d6de7b8db.png">

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
