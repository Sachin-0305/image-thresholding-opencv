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

```

import cv2
import matplotlib.pyplot as plt

img = cv2.imread("baseball.jpg")

if img is None:
    print("Error: Image not found. Check the file path.")
else:
    img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
    plt.imshow(img_rgb)
    plt.title("Original Image")
    plt.axis("off")
    plt.show()
```

### Step 2:

Load the input image using OpenCV.

```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("baseball.jpg", cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap="gray")
plt.title("Original Grayscale Image")
plt.axis("off")
plt.show()

```

### Step 3:

Convert the input image into grayscale format.

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
### Step 4: Global Thresholding

- Select a fixed threshold value.
- Apply thresholding to separate foreground and background pixels.
- Display the thresholded image.
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


### Step 5: Adaptive Thresholding

- Compute threshold values for small regions of the image.
- Apply Adaptive Mean Thresholding.
- Apply Adaptive Gaussian Thresholding.
- Display the segmented images.

- 
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

### Step 6: Otsu's Thresholding

- Automatically determine the optimal threshold value.
- Apply Otsu's thresholding technique.
- Display the segmented image.

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

### Step 7:

Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

## Program

## Developed By

**Name:** SACHIN M

**Register No:** 212223040177

## Output
<img width="631" height="408" alt="image" src="https://github.com/user-attachments/assets/18a57fa6-200e-44af-adb1-14e6bb08251b" />



### Original Grayscale Image

- The grayscale version of the input image is displayed.
- Serves as the input for thresholding operations.




<img width="628" height="400" alt="image" src="https://github.com/user-attachments/assets/a580aac6-3879-454d-bd16-aa48f787eaae" />


### Global Thresholding

- Original image is displayed.
- Thresholded image is displayed.
- A fixed threshold value is used for segmentation.
- Pixels are classified as foreground or background.

<img width="633" height="410" alt="image" src="https://github.com/user-attachments/assets/62eeebb7-d4ab-484a-81af-6eb2da724d32" />


### Adaptive Thresholding

- Original image is displayed.
- Adaptive Mean Thresholded image is displayed.
- Adaptive Gaussian Thresholded image is displayed.
- Threshold values vary across different regions of the image.
- Suitable for images with uneven illumination.



<img width="638" height="415" alt="image" src="https://github.com/user-attachments/assets/2ce5920b-3dc4-404b-8c9b-c25a5d6040b1" />

### Otsu's Thresholding

- Original image is displayed.
- Otsu segmented image is displayed.
- Optimal threshold value is calculated automatically.
- Produces improved segmentation for bimodal histograms.



<img width="638" height="396" alt="image" src="https://github.com/user-attachments/assets/205ca2f5-bfd6-4165-8e57-3951820d3993" />

## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 
