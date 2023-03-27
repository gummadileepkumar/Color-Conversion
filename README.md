# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 library and upload the image or capture an image.

### Step2:
Read the saved image using cv2.imread("filename.jpg").

### Step3:
Convert the image into the given color transformation using cv2.cvtColor(image, cv2.BGR2YCrCb) and similarly for other color formats.

### Step4:
Split and merge the image using cv2.split(hsv) and cv2.merge([h,s,v]).

### Step5:
Output the image using cv2.imshow("OUTPUT", image).

## Program:
```python
# Developed By:Gumma Dileep Kumar
# Register Number:212222240032
```
# i) Convert BGR and RGB to HSV and GRAY
```python
import cv2
houseImage = cv2.imread('royal.jpeg')
cv2.imshow('Original Image',houseImage)
hsvImage = cv2.cvtColor(houseImage,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsvImage)
hsvImage1=cv2.cvtColor(houseImage,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsvImage1)
grayImage = cv2.cvtColor(houseImage,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',grayImage)
grayImage1 = cv2.cvtColor(houseImage,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',grayImage1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```



# ii)Convert HSV to RGB and BGR
```python
import cv2
houseHSVImage = cv2.imread('royal.jpeg')
cv2.imshow('Original HSV Image',houseHSVImage)
RGBImage = cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2RGB)
cv2.imshow('BGR2HSV',RGBImage)
BGRImage=cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2BGR)
cv2.imshow('RGB2HSV',BGRImage)
cv2.waitKey(0)
cv2.destroyAllWindows()
```




# iii)Convert RGB and BGR to YCrCb
```python
import cv2
houseImage = cv2.imread('royal.jpeg')
cv2.imshow('Original HSV Image',houseImage)
YCrCb_image = cv2.cvtColor(houseImage, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR2HSV',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(houseImage, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB2HSV',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```




# iv)Split and Merge RGB Image
```python
import cv2
image = cv2.imread('royal.jpeg')
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
```




# v) Split and merge HSV Image
```python
import cv2
image = cv2.imread('royal.jpeg')
hsv = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue - Image',h)
cv2.imshow('Saturation - Image',s)
cv2.imshow('Gray - Image',v)
mergedHSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',mergedHSV)
cv2.waitKey(0)
cv2.destroyAllWindow




```
## Output:
### i) BGR and RGB to HSV and GRAY
![3 1Image](https://user-images.githubusercontent.com/118707761/228017167-a40187fd-5cb3-4a83-a538-b36b7e990023.jpg)


### ii) HSV to RGB and BGR
![3 2Image](https://user-images.githubusercontent.com/118707761/228017250-f2f88dc4-04a7-40be-8a76-2f83dc2846ed.jpg)


### iii) RGB and BGR to YCrCb
![3 3image](https://user-images.githubusercontent.com/118707761/228017300-d5f62215-174b-4724-86a3-0e69e79a0db9.jpg)


### iv) Split and merge RGB Image
![3 4image](https://user-images.githubusercontent.com/118707761/228017573-478267d4-bd92-453d-b13e-149f0c962bd9.jpg)


### v) Split and merge HSV Image
![3 5image](https://user-images.githubusercontent.com/118707761/228017629-d2c0d25d-0c5b-442a-8ae6-bc9487016c1a.jpg)



## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
