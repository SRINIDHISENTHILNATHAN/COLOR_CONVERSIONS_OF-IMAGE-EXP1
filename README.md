# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
1.  Draw a line from the top-left to the bottom-right of the image.

2.	Draw a circle at the center of the image.

3.	Draw a rectangle around a specific region of interest in the image.

4.	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
1.	Convert the image from RGB to HSV and display it.
2.	Convert the image from RGB to GRAY and display it.
3.	Convert the image from RGB to YCrCb and display it.
4.	Convert the HSV image back to RGB and display it.

### Step4:
1.	Access and print the value of the pixel at coordinates (100, 100).
2.	Modify the color of the pixel at (200, 200) to white.

### Step5:
Resize the original image to half its size and display it.
### Step6:
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
1.	Flip the original image horizontally and display it.
2.	Flip the original image vertically and display it.

### Step8:
Save the final modified image to your local directory.


## Program:
### Developed By: SRINIDHI SENTHIL
### Register Number: 212222230148


## Output:

### 1. Read and display the image
i.Load an image from your local directory and display it.
```
!pip install opencv-python
!pip install matplotlib
import cv2
import matplotlib.pyplot as plt
img=cv2.imread('exp1.png')
cv2.imshow('Image Window', img)
plt.imshow(img)
plt.axis('off')
plt.show()

```
![image](https://github.com/user-attachments/assets/e888e1d2-ea57-47dd-8ab4-c8e09ccdbc99)

### Draw Shapes and Add Text
(1) Draw a line from the top-left to the bottom-right of the image.
```
import cv2
image = cv2.imread('exp1.png')
res = cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (255,0,0), 10)
cv2.imshow('LINWINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
![image](https://github.com/user-attachments/assets/e26f8a91-3d18-4f65-a1bb-17ee911adf3f)


2. Draw a circle at the center of the image.
```
import cv2
image = cv2.imread('exp1.png')
height, width, _ = image.shape
line=cv2.line(img,(0,0),(736,414),(0,0,255),10)
cv2.imshow('CIRCLEWINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/566c6c6b-de85-4220-b2f6-9b79cc826b38)

3.Draw a rectangle around a specific region of interest in the image.
```
import cv2
image = cv2.imread("naturek.jpg")
start = (150, 100)
stop = (300, 200)
color = (255, 255, 100)
thickness = 10           
res_img = cv2.rectangle(image, start, stop, color, thickness)
cv2.imshow('WINDOW', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/784b4637-8016-41e3-86bc-f60a1ddd5440)



4.Add the text "OpenCV Drawing" at the top-left corner of the image.
```
import cv2
image = cv2.imread("exp1.png")
text = "OPENCV DRAWING"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255) 
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color, thickness)
cv2.imshow('TEXTWINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/8b67f116-8fa2-40fc-b843-5eedf72d1485)


### iii)Image Color Conversion
(i)Convert the image from RGB to HSV and display it
```
import cv2
image = cv2.imread('exp1.png',1)
cv2.imshow('ORIGINAL IMAGE',image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/531c6977-23c0-4b21-8e47-63b288ccde92)



(2) Convert the image from RGB to GRAY and display it.

```
import cv2
image = cv2.imread('exp1.png',1)
cv2.imshow('ORIGINAL IMAGE',image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![image](https://github.com/user-attachments/assets/bf7123b8-5a34-4de5-a5a0-715bf3ad9494)



(3) Convert the image from RGB to YCrCb and display it.
```import cv2
image = cv2.imread('exp1.png',1)
cv2.imshow('ORIGINAL IMAGE',image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/23dec97e-d27b-4fef-9b48-f5844f265731)


(4) Convert the HSV image back to RGB and display it.
```
import cv2
image = cv2.imread('exp1.png',1)
cv2.imshow('ORIGINAL IMAGE',image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',RGB)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/f890e799-7128-46f7-9940-19e8dbc82091)


### iv)Access and Manipulate Image Pixels
(1) Access and print the value of the pixel at coordinates (100, 100)
```
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```
![image](https://github.com/user-attachments/assets/c6e95952-6b38-400b-b1ab-3a4827c44360)

(2) Modify the color of the pixel at (200, 200) to white
```
import cv2
image = cv2.imread('exp1.png',1)
cv2.imshow('ORIGINAL IMAGE',image)
image[200, 200] = [255, 255, 255] 
cv2.imshow('MODIFIED IMAGE', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/bfd454d3-d7ad-4abe-b3ca-1a8f76c4c242)

### v)Image Resizing:
Resize the original image to half its size and display it.
```
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (350,200))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/1d5f7477-7d3a-45bd-aa7a-3459824109ec)

### vi)Image Cropping
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```
import cv2
image = cv2.imread('exp1.png',1)
image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/440b3022-4b94-4ef7-ab26-55e1c12b4c55)

### vii)Image Flipping:
(1) Flip the original image horizontally and display it.
```
import cv2
image = cv2.imread("naturek.jpg")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_180)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/567b6c86-382d-4bef-b871-d7fc4c0b2af4)


(2) Flip the original image vertically and display it.
```
import cv2
image = cv2.imread('exp1.png')
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/da6fbefa-2ff0-4f5b-9007-8b674484f342)



### viii)Write and Save the Modified Image
Save the final modified image to your local directory.
```
import cv2
img = cv2.imread('exp1.png')
img = cv2.resize(img,(300,200))
cv2.imwrite('nature_pic.jpg',img)
```
![image](https://github.com/user-attachments/assets/0c3fa123-2c60-4789-9c11-4f2f50387486)


## Result:

Thus the images are read, displayed, and written ,and color conversion was performed successfully using the python program.

