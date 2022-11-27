# Image Processing Project
Contributors:  
Stephen Halligan  
Adam Moen  
Edosa Osarenotor  

# Blogs 
Stephen: (https://stephenhalligan.wordpress.com/image-processing-project/)  
Adam: (https://imageprocessing2.wordpress.com/)  
Edosa: (https://edosaimageprocessing.wordpress.com)

## What does this program do?

This program is a banknote validity checker. In other words, we can use it to ensure a banknote is authentic and not counterfeit. We do this by using image comparison, to comapre the user's input image against an authentic banknote. If the details are similar, we can assume the banknote is valid (or a really good counterfeit!)

We also use serial nubmer checkers to validate. If the program detects a serial number on the banknote, we run a validity check on that serial number to ensure that it adds up using the European system for modern Euro note serial numbers.

## How does it work?

We start by taking images, and converting them to text. After a bit of research, we found the easiest way of doing this was by utilising a module named pytesseract. With a bit of tweaking, we managed to get an output which produces the value of the note in string format. 

We use 'if' statements to go through our output string, and confirm the value of the note using print statements.
Pytesseract is a very useful tool when it comes to recognising letters and numbers from an image, however, it often wrongly detect noise as letters/digits. To counteract this, we use image processing techniques like opening/closing and thresholding in order to enhance the image prior to running pytesseract.

For the validity checker using comparison, we used the SIFT function alongside matplotlib. This function can be used to locate keypoints and descriptors in an image. Once these keypoints have been identified, we can compare the keypoints present in one image with the keypoints in another. 

After a bit of research and some searching through stackoverflow, we found that we can get a comparison of the 2 images based on keypoints. If we use the length between the keypoints, multiplied by a set value, we can get somewhat of a 'similarity percentage' between the 2 images. 
