## This fork is giving a better quality giving the developer possibility to apply CLAHE on image, giving you opportunity to add an extra "True" in the function.
Without CLAHE: 


<p><img align="left" src="https://user-images.githubusercontent.com/99593023/221321786-3df75aea-811d-4786-af14-0d22485ac25f.png"  height="300">
</p>



<p  >

With CLHAE:

<img align="center" src="https://user-images.githubusercontent.com/99593023/221321703-56e78ca3-d92f-443d-932e-d8486a1e3ab5.png"  height="300">

</p>

# Fingerprint-Enhancement-Python

Uses oriented gabor filter bank to enhance the fingerprint image. The orientation of the gabor filters is decided by the orientation of ridges in the input image. 

## Installation and Running the tests

### method 1 - use the library, and remember to change the code from your package
  ```
  pip install fingerprint_enhancer
  ```
  
  **Usage:**
  ```
import fingerprint_enhancer								# Load the library
import cv2

img = cv2.imread('demo.jpg', 0)						# read input image
out = fingerprint_enhancer.enhance_Fingerprint(img, False, True)		# enhance the fingerprint image, the third argument is using 
cv2.imshow('enhanced_image', out);						# display the result
cv2.waitKey(0)											# hold the display window
  ```
  - Alternatively, the script "src/example.py" can be used to run the example for this library.

### method 2 - use the source codes
1) go into the src folder
- if on "develop" branch, run the file "example.py"
- if on "master" branch, run the file file "main_enhancement.py" 

2) The sample images are stored in the "images" folder

3) The enhanced image will be stored in the "enhanced" folder

## important note:
The Develop Branch is what is up to date. Other branches might not be up to date.


## Results
![temp](https://cloud.githubusercontent.com/assets/13918778/25770604/637b3f38-31ee-11e7-818f-1f8359c96e07.jpg)

## Theory
- We use oriented gabor filters to enhance a fingerprint image. The orientation of the gabor filters are based on the orientation of the ridges. the shape of the gabor filter is based on the frequency and wavelength of the ridges.

## License
- This project is licensed under the BSD 2 License - see the LICENSE.md file for details

## Acknowledgements
- This program is based on the paper: Hong, L., Wan, Y., and Jain, A. K. 'Fingerprint image enhancement: Algorithm and performance evaluation'. IEEE Transactions on Pattern Analysis and Machine Intelligence 20, 8 (1998), pp 777-789.

- The author would like to thank Dr. Peter Kovesi (This code is a python implementation of his work)
