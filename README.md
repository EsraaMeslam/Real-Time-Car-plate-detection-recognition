# Real-Time-Car-plate-detection-recognition

steps:
<br>
Step 1: Video to Frames
After converting the video to frames and resizing them for efficient processing, we define the region of interest (ROI) where license plates are expected.
<br>
Step 2: Grayscale Conversion
We convert the ROI to grayscale to simplify and speed up processing.
<br>
Step 3: Applying Bilateral Filter
The bilateralFilter function effectively reduces noise in the image while preserving edges, making it ideal for preprocessing.
<br>
Step 4: Edge Detection with Canny
We apply the Canny edge detection algorithm to identify edges in the image.
<br>
Step 5: Finding Contours
Contours are found to outline the potential license plates. We sort and reverse them to find the largest contours.
<br>
Step 6: Contour Verification
We verify if the contours represent a license plate by checking if they have four sides.
<br>
Step 7: Mask Creation
A mask of the same size as the image is created, and the contours of the potential license plate are drawn on it. We then use bitwise operations to extract the text area.
<br>
Step 8: Text Recognition with EasyOCR
Using EasyOCR, we read text from the extracted region. If successful, the recognized text is typically the license plate number.
