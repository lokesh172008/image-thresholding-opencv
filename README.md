# Image Segmentation Using Thresholding Techniques in OpenCV

## Aim

To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.

The program performs the following operations:

- Global Thresholding
- Adaptive Thresholding
- Otsu's Thresholding

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Load the input image using OpenCV.

### Step 3:

Convert the input image into grayscale format.

### Step 4: Global Thresholding

- Select a fixed threshold value.
- Apply thresholding to separate foreground and background pixels.
- Display the thresholded image.

### Step 5: Adaptive Thresholding

- Compute threshold values for small regions of the image.
- Apply Adaptive Mean Thresholding.
- Apply Adaptive Gaussian Thresholding.
- Display the segmented images.

### Step 6: Otsu's Thresholding

- Automatically determine the optimal threshold value.
- Apply Otsu's thresholding technique.
- Display the segmented image.

### Step 7:

Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

## Program

## Developed By

**Name:** 
K.Lokesh Achari

**Register No:**
212225040208

## Output

### Original Grayscale Image
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("baseball.jpg", cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap="gray")
plt.title("Original Grayscale Image")
plt.axis("off")
plt.show()
```
<img width="891" height="542" alt="639266102-298ece9c-5cc3-46fc-ad0e-3087cb7a7cc8" src="https://github.com/user-attachments/assets/de29d90d-7ac0-4015-bf6d-3b48b07f56cc" />


### Global Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("baseball.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(img, 127, 255, cv2.THRESH_BINARY)
plt.imshow(result, cmap="gray")
plt.title("Global Thresholding")
plt.axis("off")
plt.show()
```
<img width="862" height="552" alt="639266232-4776eef9-450c-423d-a11f-1105adc441f9" src="https://github.com/user-attachments/assets/eb4be663-6bad-4004-a5ae-d4edf60fa1ba" />


### Adaptive Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("baseball.jpg", cv2.IMREAD_GRAYSCALE)
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
<img width="909" height="536" alt="639266397-6c0c67b2-a4f5-4ab9-be60-3d1f5eb58f4d" src="https://github.com/user-attachments/assets/d1467343-a226-4f77-9c9d-e99a9e01f381" />

### Otsu's Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("baseball.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(
    img, 0, 255,
    cv2.THRESH_BINARY + cv2.THRESH_OTSU
)
plt.imshow(result, cmap="gray")
plt.title("Otsu's Thresholding")
plt.axis("off")
plt.show()
```
<img width="869" height="527" alt="639266522-b952c6e9-08d6-49f5-833c-8223f33246be" src="https://github.com/user-attachments/assets/4d8e43de-4107-44f9-88ae-56acac9af025" />


## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 
