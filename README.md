Image_Acqusition-_using_Web_Camera
# Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7

## Algorithm
### Step 1:
Import OpenCV Package.
<br>
### Step 2:
Capture Video from Webcam. Use VideoCapture(0) to access the webcam and start capturing video.
<br>
### Step 3:
Read Video or Image. Utilize 'imread' to read a video frame or image from the webcam.
<br>
### Step 4:
Save Image to File. Employ 'imwrite' to save the captured image to a file.
<br>
### Step 5:
Display Video or Image. Use 'imshow' to display the captured video frame or image.
<br>
### Step 6:
End Program with 'q'. Allow the program to be terminated by pressing the 'q' key.
<br>

## Program:
``` Python
### Developed By: PYNAM VINODH
### Register No: 212223240131

## i) Write the frame as JPG file
import cv2
cap=cv2.VideoCapture(0)
frame_number=0

while frame_number<5:
    ret,frame=cap.read()
    cv2.imshow('frame',frame)
    cv2.imwrite(f"frame_(frame_number).jpg",frame)
    frame_number+=1
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()


## ii) Display the video

videoCaptureObject = cv2.VideoCapture(0)
while True:
    ret, frame = videoCaptureObject.read()
    cv2.imshow('myimage', frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
videoCaptureObject.release()
cv2.destroyAllWindows()  




## iii) Display the video by resizing the window

import cv2
cap=cv2.VideoCapture(0)
cv2.namedWindow('Video',cv2.WINDOW_NORMAL)
while True:
    ret,frame=cap.read()
    cv2.imshow('Video',frame)
    cv2.resizeWindow('Video',100,200)
    if cv2.waitKey(1) & 0xFF ==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()        



## iv) Rotate and display the video

cap=cv2.VideoCapture(0)
rotation_angel=90

while True:
    ret,frame=cap.read()
    rotated_frame=cv2.rotate(frame,cv2.ROTATE_90_CLOCKWISE)
    cv2.imshow('Rotated Video',rotated_frame)
    if cv2.waitKey(1)&0xFF==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()        
```
## Output

### i) Write the frame as JPG image
![Screenshot 2024-10-01 111023](https://github.com/user-attachments/assets/e1f6f270-4a4d-4bc0-990a-a9492f182230)



</br>
</br>


### ii) Display the video

![Screenshot 2024-10-01 110750](https://github.com/user-attachments/assets/565059c1-d2cf-4a64-b911-79910aa0d6c6)


</br>
</br>


### iii) Display the video by resizing the window

![Screenshot 2024-10-01 110818](https://github.com/user-attachments/assets/cf45a64f-a5df-44a0-8ce2-679634eac67b)


</br>
</br>



### iv) Rotate and display the video

![Screenshot 2024-10-01 111216](https://github.com/user-attachments/assets/9e72d30c-8d68-4bc5-833d-afbb04cfe34c)


</br>
</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
