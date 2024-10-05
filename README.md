# COLOR_CONVERSIONS_OF-IMAGE

## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

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

o	Draw a line from the top-left to the bottom-right of the image.

o	Draw a circle at the center of the image.

o	Draw a rectangle around a specific region of interest in the image.

o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:

o	Convert the image from RGB to HSV and display it.

o	Convert the image from RGB to GRAY and display it.

o	Convert the image from RGB to YCrCb and display it.

o	Convert the HSV image back to RGB and display it.

### Step4:

o	Access and print the value of the pixel at coordinates (100, 100).

o	Modify the color of the pixel at (200, 200) to white.

### Step5:

o	Resize the original image to half its size and display it.

### Step6:

o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.

### Step7:

o	Flip the original image horizontally and display it.

o	Flip the original image vertically and display it.

### Step8:

o	Save the final modified image to your local directory.


##### Program:

### Developed By:mahalakshmi k

### Register Number: 212222240057

PROGRAM

1.Read and Display an Image

Load an image from your local directory and display it.

import cv2 

image=cv2.imread('boat.jpg',1)

image =cv2.resize(image, (400, 300))

cv2.imshow('WINDOW',image)

cv2.waitKey(0)

cv2.destroyAllWindows()

![dipt1](https://github.com/user-attachments/assets/1788280e-65f0-4c3d-9615-88a1fde4ea45)

2.Draw Shapes and Add Text

(1) Draw a line from the top-left to the bottom-right of the image.

import cv2

image = cv2.imread("boat.jpg")

image = cv2.resize(image, (400, 300))

res = cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (255,0,0), 10)

cv2.imshow('WINDOW', res)

cv2.waitKey(0)

cv2.destroyAllWindows

(![dipt2](https://github.com/user-attachments/assets/90ca6b8a-a846-49f6-9ae3-934b50e41cac)
)

(2) Draw a circle at the center of the image.

import cv2

image = cv2.imread("boat.jpg")

image = cv2.resize(image, (400, 300))

height, width, _ = image.shape

center_coordinates = (width // 2, height // 2)

res = cv2.circle(image, center_coordinates, 120, (0, 255, 0), 10)

cv2.imshow('WINDOW', res)

cv2.waitKey(0)

cv2.destroyAllWindows()

![Screenshot (609)](https://github.com/user-attachments/assets/51107c49-45a5-4f30-aab3-ae76116aa153)

(3) Draw a rectangle around a specific region of interest in the image.

import cv2

image = cv2.imread("boat.jpg")

image = cv2.resize(image, (400, 300))

start = (150, 100)

stop = (300, 200)

color = (255, 255, 100)

thickness = 10           

res_img = cv2.rectangle(image, start, stop, color, thickness)

cv2.imshow('WINDOW', res_img)

cv2.waitKey(0)

cv2.destroyAllWindows()

![Screenshot (611)](https://github.com/user-attachments/assets/7e4ff8b4-8811-4e09-afa7-333dbe7bed3f)

(4) Add the text "OpenCV Drawing" at the top-left corner of the image.

import cv2

image = cv2.imread("boat.jpg")

image = cv2.resize(image, (400, 300))

text = "OpenCV Drawing"

position = (10, 50)

font = cv2.FONT_HERSHEY_SIMPLEX

font_scale = 1

color = (255, 255, 255) 

thickness = 2

res = cv2.putText(image, text, position, font, font_scale, color, thickness,cv2.LINE_AA)

cv2.imshow('WINDOW', res)

cv2.waitKey(0)

cv2.destroyAllWindows()

![Screenshot (612)](https://github.com/user-attachments/assets/7e25f273-dfb1-4527-bfea-162b6e408c5b)

iii)Image Color Conversion

(1) Convert the image from RGB to HSV and display it

import cv2

image = cv2.imread('boat.jpg',1)

image = cv2.resize(image,(300,200))

cv2.imshow('ORIGINAL IMAGE',image)

hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)

cv2.imshow('RGB2HSV',hsv)

cv2.waitKey(0)

cv2.destroyAllWindows()

![Screenshot (613)](https://github.com/user-attachments/assets/8d5b66e8-f945-4461-b058-2bde3709a568)

(2) Convert the image from RGB to GRAY and display it.

import cv2

image = cv2.imread('boat.jpg',1)

image = cv2.resize(image,(300,200))

cv2.imshow('ORIGINAL IMAGE',image)

gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)

cv2.imshow('RGB2GRAY',gray)

cv2.waitKey(0)

cv2.destroyAllWindows()

![Screenshot (614)](https://github.com/user-attachments/assets/bf1ed601-1d76-427b-b568-fd245df07dce)

(3) Convert the image from RGB to YCrCb and display it.

import cv2

image = cv2.imread('boat.jpg',1)

image = cv2.resize(image,(300,200))

cv2.imshow('ORIGINAL IMAGE',image)

YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)

cv2.imshow('RGB-2-YCrCb',YCrCb)

cv2.waitKey(0)

cv2.destroyAllWindows()

![Screenshot (615)](https://github.com/user-attachments/assets/c4f7439f-f524-4575-9963-5b03932f23e8)

(4) Convert the HSV image back to RGB and display it.

import cv2

image = cv2.imread('boat.jpg',1)

image = cv2.resize(image,(300,200))

cv2.imshow('ORIGINAL IMAGE',image)

RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)

cv2.imshow('HSV2RGB',RGB)

cv2.waitKey(0)

cv2.destroyAllWindows()

![Screenshot (616)](https://github.com/user-attachments/assets/7cfab9d9-ba70-4ab6-a6bf-c80114dd5e6f)

iv)Access and Manipulate Image Pixels

(1) Access and print the value of the pixel at coordinates (100, 100)

pixel_value = image[100, 100]

print(f"Pixel value at (100, 100): {pixel_value}")

![Screenshot (617)](https://github.com/user-attachments/assets/3b466013-7283-4d39-a141-dd92244ee96e)

(2) Modify the color of the pixel at (200, 200) to white

import cv2

image = cv2.imread('boat.jpg',1)

image = cv2.resize(image,(400,300))

cv2.imshow('ORIGINAL IMAGE',image)

image[200, 200] = [255, 255, 255] 

cv2.imshow('MODIFIED IMAGE', image)

cv2.waitKey(0)

cv2.destroyAllWindows()

![Screenshot (618)](https://github.com/user-attachments/assets/32e87b00-aab6-4b74-b983-10201cd61115)

v)Image Resizing

Resize the original image to half its size and display it.

cv2.imshow('ORIGINAL IMAGE',image)

resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))

cv2.imshow('RESIZED IMAGE', resized_image)

cv2.waitKey(0)

cv2.destroyAllWindows()

![Screenshot (619)](https://github.com/user-attachments/assets/9cabb7ef-265a-4c2a-a809-14db181daa7d)

vi)Image Cropping

Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.

import cv2

image = cv2.imread('boat.jpg',1)

image = cv2.resize(image,(400,300))

x, y = 50, 50

width, height = 100, 100

roi = image[y:y + height, x:x + width]

cv2.imshow('CROPPED IMAGE', roi)

cv2.waitKey(0)

cv2.destroyAllWindows()

import cv2

image = cv2.imread('boat.jpg',1)

image = cv2.resize(image,(400,300))

x, y = 50, 50

width, height = 100, 100

roi = image[y:y + height, x:x + width]

cv2.imshow('CROPPED IMAGE', roi)

cv2.waitKey(0)

cv2.destroyAllWindows()

![Screenshot (620)](https://github.com/user-attachments/assets/f05c7595-db70-4126-a531-e1886dafca53)

vii)Image Flipping

(1) Flip the original image horizontally and display it.

import cv2

image = cv2.imread("boat.jpg")

image = cv2.resize(image,(300,200))

res=cv2.rotate(image,cv2.ROTATE_180)

cv2.imshow('ORIGINAL IMAGE',image)

cv2.imshow('FLIPPED IMAGE', res)

cv2.waitKey(0)

cv2.destroyAllWindows()

![Screenshot (621)](https://github.com/user-attachments/assets/543b426b-e354-4331-a4f8-54850902f39a)

(2) Flip the original image vertically and display it.

import cv2

image = cv2.imread("boat.jpg")

image = cv2.resize(image,(300,200))

res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)

cv2.imshow('ORIGINAL IMAGE',image)

cv2.imshow('FLIPPED IMAGE', res)

cv2.waitKey(0)

cv2.destroyAllWindows()

![Screenshot (622)](https://github.com/user-attachments/assets/b4e19165-b7d8-4420-b5d8-05c0d647f268)

viii)Write and Save the Modified Image

Save the final modified image to your local directory.

import cv2

img = cv2.imread("boat.jpg")

img = cv2.resize(img,(300,200))

cv2.imwrite('boat_pic.jpg',img)

![Screenshot (623)](https://github.com/user-attachments/assets/4c12203c-fa5f-4dbc-87d4-a358e827f851)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







