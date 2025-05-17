# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import required libraries (OpenCV, NumPy) and load the image in grayscale.
<br>


### Step2:
Define a structuring element (kernel) for morphological operations.
<br>

### Step3:
Apply erosion using cv2.erode() on the image with the defined kernel.
<br>

### Step4:
Apply dilation using cv2.dilate() on the image with the same kernel.
<br>

### Step5:
Display and compare the original, eroded, and dilated images.
<br>

 
## Program:

``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt


image = np.zeros((500, 500, 3), dtype=np.uint8)


font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'HARISH', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)


plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')


kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)

plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')

dilated_image = cv2.dilate(image, kernel, iterations=1)


plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Dilated Image")
plt.axis('off')



```
## Output:

### Display the input Image

![Screenshot 2025-05-17 141410](https://github.com/user-attachments/assets/05e75745-17ce-41d3-8e94-4ba3390c67ee)


### Display the Eroded Image

![Screenshot 2025-05-17 141509](https://github.com/user-attachments/assets/7c5ccc8a-7d34-4704-a30b-f77a4bfb98a3)



### Display the Dilated Image

![Screenshot 2025-05-17 141538](https://github.com/user-attachments/assets/0e9f2f60-10d6-4f23-9ecb-d0c0fbc20cef)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
