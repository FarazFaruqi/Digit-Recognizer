# Digit-Recognizer #
## Digit Recognition using the MNIST dataset ##
This project revolves around a program that will recognize a handwritten digit fed to it - quickly and correcly.

I am trying out several machine learning algorithms and concepts. I will include the description of all the algorithms I choose and the reason out here.
* ### SOFTMAX ###
I started out using softmax in tensorflow. This is a nice algorithm for starters as it gives a fairly good sense of what is to be done and how. Although it gave me was very easy to implement as I had to just call a few functions and not do any proper coding, it gave me a fair idea of what lay ahead.

* ###Thresholding  
In order to extract the features, the images had to first be processed. I used OpenCV to Threshold the image using the Otsu's method for calculating the apt threshold value.

* ### Principal Component Analysis ###  
I used PCA as a dimsension reduction algorithm. The original extracted array was 6000x28x28. I did some processing and reduced this array to 786x10 array. Now, for PCA I had to calculate Eigen Vectors for features. But the Eigen AA' would give me 786x786 matrix which is too large to compute for vectors. I tried out A'A and this gave me a 10x10 matrix with the best Eigen vectors. Similarly, I applied this to the test images and extracted the features. Later I calulated the simple distance between the test_image and the given digits. The image with the least distance was predicted as the answer. I got an accuracy of 78.3%.  
