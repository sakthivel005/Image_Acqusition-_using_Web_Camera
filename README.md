# Image_Acqusition-_using_Web_Camera
## Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Use cv2.VideoCapture(0) to access web camera

### Step 2:
Use cv2.imread to read the video or image

### Step 3:
Use cv2.imwrite to save the image

### Step 4:
Use cv2.imshow to show the video

### Step 5:
End the program and close the output video window by pressing 'q'.

## Program:

### Developed By: SAKTHIVEL R
### Register No: 212222100044

## i) Write the frame as JPG file
```
import cv2
viedoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=viedoCaptureObject.read()
    cv2.imwrite("wall.jpg",frame)
    result=False
viedoCaptureObject.release()
cv2.destroyAllWindows()
```


## ii) Display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('wall',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```


## iii) Display the video by resizing the window
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222100044_SAKTHIVEL R',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```



## iv) Rotate and display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222100044_SAKTHIVEL R',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
```








## Output

### i) Write the frame as JPG image

![Screenshot 2024-02-28 194138](https://github.com/sakthivel005/Image_Acqusition-_using_Web_Camera/assets/120550359/3d8c5f1f-de54-48f1-acc1-33cc3050a035)



### ii) Display the video

![Screenshot 2024-02-28 192923](https://github.com/sakthivel005/Image_Acqusition-_using_Web_Camera/assets/120550359/185765bc-ec64-41a0-9aeb-ff2e8e4891c7)



### iii) Display the video by resizing the window
![Screenshot 2024-02-28 193358](https://github.com/sakthivel005/Image_Acqusition-_using_Web_Camera/assets/120550359/3cc51b22-5310-4572-9c6a-3064da67ec1e)




### iv) Rotate and display the video
![Screenshot 2024-02-28 193836](https://github.com/sakthivel005/Image_Acqusition-_using_Web_Camera/assets/120550359/f66d0d2f-ae5d-4c77-89ba-e3388b0c5adb)






## Result:
Thus the image is accessed from webcamera and displayed using openCV.
