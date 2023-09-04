# COLOR-CONVERSION
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
```
Developed By:MUKESH V
Register Number:212222230086
```
### i) Convert BGR and RGB to HSV and GRAY
```python
import cv2
houseImage = cv2.imread('images.jpg')
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
### ii)Convert HSV to RGB and BGR
```python
import cv2
houseHSVImage = cv2.imread('images.jpg')
cv2.imshow('MUKESH V(212222230086)',houseHSVImage)
RGBImage = cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2RGB)
cv2.imshow('BGR2HSV',RGBImage)
BGRImage=cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2BGR)
cv2.imshow('RGB2HSV',BGRImage)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### iii)Convert RGB and BGR to YCrCb
```python
import cv2
houseImage = cv2.imread('images.jpg')
cv2.imshow('Original HSV Image',houseImage)
YCrCb_image = cv2.cvtColor(houseImage, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR2HSV',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(houseImage, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB2HSV',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### iv)Split and Merge RGB Image
```python
import cv2
image = cv2.imread('images.jpg')
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.imshow('B=Channel',blue)
cv2.imshow('G=Channel',green)
cv2.imshow('R=Channel',red)
mergeBgr = cv2.merge((blue,green,red))
cv2.imshow('Merged-BGR-image',mergeBgr)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### v) Split and merge HSV Image
```python
import cv2
image = cv2.imread('images.jpg')
hsv = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue-Image',h)
cv2.imshow('Saturation-Image',s)
cv2.imshow('Gray-Image',v)
mergedHSV = cv2.merge((h,s,v))
cv2.imshow('Merged-HSV-Image',mergedHSV)
cv2.waitKey(0)
cv2.destroyAllWindow
```
## Output:
### i) BGR and RGB to HSV and GRAY
![image](https://github.com/MukeshVelmurugan/COLOR-CONVERSION/assets/118707363/8b988ee1-28a4-4cf5-be58-704d2af1081b)



### ii) HSV to RGB and BGR
![image](https://github.com/MukeshVelmurugan/COLOR-CONVERSION/assets/118707363/191a8278-a7cc-4632-9642-a93cd1b044c0)


### iii) RGB and BGR to YCrCb
![image](https://github.com/MukeshVelmurugan/COLOR-CONVERSION/assets/118707363/45bfa17b-7692-41d5-ab38-61a0cd0618b2)


### iv) Split and merge RGB Image
![image](https://github.com/MukeshVelmurugan/COLOR-CONVERSION/assets/118707363/4ec263ad-be37-4c4a-9b25-2aedc34c5f86)


### v) Split and merge HSV Image
![image](https://github.com/MukeshVelmurugan/COLOR-CONVERSION/assets/118707363/d30ff635-8702-4bea-991e-8da517ce39f2)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
