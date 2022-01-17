# Vehicle License Plate Detection

## Detection and isolation of the number plate from an image consisting of a vehicle followed by using various means to extract the text within the isolated license number plate image.

<h2 align="center">
  <a href="https://docs.google.com/presentation/d/1XwgJYmvngBhe-WtXv0XelLwrL6OibNRC7RqRxFOYJqI/edit?usp=sharing">Presentation (Google Slides)</a>
  
</h2>

<h3 align="center">
Team Members
  
[@Abhishek-Sai-14](https://github.com/Abhishek-Sai-14/)  
[@Dinesh1418](https://github.com/Dinesh1418/)\
[@RahulYalavarthi](https://github.com/RahulYalavarthi/)
</h3>

***
**Step 1:** Input consists of a picture of the vehicle whose license plate number should be detected.

<p align="center">
<img src="https://github.com/likhitkalla/VEHICLE-LICENSE-PLATE-DETECTION/blob/main/image/original_image.jpg" width="425" height="300" />
</p>

**Step 2:**  In the next step, we convert the RGB image to grayscale to discard information that is not needed for processing.

<p align="center">
<img src="https://github.com/likhitkalla/VEHICLE-LICENSE-PLATE-DETECTION/blob/main/image/grayscale_image.jpg" width="425" height="300" />
</p>
  
**Step 3:**  The grayscale image is then preprocessed using bilateral filtering. A bilateral filter is an image smoothing filter that preserves edges, reduces noise, and is non-linear. The intensity of each pixel is replaced by a weighted average of intensity values from nearby pixels.

<p align="center">
<img src="https://github.com/likhitkalla/VEHICLE-LICENSE-PLATE-DETECTION/blob/main/image/Bilateral_filtering.jpg" width="425" height="300" />
</p>
  
**Step 4:**  Then, we use the canny edge detection method to detect edges. Canny edge detection is a technique for extracting useful structural information from different vision objects and significantly reducing the amount of data processing required.

<p align="center">
<img src="https://github.com/likhitkalla/VEHICLE-LICENSE-PLATE-DETECTION/blob/main/image/Canny_image.jpg" width="425" height="300" />
</p>
  
**Step 5:**  In order to extract the license plate from the image, we extract contours that have a rectangle shape with four sides and a closed figure.  
> A contour is defined as the line that joins all the points along the boundary of an image

<p align="center">
<img src="https://github.com/likhitkalla/VEHICLE-LICENSE-PLATE-DETECTION/blob/main/image/Contours_image.jpg" width="425" height="300" />
</p>
  
**Step 6:**  Next, we isolate the contours (License Plate) by cropping by its position within the original image.

<p align="center">
<img src="https://github.com/likhitkalla/VEHICLE-LICENSE-PLATE-DETECTION/blob/main/image/Cropped.jpg"/>
</p>

**Step 7:**  Our next step is to read the cropped image with the Pytesseract package and extract the characters from it.

<p align="center">
<img src="https://github.com/likhitkalla/VEHICLE-LICENSE-PLATE-DETECTION/blob/main/image/pytesseract.png" />
</p>

  
