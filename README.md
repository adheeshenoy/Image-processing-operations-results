# Image Processing Operations

This repository consists of images that were derived after applying image processing operations using the code part of my final project for my Image Processing Fundamentals Course.

Every operation with the subscript cv was implemented using OpenCV4. The rest were implemented using C and C++ algorithmically.

Due to plagarism concerns I was adviced by the professor to not upload the code but the results of each operation instead. 

## Image Processing Operations

Each operation was implemented on two region of interests (x, y, sx, sy):
	* (0, 0, 1200, 200)
	* (0, 200, 1200, 200)

1. add: Adds a user defined intensity to a grey-level image

![Original image](images/mars.jpg) ![Image with Add operation](images/add.jpg)

2. binarize: Perfromed on grey-level images. Based on a user defined threshold value, if the intensity of the pixel is less than the threshold, the intensity is set to 0, else it is set to 255.

![Original image](images/mars.jpg) ![Image with Binarize](images/binarize.jpg)

3. scale: Updates the size of the image to twice or half

![Original image](images/mars.jpg) ![Image with scale](images/scale.jpg)

4. threshold_add: Performed on grey-level images. Based on a user-defined threshold value, if the intensity of the pixel is more than the threshold, a user defined value v1 is added to the pixel. Else, v2 is subtracted.

![Original image](images/mars.jpg) ![Image with threshold_add](images/threshold_add.jpg)

5. double_threshold: Performed on grey-level images. Based on user defined threshold values t1 and t2 (t1 < t2), if the intensity of the pixel is between t1 and t2, the intensity is set to 255. 

![Original image](images/mars.jpg) ![Image with double_threshold](images/double_threshold.jpg)

6. color_mod: Performed on color images. Based on user defined r,g,b values, the values are added to each channel in the color images.

![Original image](images/mars.jpg) ![Image with color_mod](images/color_mod.jpg)

7. 2d_smooth: Performed on grey-level images. Based on user defined window size, 2d smoothing with an averaging kernel is performed.

![Original image](images/mars.jpg) ![Image with 2D smooth](images/2d_smooth.jpg)

8. 1d_smooth: Performed on grey-level images. Based on user defined window size, 1d incremental smoothing with an averaging kernel is performed.

![Original image](images/mars.jpg) ![Image with 1D smooth](images/1d_smooth.jpg)

9. grey_level_stretching: Performed on grey-level images. Applies histogram stretching using user defined a and b values where a and b are the original minimum and maximum values to stretch from. 
The operation also outputs two histogram images: 
	* outputB: output is the output file name and B stands for before. 
	* outputA: A stands for after. 

![Original image](images/mars.jpg) ![Image with grey_level_stretching](images/grey_level_stretching.jpg)

![Histogram Before](images/grey_level_stretchingB0.jpg) ![Histogram Before](images/grey_level_stretchingB1.jpg)

![Histogram After](images/grey_level_stretchingA0.jpg) ![Histogram After](images/grey_level_stretchingA1.jpg) 

10. threshold_stretching: Performed on grey-level images. Segments the image into foreground and background using a user defined threshold value and then applies histogram stretching on the segments individually.

![Original image](images/mars.jpg) ![Image with threshold_stretching](images/threshold_stretching.jpg)

11. rgb_stretching: Performed on color images. Applies histogram stretching on all 3 (r,g,b) channels using user defined a and b values where a and b are the original minimum and maximum values to stretch from. 

![Original image](images/mars.jpg) ![Image with rgb_stretching](images/rgb_stretching.jpg)

12. hsi_stretching: Performed on color images. Applies histogram stretching on the I channel in the HSI color space using user defined a and b values where a and b are the original minimum and maximum values to stretch from.

![Original image](images/mars.jpg) ![Image with hsi_stretching](images/hsi_stretching.jpg)

13. sobel_gradient: Performed on grey-level images. Applies the sobel operator on the image based on the window size of 3 or 5.

![Original image](images/mars.jpg) ![Image with sobel_gradient](images/sobel_gradient.jpg)

14. sobel_gradient_threshold: Performed on grey-level images. Applies the sobel operator on the image based on the window size of 3 or 5 followed by threshold based binarization.

![Original image](images/mars.jpg) ![Image with sobel_gradient_threshold](images/sobel_gradient_threshold.jpg)

15. sobel_gradient_threshold_direction: Performed on grey-level images. Applies the sobel operator on the image based on the window size of 3 or 5 followed by threshold based binarization. The function then outputs the gradients that have the angles between the user defined range.

![Original image](images/mars.jpg) ![Image with sobel_gradient_threshold_direction](images/sobel_gradient_threshold_direction.jpg)

16. HSI_sobel: Performed on color images. Applies the sobel operator on the intensity channel of the HSI color space based on the window size of 3 or 5 followed by threshold based binarization and direction based thresholding. 
The function outputs 3 images:
	* output: The gradient image.
	* outputB: The thresholded image.
	* outputD: The direction thresholded image.

![Original image](images/mars.jpg) ![Image with HSI_sobel](images/HSI_sobel.jpg)

![Binarized image](images/HSI_sobel_B.jpg) ![Direction thresholded](images/HSI_sobel_D.jpg)

17. cv_sobel: Performed on grey-level and color images. Converts the image to a grey-level image and applies the sobel operator. Outputs the binarized version of the gradient image based on the threshold value provided by the user.

![Original image](images/mars.jpg) ![Image with cv_sobel](images/cv_sobel.jpg) ![Binarized image](images/cv_sobel_B.jpg)

18. cv_canny: Performed on grey-level and color images. Converts the image to a grey-level image and applies the canny operator using the user defined threshold values where threshold1 < threshold2.

![Original image](images/mars.jpg) ![Image with cv_canny](images/cv_canny.jpg)

19. cv_grey_hist_stretch: Performed on grey-level images. Applies histogram stretching on grey-level images.

![Original image](images/mars.jpg) ![Image with cv_grey_hist_stretch](images/cv_grey_hist_stretch.jpg)

20. cv_grey_hist_eq: Performed on grey-level images. Applies histogram equalization on grey-level images.

![Original image](images/mars.jpg) ![Image with cv_grey_hist_eq](images/cv_grey_hist_eq.jpg)

21. cv_HSV_hist_eq: Performed on color images. Applies histogram equalization on user defined channels in the HSV color space. 
Example channel input: HS (This will apply histogram equalization on the hue and saturation channels.)

![Original image](images/mars.jpg) ![Image with cv_HSV_hist_eq](images/cv_HSV_hist_eq.jpg)

22. cv_hist_eq_canny: Performed on grey-level and color images. Converts the image to a grey-level image, applies histogram equalization followed by the canny operator.

![Original image](images/mars.jpg) ![Image with cv_hist_eq_canny](images/cv_hist_eq_canny.jpg)

6. cv_hist_eq_sobel: Performed on grey-level and color images. Converts the image to a grey-level image, applies histogram equalization followed by the sobel operator.
The function outputs 2 images:
	* output: The gradient image.
	* outputB: The thresholded image.

![Original image](images/mars.jpg) ![Image with cv_hist_eq_sobel](images/cv_hist_eq_sobel.jpg) ![Thresholded image](images/cv_hist_eq_sobel_B.jpg)

7. scan_code: Performed on grey-level and color images. Utilizes the QRCodeDetector class in OpenCV to detect and decode QR codes.