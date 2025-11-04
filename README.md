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
from google.colab import files
import cv2
import numpy as np
import matplotlib.pyplot as plt

# 🔹 Step 1: Upload the image
uploaded = files.upload()

# 🔹 Step 2: Automatically get the uploaded filename
filename = next(iter(uploaded))
print("✅ Uploaded file:", filename)

# 🔹 Step 3: Read and process the image
image = cv2.imread(filename)

# Convert to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Calculate histogram of original grayscale image
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)

# Calculate histogram of equalized image
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])

# 🔹 Step 4: Plot results
plt.figure(figsize=(10, 7))

plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image\n Name: Daniel C    Reg no: 212223240023')
plt.axis('off')

plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

plt.subplot(2, 2, 3)
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

plt.subplot(2, 2, 4)
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

plt.tight_layout()
plt.show()



```
## Output:
### Original Gray scale Image:
<img width="556" height="421" alt="image" src="https://github.com/user-attachments/assets/f20b5157-64b1-4271-adbb-50b326c49b1e" />

## Equalized Image:
<img width="549" height="409" alt="image" src="https://github.com/user-attachments/assets/f6a1302c-6ee6-4ea4-9548-fe823bac073c" />


### Histogram of Grayscale Image:
<img width="651" height="432" alt="image" src="https://github.com/user-attachments/assets/7775005d-872f-4cff-9a8f-56fce5315794" />


### Histogram Equalization of Grayscale Image.

<img width="643" height="427" alt="image" src="https://github.com/user-attachments/assets/fbf30804-556c-499f-b398-caf8093ae4ef" />



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
