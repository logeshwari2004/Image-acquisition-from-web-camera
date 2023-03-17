# Image-Acquisition-from-Web-Camera
## Aim
 
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
```
##Step 1:

Import cv2 and capture the video using cv2.VideoCapture(0)

##Step 2:
Write the captured image using cv2.imwrite("NewPicture.jpg",frame)

##Step 3:
Resize the image using cv2.resize(frame, (0,0), fx = 0.5, fy=0.5)

##Step 4:
Display the image until the loop gets over

##Step 5:
Rotate the image using cv2.rotate(smaller_frame,cv2.cv2.ROTATE_180)
```

## Program:
``` Python
### Developed By:LOGESHWARI.P
### Register No:212221230055

## i) Write the frame as JPG file

VidCap = cv2.VideoCapture(0)
while(True):
    ret,frame = VidCap2.read()
    cv2.imshow('video_image',frame)
    cv2.imwrite("hari.jpg",frame)
    if cv2.waitKey(1) == ord('q'):
        break
    result = False
VidCap.release()
cv2.destroyAllWindows()





## ii) Display the video

VidCap=cv2.VideoCapture(0)
while(True):
    ret,frame=VidCap.read()
    cv2.imshow('myimage',frame)
    if cv2.waitKey(1) == ord('q'):
        break
VidCap.release()
cv2.destroyAllWindows()




## iii) Display the video by resizing the window

cap=cv2.VideoCapture(0)
while(True):
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame = cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2,:width//2]=smaller_frame
    image[height//2:,:width//2]=smaller_frame
    image[:height//2,width//2:]=smaller_frame
    image[height//2:,width//2:]=smaller_frame
    
    cv2.imshow('quadrant_screen',image)
    if cv2.waitKey(1) == ord('q'):
        break
VidCap.release()
cv2.destroyAllWindows()





## iv) Rotate and display the video

cap=cv2.VideoCapture(0)
while(True):
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame = cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2,:width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:,:width//2]=smaller_frame
    image[:height//2,width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:,width//2:]=smaller_frame
    
    cv2.imshow('quadrant_rotated_screen',image)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()

```
## Output

### i) Write the frame as JPG image

![DIP2A](https://user-images.githubusercontent.com/94211349/225951941-a459eb3b-e05c-46f1-a172-a3e429ed8cab.png)




### ii) Display the video


![DIP2B](https://user-images.githubusercontent.com/94211349/225951989-91f334aa-168b-4f2a-bfd9-af0e4b789ed1.jpeg)



### iii) Display the video by resizing the window


![DIP2C](https://user-images.githubusercontent.com/94211349/225952034-613a4132-6a8a-49a2-9964-0bdbbffea321.jpeg)




### iv) Rotate and display the video



![DIP2D](https://user-images.githubusercontent.com/94211349/225952086-ba9fdbca-f760-4d0b-8cad-970cf6c8aefb.png)





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
