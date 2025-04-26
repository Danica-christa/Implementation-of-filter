# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.

### Step2
Convert the image from BGR to RGB.

### Step3
Apply the required filters for the image separately.

### Step4
Plot the original and filtered image by using matplotlib.pyplot.

### Step5
End the program.

## Program:
### Developed By   : DANICA CHRISTA
### Register Number: 212223240022

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("img0.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```

ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```

iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```

iv)Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## OUTPUT:
## original image:
![image](https://github.com/user-attachments/assets/c82bc6c1-8195-4c55-b545-8ac2f00abf6e)


### 1. Smoothing Filters

## i) Using Averaging Filter
![image](https://github.com/user-attachments/assets/893e0e14-cc36-4c99-8268-d833ed46009e)



## ii)Using Weighted Averaging Filter
![image](https://github.com/user-attachments/assets/7dddff0f-a61d-4b60-bad0-c2c4abe2ad40)




## iii)Using Gaussian Filter
![image](https://github.com/user-attachments/assets/88e64523-f5a7-40b8-8a39-566ed1f14451)





## iv) Using Median Filter
![image](https://github.com/user-attachments/assets/1de66690-4001-4fc1-b7ee-2618809d4eb2)






### 2. Sharpening Filters
</br>

## i) Using Laplacian Kernal
![image](https://github.com/user-attachments/assets/1244c999-4afe-43f8-a1d0-a76f695575df)




## ii) Using Laplacian Operator
![image](https://github.com/user-attachments/assets/91f65dd6-f63e-45af-b796-d91c37028094)





## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.



