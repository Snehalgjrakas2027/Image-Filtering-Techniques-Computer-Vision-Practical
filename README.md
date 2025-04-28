
# Image Filtering Techniques – Computer Vision Practical

## Aim

To apply and analyze the effects of **Gaussian**, **Sobel**, and **Median** filters on digital images, demonstrating their respective functionalities in **noise reduction**, **edge detection**, and **noise removal**.

---

## Overview

This practical focuses on implementing three fundamental image filtering techniques:

- **Gaussian Filter**: Used for smoothing and reducing image noise.
- **Sobel Filter**: Used for detecting edges within an image.
- **Median Filter**: Used for effective removal of "salt-and-pepper" noise.

Each filter is applied to sample images to observe and analyze its impact on image quality and features.

---

## Requirements

- Python 3.x
- OpenCV (`cv2`) library
- NumPy (`numpy`)

Install the required libraries using:

```bash
pip install opencv-python numpy
```

---

## How to Run

1. Clone or download the project files.
2. Ensure that the input images are placed in the working directory.
3. Execute the respective scripts for each filter or a combined script with all filters.

Example:

```bash
python gaussian_filter.py
python sobel_filter.py
python median_filter.py
```

or for a combined program:

```bash
python filters_combined.py
```

---

## Filters Implemented

### 1. Gaussian Filter
- Applies a Gaussian blur to smooth the image.
- Reduces noise and detail.

Example:

```python
blurred = cv2.GaussianBlur(img, (5, 5), 0)
```

---

### 2. Sobel Filter
- Detects edges by calculating the gradient of image intensity.
- Highlights vertical, horizontal, or diagonal edges.

Example:

```python
sobelx = cv2.Sobel(img, cv2.CV_64F, 1, 0, ksize=5)
sobely = cv2.Sobel(img, cv2.CV_64F, 0, 1, ksize=5)
```

---

### 3. Median Filter
- Replaces each pixel's value with the median value of its neighbors.
- Especially effective for removing salt-and-pepper noise.

Example:

```python
median = cv2.medianBlur(img, 5)
```

---

## File Structure

```
/Image_Filters
    ├── gaussian_filter.py
    ├── sobel_filter.py
    ├── median_filter.py
    ├── filters_combined.py   # (Optional) Combined all-filters script
    └── input_image.jpg
```

---

## Observations

- **Gaussian Filter** softens the image and reduces minor noise.
- **Sobel Filter** highlights edges, useful for detecting object boundaries.
- **Median Filter** removes noise while preserving edges better than Gaussian blur.

---

## Notes

- Make sure the image paths are correct.
- You can modify the kernel sizes and parameters to observe different filtering effects.
- Use `cv2.imwrite()` to save the filtered output images if required.

---
