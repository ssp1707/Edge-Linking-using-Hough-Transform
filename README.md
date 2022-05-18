# Edge-Linking-using-Hough-Transform
## Aim:
To write a Python program to detect the lines using Hough Transform.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale.

### Step4:
Using Canny operator from cv2,detect the edges of the image.

### Step5:
Using the HoughLinesP(),detect line co-ordinates for every points in the images.Using For loop,draw the lines on the found co-ordinates.Display the image.


## Program:
```Python
Developed by: S. Sanjna Priya
Registeration Number : 212220230043
```

# Read image and convert it to grayscale image
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread ('lin.jpg') 
gray_image = cv2.cvtColor(image1,cv2.COLOR_BGR2GRAY)
cv2.imshow('GRAY IMAGE',gray_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

# Find the edges in the image using canny detector and display
```
edges1 = cv2.Canny(gray_image, 120, 150)
plt.imshow(edges1,cmap='gray')
plt.title('canny_edges')
plt.show()
```

# Detect points that form a line using HoughLinesP
```
lines=cv2.HoughLinesP(edges1,1,np.pi/180,threshold=70,minLineLength=50,maxLineGap=50)
```

# Draw lines on the image
```

```

# Display the result
```

```
## Output

### Input image and grayscale image



### Canny Edge detector output



### Display the result of Hough transform



## Result:
Thus the program is written with python and OpenCV to detect lines using Hough transform. 
