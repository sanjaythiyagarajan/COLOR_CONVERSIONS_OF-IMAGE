# COLOR_CONVERSIONS_OF-IMAGE

## AIM


#### To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv) To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:

### Anaconda - Python 3.7

## Algorithm:


### Step 1

Choose an image and save it as a filename.jpg 

### Step 2

Use imread(filename, flags) to read the file.


### Step 3

Use imshow(window_name, image) to display the image.

### Step 4

Use imwrite(filename, image) to write the image.

### Step 5

End the program and close the output image windows.


### Step 6

Convert BGR and RGB to HSV and GRAY

### Step 7

Convert HSV to RGB and BGR

### Step 8

Convert RGB and BGR to YCrCb

### Step 9

Split and Merge RGB Image


### Step 10

Split and merge HSV Image

 python
 
Developed By: SANJAY T

Register Number: 212222110039


#### IMAGE 

![digital](https://github.com/sanjaythiyagarajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119409242/b92c5a68-6e92-4024-a4c0-c2faf29ea7cf)


## Program:


### (i) Read and display the image
 ```py
#Read and display the image
import cv2
image=cv2.imread('digital.jpg',1)
image=cv2.resize(image,(200,325))
cv2.imshow('sanjay',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### Output:

![image](https://github.com/sanjaythiyagarajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119409242/3ea47514-8e07-4183-8bbd-8efd69caf3d1)


## Program:

### (ii) Write the image
```
py
#Write the image
import cv2
image=cv2.imread('digital.jpg',0)
cv2.imwrite('demos.jpg',image)

```
### Output

![image](https://github.com/sanjaythiyagarajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119409242/86be2335-322c-4308-b965-188250e5e90b)


## Program:

### (iii) Shape of the Image

py
#Shape of the Image
import cv2
image=cv2.imread('digital.jpg',1)
print(image.shape)



### Output

![image](https://github.com/sanjaythiyagarajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119409242/732690aa-12df-437e-83ac-ffa7d1e7e5bf)



## Program:

### (iv) Access rows and columns
```
py
#Access rows and columns
import random
import cv2
image=cv2.imread('digital.jpg',1)
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                    random.randint(0,255),
                    random.randint(0,255)] 
cv2.imshow('part image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

### Output

![image](https://github.com/sanjaythiyagarajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119409242/23d29911-6889-44dd-9c81-79076d0484f1)



## Program:

### (v) Cut and paste portion of image
```
py
#Cut and paste portion of image
import cv2
image=cv2.imread('digital.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[150:200,110:160]
image[110:160,150:200] = tag
cv2.imshow('partimage1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
### Output

![image](https://github.com/sanjaythiyagarajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119409242/2d377035-0be4-44ad-bfc5-628dc08213ba)


## Program:

### (vi) BGR and RGB to HSV and GRAY
```
py
#BGR and RGB to HSV and GRAY
import cv2
img = cv2.imread('digital.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)

hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)

gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)

gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Original Image

![image](https://github.com/sanjaythiyagarajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119409242/d246a88c-70a5-4cd9-8b68-34ce7149828b)


### Output

![image](https://github.com/sanjaythiyagarajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119409242/00fa1be4-e13b-4a1b-9ef0-0a0b9f4c9916)


## Program:

### (vii) HSV to RGB and BGR
```
py
#HSV to RGB and BGR
import cv2
img = cv2.imread('digital.jpg')
img = cv2.resize(img,(300,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Original HSV

![image](https://github.com/sanjaythiyagarajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119409242/5ca29390-90f3-4746-8610-5eb1af5a69f5)


### Output


![image](https://github.com/sanjaythiyagarajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119409242/63ea7eeb-39e6-4f63-823e-a82abeb95360)


## Program:

### (viii) RGB and BGR to YCrCb
```py

#RGB and BGR to YCrCb
import cv2
img = cv2.imread('digital.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()

```
### Output


![image](https://github.com/sanjaythiyagarajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119409242/125c6533-a68e-4578-b8d4-4d1e3da84c2f)


## Program:

### (ix) Split and merge RGB Image
```py
#Split and merge RGB Image
import cv2
img = cv2.imread('digital.jpg',1)
img = cv2.resize(img,(300,200))

R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output

#### Channels

![image](https://github.com/sanjaythiyagarajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119409242/9bd148ff-0c65-434a-b09f-5c0be459ca75)


#### Merged RGB

![image](https://github.com/sanjaythiyagarajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119409242/f1b8bc12-5325-4425-a8e9-e4c0456a6d6a)


## Program:

### (x) Split and merge HSV Image
```py
#Split and merge HSV Image
import cv2
img = cv2.imread("digital.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()

```
### Output

### Merged HSV

![image](https://github.com/sanjaythiyagarajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119409242/f57064cd-1984-4046-96ed-7d6e8c4ee4e5)




### Splitted

![image](https://github.com/sanjaythiyagarajan/COLOR_CONVERSIONS_OF-IMAGE/assets/119409242/57872d5d-6723-4860-8c3d-e70384c176bf)



## Result:
#### Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.
