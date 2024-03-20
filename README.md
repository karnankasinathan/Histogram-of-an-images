# Histogram-of-an-images
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
# Developed By: Karnan K
# Register Number: 212222230062
```
## Output:
### Input Grayscale Image and Color Image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("i1")
color_image = cv2.imread("i3",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Histogram of Grayscale Image and any channel of Color Image
```
import numpy as np
import cv2
Gray_image = cv2.imread("i1")
Color_image = cv2.imread("i3")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
### Histogram Equalization of Grayscale Image.
```
import cv2
gray_image = cv2.imread("i1",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Input Grayscale Image and Color Image
<img src="https://github.com/SriramS22/Histogram-of-an-images/assets/119094390/3a270119-bcd5-47a5-8463-3e6cca2c25a1" width=450 height=450>

<img src="https://github.com/SriramS22/Histogram-of-an-images/assets/119094390/79b003ca-818e-4c33-acf4-97fa65f6b826" width=450 height=450>

### Histogram of Grayscale Image and any channel of Color Image

<img src="https://github.com/SriramS22/Histogram-of-an-images/assets/119094390/1e2cc124-3ff6-46c9-8351-80af53aa3b47" width=450 height=450>

<img src="https://github.com/SriramS22/Histogram-of-an-images/assets/119094390/4149fade-d963-499a-86fc-afe1c61352b7" width=450 height=450>

<img src="https://github.com/SriramS22/Histogram-of-an-images/assets/119094390/283beae4-da4e-45af-8a86-4f926f20c6f5" width=450 height=450>

<img src="https://github.com/SriramS22/Histogram-of-an-images/assets/119094390/41a8b9da-6e55-4f99-abc0-608512a8ebed" width=450 height=450>

### Histogram Equalization of Grayscale Image.
<img src="https://github.com/SriramS22/Histogram-of-an-images/assets/119094390/221a29d2-2066-43ca-9e73-edad600ae515" width=450 height=450>

<img src="https://github.com/SriramS22/Histogram-of-an-images/assets/119094390/40ed9b0d-18a6-4eff-8fad-cd82c45b6de0" width=450 height=450>


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
