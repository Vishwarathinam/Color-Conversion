# Color Conversion

## AIM

To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required

Anaconda - Python 3.7.

## Algorithm

### Step1:

Import cv2 and save and image as filename.jpg.

### Step2:

Use imread(filename, flags) to read the file.

### Step3:

Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:

Split and merge the image using cv2.split and cv2.merge commands.

### Step5:

End the program and close the output image windows.


## Program

```python

# Developed By: Vishwa Rathinam .S
# Register Number: 212221240063

```

### i) Convert BGR and RGB to HSV and GRAY

```python
import cv2
sun_color_image = cv2.imread('panda.jpg')
cv2.imshow('Original image', sun_color_image)
hsv_image = cv2.cvtColor(sun_color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV' ,hsv_image )
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()
```

### ii)Convert HSV to RGB and BGR

```python
import cv2
sun_color_image = cv2.imread('panda.jpg')
cv2.imshow('Original image', sun_color_image)
hsv_image = cv2.cvtColor(sun_color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' ,hsv_image )
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()
```

### iii)Convert RGB and BGR to YCrCb

```python
import cv2
sun_color_image = cv2.imread('panda.jpg')
cv2.imshow('Original image', sun_color_image)
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb', gray_image1)
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()
```

### iv)Split and Merge RGB Image

```python
import cv2
image = cv2.imread('panda.jpg')
blue=image[:,:,0]
green=image[:,:,1]
red=image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
Merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',Merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()
```

### v) Split and merge HSV Image

```python
import cv2
image = cv2.imread('panda.jpg')
hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue-Image',h)
cv2.imshow('Saturation-Image',s)
cv2.imshow('Gray-Image',v)
Merged_HSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()
```


## Output:

### i) BGR and RGB to HSV and GRAY


![img1](https://user-images.githubusercontent.com/95266350/227995267-0c76007b-04a3-4804-bf1e-d9faf8eeab03.png)


### ii) HSV to RGB and BGR


![img2](https://user-images.githubusercontent.com/95266350/227995297-7da3d3a3-d7e9-430c-8e8b-7ee46475f0ca.png)


### iii) RGB and BGR to YCrCb


![img3](https://user-images.githubusercontent.com/95266350/227995312-4a1b4732-04e0-4ead-ba1c-d5351facfe3c.png)


### iv) Split and merge RGB Image

![img4](https://user-images.githubusercontent.com/95266350/227995333-47f09f4c-344f-40ed-9af8-b9e1d5c80141.png)



### v) Split and merge HSV Image

![img5](https://user-images.githubusercontent.com/95266350/227995354-c59b64b4-d1a4-4922-9f4d-76a2a45dbee4.png)




## Result:

Thus the color conversion was performed between RGB, HSV and YCbCr color models.


