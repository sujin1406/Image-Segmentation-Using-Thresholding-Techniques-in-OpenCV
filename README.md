# Image-Segmentation-Using-Thresholding-Techniques-in-OpenCV

# Aim
1. To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.
2. The program performs the following operations:

 Global Thresholding
 Adaptive Thresholding
 Otsu's Thresholding
# Software Used
Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
NumPy
Matplotlib
# Algorithm
## Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

## Step 2:
Load the input image using OpenCV.

## Step 3:
Convert the input image into grayscale format.

## Step 4: Global Thresholding
1. Select a fixed threshold value.
2. Apply thresholding to separate foreground and background pixels.
3. Display the thresholded image.
## Step 5: Adaptive Thresholding
1. Compute threshold values for small regions of the image.
2. Apply Adaptive Mean Thresholding.
3. Apply Adaptive Gaussian Thresholding.
4. Display the segmented images.
## Step 6: Otsu's Thresholding
1. Automatically determine the optimal threshold value.
2. Apply Otsu's thresholding technique.
3. Display the segmented image.
## Step 7:
Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

# Program
Developed By : SUJIN M L


Register No: 212225040435

# Output
## Original Image
```
import cv2
import matplotlib.pyplot as plt

img = cv2.imread("GT.jpg")

if img is None:
    print("Error: Image not found. Check the file path.")
else:
    img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
    plt.imshow(img_rgb)
    plt.title("Original Image")
    plt.axis("off")
    plt.show()
```
<img width="1096" height="667" alt="image" src="https://github.com/user-attachments/assets/658b3d48-6645-4825-ab92-55046967d9a4" />

## Original Grayscale Image
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("GT.jpg", cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap="gray")
plt.title("Original Grayscale Image")
plt.axis("off")
plt.show()
```
<img width="1095" height="650" alt="image" src="https://github.com/user-attachments/assets/4e085f7a-3b52-4c6c-882f-5f19ace0f005" />

## Global Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("GT.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(img, 127, 255, cv2.THRESH_BINARY)
plt.imshow(result, cmap="gray")
plt.title("Global Thresholding")
plt.axis("off")
plt.show()
```
<img width="1097" height="658" alt="image" src="https://github.com/user-attachments/assets/6bd5c61f-55cc-4605-bb0a-3c0117b70ee8" />

## Adaptive Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("GT.jpg", cv2.IMREAD_GRAYSCALE)
result = cv2.adaptiveThreshold(
    img, 255,
    cv2.ADAPTIVE_THRESH_GAUSSIAN_C,
    cv2.THRESH_BINARY,
    11, 2
)
plt.imshow(result, cmap="gray")
plt.title("Adaptive Thresholding")
plt.axis("off")
plt.show()
```
<img width="1100" height="659" alt="image" src="https://github.com/user-attachments/assets/c61282d9-b80d-4e53-a3a7-a837b30a0358" />

## Otsu's Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("GT.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(
    img, 0, 255,
    cv2.THRESH_BINARY + cv2.THRESH_OTSU
)
plt.imshow(result, cmap="gray")
plt.title("Otsu's Thresholding")
plt.axis("off")
plt.show()
```
<img width="1094" height="654" alt="image" src="https://github.com/user-attachments/assets/9d61d93d-9d97-4f54-8752-acfd918674bd" />

# Result
Thus, image segmentation is successfully performed using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques in OpenCV.
