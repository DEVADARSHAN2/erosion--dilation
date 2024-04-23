## EX 09 Implementation-of-Erosion-and-Dilation
### Aim
To implement Erosion and Dilation using Python and OpenCV.
### Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
#### Step1:<br>
Import the necessary pacakages

#### Step2:<br>
Create the text using cv2.putText

#### Step3:<br>
Create the structuring element

#### Step4:<br>
Erode the image


#### Step5: <br>
Dilate the Image

 
### Program:
```
NAME: DEVADARSHAN A S 
REG.NO: 212222110007
```

##### Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
##### Create the Text using cv2.putText
``` Python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'DEVA',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
##### Create the structuring element
``` Python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
##### Erode the image
``` Python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

```
##### Dilate the image
``` Python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')



```
### Output:
#### Display the input Image
![Screenshot 2024-04-23 104018](https://github.com/DEVADARSHAN2/erosion--dilation/assets/119432150/ff10d840-16c9-4df8-9c4a-ce0f6d6853b9)

#### Display the Eroded Image
![Screenshot 2024-04-23 104039](https://github.com/DEVADARSHAN2/erosion--dilation/assets/119432150/6351ee9e-438e-4c56-8b63-0f710fd9f589)

#### Display the Dilated Image
![Screenshot 2024-04-23 104053](https://github.com/DEVADARSHAN2/erosion--dilation/assets/119432150/6aa3a3d2-4cc4-49ed-8bb6-6b33ea492b5a)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
