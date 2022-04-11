# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:

import opencv.
<br>

### Step2:

Read the original Image.
<br>

### Step3:

Store the required conversion of the image in a variable.
<br>

### Step4:

Show the image stored in the given variable.
<br>

### Step5:

Destroy all the windows and end the program.
<br>

## Program:
```python
# Developed By: D. Amarnath Reddy
# Register Number: 212221240012
# i) Convert BGR and RGB to HSV and GRAY

import cv2
house_color_image= cv2.imread('car.png')
cv2.imshow ('Original image', house_color_image)
hsv_image= cv2.cvtColor (house_color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV', hsv_image)
hsv_image1 = cv2.cvtColor (house_color_image, cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV', hsv_image1)
gray_image= cv2.cvtColor (house_color_image, cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY', gray_image)
gray_image1 = cv2.cvtColor (house_color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()

# ii)Convert HSV to RGB and BGR

import cv2
house_HSV_image= cv2.imread('car.png')
cv2.imshow('Original HSV image',house_HSV_image)
RGB_image = cv2.cvtColor(house_HSV_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV to RGB',RGB_image )
BGR_image = cv2.cvtColor(house_HSV_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV to BGR',BGR_image)
cv2.waitKey(0)
cv2.destroyAllwindows()

# iii)Convert RGB and BGR to YCrCb

import cv2
houseImage = cv2.imread('car.png')
cv2.imshow('Original HSV Image',houseImage)
YCrCb_image = cv2.cvtColor(houseImage, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR2HSV',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(houseImage, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB2HSV',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iv)Split and Merge RGB Image

import cv2
image = cv2.imread('car.png')
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
mergeBgr = cv2.merge((blue,green,red))
cv2.imshow('Merged BGR image',mergeBgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

# v) Split and merge HSV Image

import cv2
image = cv2.imread('car.png')
hsv = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue - Image',h)
cv2.imshow('Saturation - Image',s)
cv2.imshow('Gray - Image',v)
mergedHSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',mergedHSV)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### i) BGR and RGB to HSV and GRAY
<br>
<img width="1440" alt="1" src="https://user-images.githubusercontent.com/94165103/162772330-96a49207-80d1-4fb5-9807-c5beef77e0e2.png">
<br>

### ii) HSV to RGB and BGR
<br>
<img width="1440" alt="2" src="https://user-images.githubusercontent.com/94165103/162772364-7baa53a2-f71d-4d0c-942d-94d705d7f273.png">
<br>

### iii) RGB and BGR to YCrCb
<br>
<img width="1440" alt="3" src="https://user-images.githubusercontent.com/94165103/162772392-c9daccab-7d4d-4649-9f32-651d1af8758d.png">
<br>

### iv) Split and merge RGB Image
<br>
<img width="1440" alt="4" src="https://user-images.githubusercontent.com/94165103/162772438-74820c09-5d59-49ec-9472-0d2a141e4617.png">
<br>

### v) Split and merge HSV Image
<br>
<img width="1440" alt="5" src="https://user-images.githubusercontent.com/94165103/162772469-a3a1b2fa-4f2a-42a2-9140-6f0817ad89a2.png">
<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
