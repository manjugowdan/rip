Develop a program TO PERFORM Linear Transformation on a image.

import cv2
 
img = cv2.imread('E:letteRm.jpg')
(h, w) = img.shape[:2
                    ]
# calculate the center of the image
center = (w / 2, h / 2)
 
angle90 = 90
angle180 = 180
angle270 = 270
 
scale = 1.0
 
M = cv2.getRotationMatrix2D(center, angle90, scale)
rotated90 = cv2.warpAffine(img, M, (h, w))

M = cv2.getRotationMatrix2D(center, angle180, scale)
rotated180 = cv2.warpAffine(img, M, (w, h))
 
M = cv2.getRotationMatrix2D(center, angle270, scale)
rotated270 = cv2.warpAffine(img, M, (h, w))
 
 
cv2.imshow('Original Image',img)
cv2.waitKey(0) 
cv2.destroyAllWindows()
 
cv2.imshow('90 degree',rotated90)
cv2.waitKey(0) 
cv2.destroyAllWindows() 
 
cv2.imshow('180 degree',rotated180)
cv2.waitKey(0) 
cv2.destroyAllWindows() 
 
cv2.imshow('270 degree',rotated270)
cv2.waitKey(0)
cv2.destroyAllWindows()

![image](https://user-images.githubusercontent.com/96232756/148197569-e04017eb-2e0f-4bf4-8397-b3a85417881f.png)
![image](https://user-images.githubusercontent.com/96232756/148197616-a6cfe7ce-b9fd-43c1-bb92-79f6aabd1c2a.png)
![image](https://user-images.githubusercontent.com/96232756/148197758-e23743f3-82b2-46c8-95e5-a9fff63d2be9.png)
![image](https://user-images.githubusercontent.com/96232756/148197795-80167b72-40b9-4a80-86d7-c5130ca4ece4.png)



