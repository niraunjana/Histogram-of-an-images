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
```
# Developed By: NIRAUNJANA GAYATHRI G R
# Register Number: 212222230096
```
## Colour and Gray Image

```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("grayflower.jpg")
color_image = cv2.imread("colourflower.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Histogram of Grayscale Image
```

import numpy as np
import cv2
Gray_image = cv2.imread("grayflower.jpg")
Color_image = cv2.imread("colourflower.jpg")
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
```
## Histogram of Green channel of colour Image
```

plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
## Histogram Equalization of Grayscale Image
```

import cv2
gray_image = cv2.imread("colourflower.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image

![WhatsApp Image 2024-03-15 at 11 59 31_60ac8b17](https://github.com/niraunjana/Histogram-of-an-images/assets/119395610/0a1f002c-88e4-42b2-a582-1726edfb8490)



### Histogram of Grayscale Image 

![image](https://github.com/niraunjana/Histogram-of-an-images/assets/119395610/b03cb2b5-3c60-4862-86cf-1d3f3813a42b)

![image](https://github.com/niraunjana/Histogram-of-an-images/assets/119395610/051681dd-e712-4d83-bc57-2133996d7d7c)


### Histogram of Green channel of Color Image

![image](https://github.com/niraunjana/Histogram-of-an-images/assets/119395610/fc675546-f806-4a48-87e9-7a7622248fd3)

![image](https://github.com/niraunjana/Histogram-of-an-images/assets/119395610/9cb203eb-1758-47d1-b9d9-03b373f208ec)

### Histogram Equalization of Grayscale Image.

![WhatsApp Image 2024-03-17 at 12 46 55_fcf84378](https://github.com/niraunjana/Histogram-of-an-images/assets/119395610/3b7e1ad0-9248-4ccc-82e7-b994e3f0e51e)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
