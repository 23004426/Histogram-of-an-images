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

# Developed By: Tirupathi Jayadeep
# Register Number: 212223240169
```python

### Gray Image and Color Image
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("rose.jpeg")
color_image = cv2.imread("flower.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

### Histogram of Grayscale Image
import cv2
import matplotlib.pyplot as plt
gray_img = cv2.imread('rose.jpeg')
color_img = cv2.imread('flower.jpg')
hist = cv2.calcHist([gray_img],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_img],[1],None,[256],[0,256])
plt.figure()
plt.imshow(gray_img)
plt.show()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

### Histogram of Color Image
import cv2
import matplotlib.pyplot as plt
gray_img = cv2.imread('rose.jpeg')
color_img = cv2.imread('flower.jpg')
hist = cv2.calcHist([gray_img],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_img],[1],None,[256],[0,256])
plt.figure()
plt.imshow(color_img)
plt.show()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()

### Histogram Equilization of GrayScale Image
import cv2
gray_img = cv2.imread('rose.jpeg',0)
gray_img = cv2.resize(gray_img,(300,200))
cv2.imshow('Grey Scale Image',gray_img)
equ = cv2.equalizeHist(gray_img)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)


```

## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/23004426/Histogram-of-an-images/assets/144979327/042c163f-9668-4892-bd70-6ae94d471dca)
![image](https://github.com/23004426/Histogram-of-an-images/assets/144979327/aa4c9c0d-a9e4-4389-a60d-94502d0f78af)


### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/23004426/Histogram-of-an-images/assets/144979327/a6bdc5c7-05af-4d17-9872-fd6a4d542eeb)
![image](https://github.com/23004426/Histogram-of-an-images/assets/144979327/e342f158-f131-4dc2-9c0d-6396d3968ccb)



###  Histogram of Color Image 
![image](https://github.com/23004426/Histogram-of-an-images/assets/144979327/b0bc1068-efbd-47d2-a2bb-c62111d443b8)
![image](https://github.com/23004426/Histogram-of-an-images/assets/144979327/5c9124b4-36bf-4020-a930-c186ef8d852a)

### Histogram Equalization of Grayscale Image.
![image](https://github.com/23004426/Histogram-of-an-images/assets/144979327/c6d2ed92-50ee-4c37-b810-ddeeadb848da)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
