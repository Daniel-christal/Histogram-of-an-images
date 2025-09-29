# Histogram-of-an-images
# Developed By:DANIEL C
# Reg no:212223240023
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: Daniel C
# Register Number:212223240023
# Input Grayscale Image and Color Image:

import cv2
import matplotlib.pyplot as plt
Gray_image = cv2.imread('tree.jpg')
Color_image = cv2.imread('york.jpg')
plt.imshow(Gray_image)
plt.show()
plt.imshow(Color_image)
plt.show() 

# Histogram of Grayscale Image and Green channel of Color Image:
hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
hist1 = cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
plt.figure()
plt.title("Histogram of Color Image Green Channel")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()

# Histogram Equalization of Grayscale Image:
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)



```
## Output:
### Input Grayscale Image and Color Image
<img width="532" height="522" alt="image" src="https://github.com/user-attachments/assets/ce9e6dbf-320c-427e-8065-3205e2fff995" />

<img width="687" height="457" alt="image" src="https://github.com/user-attachments/assets/2ed0a72e-d257-4c99-8c4e-d0230453ee2e" />


### Histogram of Grayscale Image and any channel of Color Image

<img width="738" height="548" alt="image" src="https://github.com/user-attachments/assets/c21a1b66-d853-4497-81d2-66cca07be8c3" />

<img width="746" height="580" alt="image" src="https://github.com/user-attachments/assets/54e6534e-ac83-4fa2-b7e1-85965bc72463" />

### Histogram Equalization of Grayscale Image.

<img width="923" height="813" alt="image" src="https://github.com/user-attachments/assets/63104174-3aee-49c2-ae98-a0eb7099c226" />



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
