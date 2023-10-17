# EX-10 EROSION AND DILATION
### Aim
To implement Erosion and Dilation using Python and OpenCV.
### Software Required
Anaconda - Python 3.7 , OpenCV
### Algorithm:
- Step1: Import the necessary packages.
- Step2: Use cv2.putText to add the text to the image at specific coordinates.
- Step3: Define two kernels (kernel and kernel1) for morphological operations.
- Step4: Display the eroded image using cv2.imshow.
- Step5: Display the dilated image using cv2.imshow.

Developed By: IYYANAR S
Register No: 212222240036<br>
### Program:
- Importing the necessary packages
  ``` Python
  import cv2
  import numpy as np
  ```
- Create the Text using cv2.putText.
  ```Python
  img1=np.zeros((100,500),dtype="uint8")
  font=cv2.FONT_HERSHEY_PLAIN
  cv2.putText(img1,"IYYANAR S 212222240036",(5,60),font,2,(255),5,cv2.LINE_AA)
  cv2.imshow("Original Image",img1)
  cv2.waitKey(0)
  ```
  ![91](https://github.com/Iyyanar22009120/EROSION-AND-DILATION/assets/118680259/3e5164ce-c902-46c4-89bc-1c044e5bad0e)

- Create the structuring element.
  ```Python
  kernel=np.ones((5,5),np.uint8)
  kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
  ```
- Erode the image.
  ```Python
  cv2.erode(img1, kernel)
  image_erode = cv2.erode(img1,kernel1)
  cv2.imshow("Erode Image",image_erode)
  cv2.waitKey(0)
  ```
![92](https://github.com/Iyyanar22009120/EROSION-AND-DILATION/assets/118680259/8af6158e-d451-4663-9725-a0794291b7f1)

- Dilate the image.
  ```Python
  image_dilatel=cv2.dilate(img1,kernel1)
  cv2.imshow("Dilate Image",image_dilatel)
  cv2.waitKey(0)
  ```
![93](https://github.com/Iyyanar22009120/EROSION-AND-DILATION/assets/118680259/462a71b5-1a07-4998-ac96-a12a55208ff9)

### Result
Thus the generated text image is eroded and dilated using python and OpenCV.
