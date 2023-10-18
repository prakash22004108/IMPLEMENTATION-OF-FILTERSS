# IMPLEMENTATION-OF-FILTERSS
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
Plot the original and filtered image by using matplotlib.pyplot

### Step5
End the program.

## Program:

```
Developed By : PRAKASH R
Register Number: 212222240074
```
### 1. Smoothing Filters

i) Using Averaging Filter
``` python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("flower.jpg")
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
```python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("flower.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter
```python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("flower.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```

iv) Using Median Filter
```python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("flower.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
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
i) Using Laplacian Kernal
```python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("flower.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
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
```python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("flower.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```














## OUTPUT:
### 1. Smoothing Filters


i) Using Averaging Filter

![1 (2)](https://github.com/dharmaraj-007/IMPLEMENTATION-OF-FILTERSS/assets/119560386/6f6db2dd-df49-4433-81e2-29ecaa871288)
![1 (1)](https://github.com/dharmaraj-007/IMPLEMENTATION-OF-FILTERSS/assets/119560386/ac84f9fd-9733-4d12-9212-ae6388da200e)


ii) Using Weighted Averaging Filter

![2(3)](https://github.com/dharmaraj-007/IMPLEMENTATION-OF-FILTERSS/assets/119560386/83fa0cef-90be-4401-9d3c-284171fec57b)
![2(2)](https://github.com/dharmaraj-007/IMPLEMENTATION-OF-FILTERSS/assets/119560386/73241703-6fbc-4e5d-9b65-31407e7900b2)

iii) Using Gaussian Filter

![3 (1)](https://github.com/dharmaraj-007/IMPLEMENTATION-OF-FILTERSS/assets/119560386/f32b454a-346b-44c0-a13c-4b4fa855e143)
![3 (2)](https://github.com/dharmaraj-007/IMPLEMENTATION-OF-FILTERSS/assets/119560386/3051d7d5-fbb2-4165-84a3-c57033af23f5)


iv) Using Median Filter

![4 (1)](https://github.com/dharmaraj-007/IMPLEMENTATION-OF-FILTERSS/assets/119560386/1a59e308-991a-4164-8ebe-14af0e1e9b1b)
![4 (2)](https://github.com/dharmaraj-007/IMPLEMENTATION-OF-FILTERSS/assets/119560386/d44fdaa7-63ed-4142-9d9c-d2b92ed7086c)


### 2. Sharpening Filters


i) Using Laplacian Kernal

![5 (1)](https://github.com/dharmaraj-007/IMPLEMENTATION-OF-FILTERSS/assets/119560386/42bee750-13d7-4cd1-bcd1-cbd2bf4a3e18)
![5 (2)](https://github.com/dharmaraj-007/IMPLEMENTATION-OF-FILTERSS/assets/119560386/bc505f28-4241-4890-ad18-2ad6c40f23f9)

ii) Using Laplacian Operator

![6 (1)](https://github.com/dharmaraj-007/IMPLEMENTATION-OF-FILTERSS/assets/119560386/47390cd4-7b4a-414b-b032-86b1920fabb5)
![6 (2)](https://github.com/dharmaraj-007/IMPLEMENTATION-OF-FILTERSS/assets/119560386/471ddfbb-f525-4b8b-9c5c-a16f49b43085)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
