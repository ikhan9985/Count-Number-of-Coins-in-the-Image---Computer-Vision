# Count-Number-of-Coins-in-the-Image---Computer-Vision
Count Number of Coins in the Image - Computer Vision


This code detects coins in an input image using OpenCV.

The image is first loaded using cv2.imread() function and converted to grayscale using cv2.cvtColor(). Gaussian blur is applied to the grayscale image using cv2.GaussianBlur() to reduce noise, and then the Canny edge detection algorithm is applied to the blurred image using cv2.Canny().

The edges of the image are then passed to cv2.findContours() to detect the contours. The contours are filtered to keep only the outermost contours using the is_inside_contour() function. This function checks if a contour is fully contained inside another contour and returns True if it is fully contained, otherwise False. If a contour is fully contained inside another contour, it is filtered out.

The filtered contours are then drawn on the original image using cv2.drawContours() function in green color, and the number of detected coins is printed. The resulting image is displayed using cv2.imshow().
