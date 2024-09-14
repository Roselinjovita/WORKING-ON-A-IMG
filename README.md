# WORKIN ON A IMG WORKSHOP
#### NAME : ROSELIN MARY JOVITA.S
#### REG NO:  212222230122

# PROGRAM
```
pip install opencv-contrib-python
import cv2
image1 = cv2.imread('nobi.jpg')
image2 = cv2.imread('dor.jpg')
image1.shape
image2.shape
# Resize both images to the desired size (530, 412)
new_size = (500, 530)  # (width, height)
image1_resized = cv2.resize(image1, new_size)
image2_resized = cv2.resize(image2, new_size)
height,width,c=image1.shape
row_mid=265
col_mid=250
# Split the image into 4 regions using row and column coordinates
R1 = image1_resized[0:row_mid, 0:col_mid]      # Top-left region
R2 = image1_resized[0:row_mid, col_mid:width]  # Top-right region
R3 = image1_resized[row_mid:height, 0:col_mid] # Bottom-left region
R4 = image1_resized[row_mid:height, col_mid:width] # Bottom-right region
R5 = image2_resized[0:row_mid, 0:col_mid]      # Top-left region
R6 = image2_resized[0:row_mid, col_mid:width]  # Top-right region
R7 = image2_resized[row_mid:height, 0:col_mid] # Bottom-left region
R8 = image2_resized[row_mid:height, col_mid:width] # Bottom-right region
#Splitting the Image Using Coordinates:

#R1: Top-left region ([0:265, 0:206])
#R2: Top-right region ([0:265, 206:413])
#R3: Bottom-left region ([265:531, 0:206])
#R4: Bottom-right region ([265:531, 206:413])

# Save the regions as separate images
cv2.imwrite('R1.jpg', R1)
cv2.imwrite('R2.jpg', R2)
cv2.imwrite('R3.jpg', R3)
cv2.imwrite('R4.jpg', R4)
cv2.imwrite('R5.jpg', R5)
cv2.imwrite('R6.jpg', R6)
cv2.imwrite('R7.jpg', R7)
cv2.imwrite('R8.jpg', R8)
# Optionally, display the regions (for verification)
cv2.imshow('R1', R1)
cv2.imshow('R2', R2)
cv2.imshow('R3', R3)
cv2.imshow('R4', R4)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imshow('R5', R5)
cv2.imshow('R6', R6)
cv2.imshow('R7', R7)
cv2.imshow('R8', R8)
cv2.waitKey(0)
cv2.destroyAllWindows()
image1_resized[0:row_mid, 0:col_mid] = R5
image2_resized[row_mid:height, col_mid:width] = R4
# Display the resized images
cv2.imshow('Resized Image 1', image1_resized)
cv2.imshow('Resized Image 2', image2_resized)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# OUTPUT

![WORKING ON AN IMG](https://github.com/user-attachments/assets/0224c869-e186-410d-89c3-6f7195f3902d)


# RESULT
Thus the program has been successfully executed.

