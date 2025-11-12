# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
import the neccesary packages
### Step2:
Create the text using cv2.put Text
### Step3:
create the structuting element
### Step4:
Erodde the image
### Step5:
Dilate the image

 
## Program:

``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
def load_image():
    blank_image = np.zeros((600,600))
    font = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_image,text='Jenittan',org=(600,800),fontFace=font,fontScale = 5,color=(255,255,255),thickness=15,lineType=cv2.LINE_AA)
    return blank_image
def display_img(img):
    fig = plt.figure(figsize=(12,10))
    ax=fig.add_subplot(111)
    ax.imshow(img,cmap='gray')
    plt.show()
img=load_image()
display_img(img)
kernel=np.ones((5,5),dtype=np.uint8)
erosion = cv2.erode(img,kernel,iterations = 2)
display_img(erosion)
dilution=cv2.dilate(img,kernel,iterations=2)
display_img(dilution)

```
## Output:

### Display the input Image
<img width="742" height="560" alt="Screenshot 2025-11-12 221516" src="https://github.com/user-attachments/assets/7fc24d46-b071-4aa6-8810-47a2c4580533" />


### Display the Eroded Image
<img width="718" height="555" alt="Screenshot 2025-11-12 221526" src="https://github.com/user-attachments/assets/5f32f38f-c847-4bd6-90d1-458f728bd923" />


### Display the Dilated Image
<img width="726" height="550" alt="Screenshot 2025-11-12 221536" src="https://github.com/user-attachments/assets/b8dcba00-66fa-41df-bc3a-6434cdcbe93e" />



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
