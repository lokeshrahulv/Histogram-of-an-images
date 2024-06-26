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
Developed By: Lokesh Rahul V V
Register Number: 212222100024
```
## Input Grayscale Image and Color Image :
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("flower.jpg")
color_image = cv2.imread("sphere.jpg")
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Color Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
````
## Histogram of Grayscale Image and any channel of Color Image :
```python
import numpy as np
import cv2
Gray_image = cv2.imread("flower.jpg")
Color_image = cv2.imread("sphere.jpg")
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
## Histogram Equalization of Grayscale Image :
```python
import cv2
gray_image = cv2.imread("flower.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-03-20 233924](https://github.com/lokeshrahulv/Histogram-of-an-images/assets/118423842/42135ae9-dd30-4c02-931b-a18256e7d6fe)
![Screenshot 2024-03-20 233742](https://github.com/lokeshrahulv/Histogram-of-an-images/assets/118423842/28f4bbcc-ca08-456a-93aa-8960aa1577e8)

### Histogram of Grayscale Image and any channel of Color Image
### Gray Scale:
![fg](https://github.com/lokeshrahulv/Histogram-of-an-images/assets/118423842/bece7bc8-b262-4aa6-877b-f0510dfb1a8f)
![,,](https://github.com/lokeshrahulv/Histogram-of-an-images/assets/118423842/21a288d4-631c-43b0-b8c9-91bbd9280c52)

### Color Image:
![yyh](https://github.com/lokeshrahulv/Histogram-of-an-images/assets/118423842/84d0e683-6631-4548-aa85-2e5a8252745f)
![kk](https://github.com/lokeshrahulv/Histogram-of-an-images/assets/118423842/0c54a330-3e57-4150-9792-6babfae179b4)

### Histogram Equalization of Grayscale Image.
![Screenshot 2024-03-20 234034](https://github.com/lokeshrahulv/Histogram-of-an-images/assets/118423842/0fcbf977-ef54-40be-863f-8569f6f4c2b0)
![Screenshot 2024-03-20 234026](https://github.com/lokeshrahulv/Histogram-of-an-images/assets/118423842/4a3c0ff2-5f52-49ec-9662-9f3382ead309)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
