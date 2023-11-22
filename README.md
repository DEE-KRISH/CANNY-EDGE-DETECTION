# Canny Edge Detection Algorithm

Canny Edge Detection is an image processing technique used to detect edges in an image while suppressing noise.

The Canny Edge Detection algorithm is a widely-used technique in computer vision and image processing. It is designed to identify and highlight edges in an image, making it valuable for tasks such as object detection, image segmentation, and feature extraction.

## Algorithm Steps

1. **Smoothing:**
   - The image is convolved with a Gaussian filter to reduce noise.
   - This step helps in removing high-frequency noise and small details.

2. **Gradient Calculation:**
   - The gradients (both magnitude and direction) of the smoothed image are calculated.
   - The gradient represents the rate of change of intensity in different directions.

3. **Non-maximum Suppression:**
   - The algorithm performs non-maximum suppression to thin the edges.
   - Only the local maxima in the gradient direction are retained, while other values are set to zero.
   - This step helps in preserving only the most prominent edges.

4. **Double Thresholding:**
   - The edges are classified into strong, weak, and non-relevant edges based on gradient values.
   - Pixels with gradient magnitudes above a high threshold are considered strong edges.
   - Pixels with values below a low threshold are considered non-relevant.
   - Pixels with values between the high and low thresholds are classified as weak edges.

5. **Edge Tracking by Hysteresis:**
   - Weak edges are included in the final edge map only if they are connected to strong edges.
   - This step helps in eliminating isolated weak edges that may be caused by noise.

## Applications

Canny Edge Detection is utilized in various computer vision and image processing applications, including:
- Object detection
- Image segmentation
- Feature extraction

The resulting edge map highlights the boundaries and contours of objects in an image, making it easier to analyze and understand the structure of the visual information.
