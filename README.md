# OPENING--AND-CLOSING

## Aim:
To implement Opening and Closing using Python and OpenCV.

## Software Required:
1. Anaconda - Python 3.7
2. OpenCV
   
## Algorithm:
### Step1:
Import the necessary packages
### Step2:
Give the input text using cv2.putText()
### Step3:
Perform opening operation and display the result
### Step4:
Similarly, perform closing operation and display the result

 
## Program:
```
NAME : Rhudhra phriyamvadha K S
REG NO : 212224040275
```

``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Hemavathy S', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')

# Closing is dilation followed by erosion
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
```
## Output:

### Display the input Image
<img width="581" height="516" alt="image" src="https://github.com/user-attachments/assets/b0e48920-8251-4946-88e1-a5c9a63b5ce4" />

### Display the result of Opening
<img width="533" height="517" alt="image" src="https://github.com/user-attachments/assets/002bd4a5-6ef5-4ed6-acc5-17ad6fcca002" />

### Display the result of Closing
<img width="582" height="522" alt="image" src="https://github.com/user-attachments/assets/2b8d48bb-f726-4c34-990e-414b682270d8" />

## Result:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
