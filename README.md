# Number-Plate-Detection
License Plate Recognition is an image-processing technology used to identify vehicles by their license plates. This technology is used in various security and traffic applications. I made this using simple Python code.
Steps involved in License Plate Recognition
## 0. Reading in Image, Grayscale and Blur:
![read](https://user-images.githubusercontent.com/62790398/122669118-74a4d500-d1d9-11eb-978b-ee8ef2e345cb.png)
## 1. Applying filters and find edges for locaalization
![filter](https://user-images.githubusercontent.com/62790398/122669142-92723a00-d1d9-11eb-8f81-091d87a836a8.png)

## 2. Finding Contours and Apply Mask: 
Maximum the number plates are written in white FLAT surfaces in the car. Sp, Making Greyscale and identifying the edges is very helpful to recognise the text in NumberPlate. The first step is to detect the License plate from the car. We will use the contour option in OpenCV to detect for rectangular objects to find the number plate. The accuracy can be improved if we know the exact size, color and approximate location of the number plate. Normally the detection algorithm is trained based on the position of camera and type of number plate used in that particular country. This gets trickier if the image does not even have a car, in this case we will an additional step to detect the car and then the license plate.

![download](https://user-images.githubusercontent.com/62790398/122669152-9f8f2900-d1d9-11eb-8025-37ec5ccb6e56.png)

## 3. Character Segmentation: 
Once we have detected the License Plate we have to crop it out and save it as a new image. Again this can be done easily using OpenCV.

![char](https://user-images.githubusercontent.com/62790398/122669161-aae25480-d1d9-11eb-85ac-ee0285ab8a7d.png)

## 4. Character Recognition using OCR: 
Now, the new image that we obtained in the previous step is sure to have some characters (Numbers/Alphabets) written on it. So, we can perform OCR (Optical Character Recognition) on it to detect the number.

![ocr](https://user-images.githubusercontent.com/62790398/122669172-b9307080-d1d9-11eb-863e-28e005d46df6.png)

