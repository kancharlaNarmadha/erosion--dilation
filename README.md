
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
NAME: Kancharla Narmadha
REG.NO: 212222110016
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
cv2.putText(img ,'Narmadha',(60,70),font,2,(255),5,cv2.LINE_AA)
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
(-0.5, 399.5, 99.5, -0.5)
![Untitled](https://github.com/swedha333/erosion--dilation/assets/119559316/af5fef88-3166-4fc7-9d16-b8202eea9042)

#### Display the Eroded Image
(-0.5, 399.5, 99.5, -0.5)
![Untitled](https://github.com/swedha333/erosion--dilation/assets/119559316/025c2f41-cb2a-4dd6-9ae5-9ad56ac8806e)

#### Display the Dilated Image
(-0.5, 399.5, 99.5, -0.5)
![Untitled](https://github.com/swedha333/erosion--dilation/assets/119559316/5f801918-726b-4eba-88c9-061773a7ffb6)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
