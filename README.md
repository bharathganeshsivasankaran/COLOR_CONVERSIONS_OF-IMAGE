# EX01 COLOR_CONVERSIONS_OF-IMAGE
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
### Developed By: Bharathganesh S
### Register Number: 212222230022


## Output:

### 1. Read and display the image
i.Load an image from your local directory and display it.
```
import cv2
image=cv2.imread('naturek.jpg',1)
cv2.imshow('NATUREK',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![363556469-520ea58c-0186-456d-9b9e-9e23c56bfb46](https://github.com/user-attachments/assets/b10079c0-dcb4-4301-ada7-3dcd6061c6f5)


### Draw Shapes and Add Text
(1) Draw a line from the top-left to the bottom-right of the image.
```
import cv2
image = cv2.imread("naturek.jpg")
res = cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (255,0,0), 10)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![365507700-3f281a31-8d3f-4e96-959b-b373d9001383](https://github.com/user-attachments/assets/009a7c45-e255-45ec-917e-e1b26306c463)


2. Draw a circle at the center of the image.
```
import cv2
image = cv2.imread("naturek.jpg")
height, width, _ = image.shape
center_coordinates = (width // 2, height // 2)
res = cv2.circle(image, center_coordinates, 120, (0, 255, 0), 10)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![365509117-bcbd9b85-cf3f-4feb-9cfa-24790dd1814c](https://github.com/user-attachments/assets/6a4021bf-4f64-4913-9c48-6dfad34479e9)


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
![365507022-add75b55-2ff3-446f-b7f0-f700b0ebb734](https://github.com/user-attachments/assets/1e61433b-1d2c-4348-9073-4fe14e9aca29)



4.Add the text "OpenCV Drawing" at the top-left corner of the image.
```
import cv2
image = cv2.imread("naturek.jpg")
text = "OpenCV Drawing"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255) 
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![365507032-95c05efb-5590-4d91-9462-8c1c44689927](https://github.com/user-attachments/assets/0afa4f3d-d365-447a-b230-108b260992ab)


### iii)Image Color Conversion
(i)Convert the image from RGB to HSV and display it
```
import cv2
image = cv2.imread('naturek.jpg',1)
cv2.imshow('ORIGINAL IMAGE',image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![365507069-1cf5b4fa-78bf-4f94-941d-5b2fb7748dd4](https://github.com/user-attachments/assets/182169e9-fca6-4bba-8ddd-9e702efa48ab)


(2) Convert the image from RGB to GRAY and display it.

```
import cv2
image = cv2.imread('naturek.jpg',1)
cv2.imshow('ORIGINAL IMAGE',image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![365507090-c2360004-6330-4114-bba8-fd8c4aac14fc](https://github.com/user-attachments/assets/6e717a91-0042-4099-a5e3-00b12954de29)


(3) Convert the image from RGB to YCrCb and display it.
```
import cv2
image = cv2.imread('naturek.jpg',1)
cv2.imshow('ORIGINAL IMAGE',image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![365507853-f519b75b-8777-4709-aef0-237cf690b5e6](https://github.com/user-attachments/assets/77c9e0fe-46c7-4180-91ea-07d1fb76d0da)


(4) Convert the HSV image back to RGB and display it.
```
import cv2
image = cv2.imread('naturek.jpg',1)
cv2.imshow('ORIGINAL IMAGE',image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',RGB)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![365507905-6e818c27-966e-46e0-a1b3-52887d8010ef](https://github.com/user-attachments/assets/d9b17484-4bf4-4bcc-949b-bb4087e671a8)


### iv)Access and Manipulate Image Pixels
(1) Access and print the value of the pixel at coordinates (100, 100)
```
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```
![365507960-53fb2f1a-8e20-4b3b-bdeb-cf314f0326fd](https://github.com/user-attachments/assets/ff8b8df7-0119-4196-93fa-cabaa5bb065a)


(2) Modify the color of the pixel at (200, 200) to white
```
import cv2
image = cv2.imread('naturek.jpg',1)
cv2.imshow('ORIGINAL IMAGE',image)
image[200, 200] = [255, 255, 255] 
cv2.imshow('MODIFIED IMAGE', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![365508857-da0721e2-3301-43c2-9f66-e6974f3a4698](https://github.com/user-attachments/assets/1579420a-1a28-4fb3-8b10-9e9b93f60f16)


### v)Image Resizing:
Resize the original image to half its size and display it.
```
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![365508068-60fbc978-3772-4249-9148-9c5486c4599e](https://github.com/user-attachments/assets/5ac2bff9-c0ff-408f-ab5b-66302a286dbd)

![365508117-3ed7632c-9359-45e6-9aef-3fce7858cc4e](https://github.com/user-attachments/assets/6d3cd60f-72ec-4059-899b-5d6dc5aa88c4)

### vi)Image Cropping
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```
import cv2
image = cv2.imread('naturek.jpg',1)
image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![365508158-6a1d03bb-0c93-4207-941b-96ea80360a07](https://github.com/user-attachments/assets/bd43cf6e-23f1-43e8-95de-d4d5c5340972)

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
![365509345-747a0eff-266f-494d-862c-be8548fd88d8](https://github.com/user-attachments/assets/62dc5940-abab-41d9-bcef-f06b75bc827e)


(2) Flip the original image vertically and display it.
```
import cv2
image = cv2.imread("naturek.jpg")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![365507248-f4d998f1-00a1-4fc5-90e1-918d8c793018](https://github.com/user-attachments/assets/d9dad515-42b4-4f81-ba73-4bcd27c31785)

![365507266-fa353d26-4e1d-4117-8fa6-045c6cd24447](https://github.com/user-attachments/assets/5d984e31-7c85-4f2f-8ceb-5334b049ace6)

### viii)Write and Save the Modified Image
Save the final modified image to your local directory.
```
import cv2
img = cv2.imread("naturek.jpg")
img = cv2.resize(img,(300,200))
cv2.imwrite('nature_pic.jpg',img)
```
![365507222-874121bf-a1c9-4fb9-be27-e4613309ad2d](https://github.com/user-attachments/assets/46e9617a-1b08-499c-bd72-04097d65d94d)

## Result:

Thus the images are read, displayed, and written ,and color conversion was performed successfully using the python program.

