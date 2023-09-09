# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

import cv2 and matplotlib.pyplot
<br>
### Step2:

Read and display the input images
<br>
### Step3:

Calculate the Histogram Values using calcHist()

<br>

### Step4:

Display the histograms
<br>

### Step5:

Calculate and display the equalized image using equalizeHist()
<br>

## Program:
```python
# Developed By: GURUMOORTHI R
# Register Number: 212222230042
```
```
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.

Gray_image = cv2.imread('diptgray.jpg')
Color_image = cv2.imread('dipt.jpg')
plt.imshow(Gray_image)
plt.show()
plt.imshow(Color_image)
plt.show()



# Display the histogram of gray scale image and any one channel histogram from color image

hist = cv2.calcHist([Gray_image], [0], None, [256], [0, 256])
hist1 = cv2.calcHist([Color_image], [1], None, [256], [0, 256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
plt.figure()
plt.title("Histogram")
plt.xlabel('color value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()




# Write the code to perform histogram equalization of the image. 

Gray_image = cv2.imread('diptgray.jpg',0)
equ=cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image', Gray_image)
cv2.imshow('Equalized Image', equ)
cv2.waitKey(0)
cv2.destroyAllWindows()





```
## Output:
### Input Grayscale Image and Color Image

![gray scale](https://github.com/gururamu08/HISTOGRAM/assets/118707009/eb080ad8-f65a-4e63-93b7-3adcadf18b14)

![color image](https://github.com/gururamu08/HISTOGRAM/assets/118707009/1744b6fa-c26f-442a-99e3-f32211f93798)





### Histogram of Grayscale Image and any channel of Color Image

![hist 1](https://github.com/gururamu08/HISTOGRAM/assets/118707009/d69ab1cf-4e63-4661-b61a-b84e46eef333)

![hist2](https://github.com/gururamu08/HISTOGRAM/assets/118707009/0d2c2474-d7ba-457f-865c-171e30f4af14)




### Histogram Equalization of Grayscale Image


![gray image](https://github.com/gururamu08/HISTOGRAM/assets/118707009/665eaf13-8293-42fb-b501-4136d5406df4)


![equalized image](https://github.com/gururamu08/HISTOGRAM/assets/118707009/9b546c55-5ec8-4830-9cab-a7677fe67742)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
