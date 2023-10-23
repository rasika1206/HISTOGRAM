# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step2:
Calculate the Histogram of Gray scale image and any one channel of the color image.

### Step3:
Display the histograms.

### Step4:
Equalize the color image.

### Step5:
Display the equalized grayscale image.



## Program:
```python
# Developed By:RASIKA.M
# Register Number:212222230117
```
```
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('elsa.jpg')
plt.imshow(Gray_image)
plt.show()
Color_image=cv2.imread('anna.jpg')
plt.imshow(Color_image)
plt.show()
```

# Write your code to find the histogram of gray scale image and color image channels.
```
hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel("gray_scale value")
plt.ylabel("pixel count")
plt.stem(hist)
plt.show()
```

# Display the histogram of gray scale image and any one channel histogram from color image
```
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel("color_scale value")
plt.ylabel("pixel count")
plt.stem(hist1)
plt.show()
```
# Write the code to perform histogram equalization of the image. 
```
equ=cv2.equalizeHist(cv2.imread('tulip.jpg',0))
equ=cv2.cvtColor(equ,cv2.COLOR_BGR2RGB)
plt.title("Equalised Image")
plt.axis("off")
plt.imshow(equ)
plt.show()



```
## Output:
### Input Grayscale Image and Color Image
<br>![Screenshot from 2023-10-23 15-31-03](https://github.com/rasika1206/HISTOGRAM/assets/124434806/40f77c21-fc39-42f7-bde8-cc916600caaf)

<br>![Screenshot from 2023-10-23 15-31-10](https://github.com/rasika1206/HISTOGRAM/assets/124434806/9c9f7657-228e-45e3-9b73-0aaf412e3cb5)

<br>
<br>

### Histogram of Grayscale Image and any channel of Color Image
<br>
<br>

<br>![Screenshot from 2023-10-23 15-31-26](https://github.com/rasika1206/HISTOGRAM/assets/124434806/0ed85098-8a49-4035-be48-aab8de67dba1)

<br>![Screenshot from 2023-10-23 15-31-36](https://github.com/rasika1206/HISTOGRAM/assets/124434806/6b794c06-955a-4895-b266-9cbffcf3beb9)


### Histogram Equalization of Grayscale Image
<br>![Screenshot from 2023-10-23 15-31-51](https://github.com/rasika1206/HISTOGRAM/assets/124434806/3181ebd4-a911-40fb-90d8-5f92392b30d0)


<br>
<br>
<br>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
