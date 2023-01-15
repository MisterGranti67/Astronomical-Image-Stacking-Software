
# (LEPI) Logiciel d'Édition Profesionnel d'Image
[![GPLv3 License](https://img.shields.io/github/license/MisterGranti67/Astronomical-Image-Stacking-Software) 
[![Python 3.10.5](https://camo.githubusercontent.com/44da37f0f02bf104f0650fa5f2c754ed3f6166066c9210f31bacb9e63d60736e/68747470733a2f2f696d672e736869656c64732e696f2f707970692f707976657273696f6e732f70796261646765732e737667)](https://www.python.org/downloads/)




## 1. The project's goal
During a tutored project for our IT GOAL, we have to create image editing software (based on a .fits, .fit)
The project is carried out in French, only this document is in English.

[![logiciel](https://github.com/MisterGranti67/Astronomical-Image-Stacking-Software/tree/main/img/logiciel.png)]

## 2. Prerequisites
### 2.1 The programming language
We have chosen the Python programming language (**Version 3.10.4 recommended**), being simplified to use and rich in library, it is easier for us to develop thanks to this one. The downside is that it is cumbersome to use, some functions can take several tens of minutes to run.
### 2.2 Libraries
#### 2.2.1 Astropy
Use the ```pip install astropy[all]``` to download the latest version of the library. It is used to simplify our functions, especially on FITS images
#### 2.2.1 Matplotlib
Use the ```pip install matplotlib``` to download the latest version of the library. It is used to display our images and graphics on the application
#### 2.2.1 Numpy
Use the ```pip install numpy``` to download the latest version of the library. It is used to calculate easily thanks to the different functions
#### 2.2.1 scipy
Use the ```pip install scipy``` to download the latest version of the library. It is used to rotate a matrix
#### 2.2.1 Pyinstaller
Use the ```pip install Pyinstaller``` to download the latest version of the library. It is used to generate an .exe file
## 3. Installation
### 3.1 With the .exe
> a. Create a folder
>> b. Place the .exe in it
>>> c. Create an img folder in this folder
>>>> d. Place your "M13_blue" folder holding the fit images named "M13_blue_000X"
>>>>> e. Run the .exe file

### 3.1 Without the .exe
> a. Create a folder
>> b. Place the files main.py, Calculation.py, Filters.py, Interface_front.py, Normalization.py, Stacking.py, Stacking_front.py in the file
>>> c. Create an img folder in this folder
>>>> d. Place your file "M13_blue" holding the name fit images "M13_blue_000X"
>>>>> e.Open the main.py file and run the command "```python main.py```"

## 4. Features
### 4.1 Stacking
#### 4.1.1 Sum
Assembly of several images by adding the pixels of each image represented by a 2d array
#### 4.1.1 Average
Assembling several images using the average of each pixel of the different images represented by a 2d array
#### 4.1.1 Median
Assembling several images by determining the median of each pixel of the different images represented by a 2d array.
#### 4.1.1 Sigma
Additive stitching of multiple images by adding each image with their outliers filter by the deviation and dispersion of the median for the different images of represented by a 2d array
### 4.2 Filters
#### 4.2.1 Outliers
##### 4.2.1.1 Median
Allows you to remove outliers from each image in a multi-image list and replace outliers with the median based on the deviation/dispersion around the median of Q1 and Q3 with the interquartile range
##### 4.2.1.2 Average
Remove outliers from each image in a list with multiple images and replace outliers with the mean based on the deviation/dispersion around the median of Q1 and Q3 with the interquartile range
##### 4.2.1.3 Sigma
Remove the outliers from each image in a list with multiple images and replace the outliers with the deviation and dispersion of the median based on the deviation/dispersion around the median of Q1 and Q3 with the interquartile range

#### 4.2.2 Butterworth
##### 4.2.2.1 High pass
Allows to apply an image represented via a 2d array a butterworth high pass filter by converting our image to frequency via the fourier transform and applying the butterworth high pass filter and converting it back into a pixel
##### 4.2.2.2 low pass
Allows to apply an image represented via a 2d array a butterworth low pass filter by converting our image to frequency via the fourier transform and applying the butterworth low pass filter and converting it back into a pixel
#### 4.2.3 Gaussian
##### 4.2.3.1 High pass
Allows to apply a Gaussian high pass filter which applies a Gaussian convolution matrix on each pixel of an image represented via a 2d array and subtracts it from the base image making a high = data-low(gauss)
##### 4.2.3.2 Simple
to apply a Gaussian convolution matrix giving a blur effect on each pixel of an image represented via a 2d array

#### 4.2.4 Median
Allows you to give a filtered image of each pixel by replacing them with the median of each neighboring pixel at a chosen diameter
#### 4.2.5 Average
Allows you to give a filtered image of each pixel by replacing them with the average of each neighboring pixel at a chosen diameter
#### 4.2.6 Convolution
Allows to apply a convolution matrix on each pixel of an image represented via a 2d table The matrix is applied according to the neighbors located according to the size/diameter of the matrix directly on the pixels of the image
#### 4.2.7 Sobel
Allows you to apply a sobel convolution matrix vertically and horizontally giving an effect of accentuating the edges of objects in the image and applying to each pixel of an image represented via a 2d table
#### 4.2.8 Bilateral
Allows to apply a bilateral filter on an image giving a blur/softening effect on each pixel of an image represented via a 2d table via the value of the Gaussian distribution and the distance between the points in the chosen neighbor diameter allowing to have a fairer distribution than a classic Gaussian filter

## 5. Crédit
- [Matthieu CZARKOWSKI](https://github.com/la-ref) Creation of stacking, filter, scaling algorithms
- [Gauthier CORION](https://github.com/MisterGranti67) Creating the interface with Pyqt


