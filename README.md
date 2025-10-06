# BASIC-IMAGE-TRANSFORMATION


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br> Read the color image using imread().

### Step2:
<br> Print the image using imshow().

### Step3:
<br> Perform Translation, Scaling, Shearing on the image.

### Step4:
<br> And perform Reflection, Rotation, Cropping on the image.

### Step5:
<br> Display the output.

## Program:
```
Developed By: YUVARAJ V
Register Number: 212223230252
```

```python
i)Image Translation

tx, ty = 100, 200  # Translation factors (shift by 100 pixels horizontally and 50 vertically)
M_translation = np.float32([[1, 0, tx], [0, 1, ty]])  # Translation matrix: 

translated_image = cv2.warpAffine(image, M_translation, (2636, 1438))


ii) Image Scaling

fx, fy = 2.0, 1.0  
scaled_image = cv2.resize(image, None, fx=fx, fy=fy, interpolation=cv2.INTER_LINEAR)


iii)Image Shearing

shear_matrix = np.float32([[1, 0.5, 0], [0.5, 1, 0]])  
sheared_image = cv2.warpAffine(image, shear_matrix, (2636, 1438))


iv)Image Reflection

reflected_image = cv2.flip(image, 2)



v)Image Rotation

(height, width) = image.shape[:2]                                   # Get the image height and width
angle = 45                                                          # Rotation angle 
center = (width // 2, height // 2)  
M_rotation = cv2.getRotationMatrix2D(center, angle, 1)  

rotated_image = cv2.warpAffine(image, M_rotation, (width, height))  # Apply rotation



vi)Image Cropping

x, y, w, h = 0, 0, 2200, 1550  

cropped_image = image[y:y+h, x:x+w] 



```
## Output:

### Original image
<img width="667" height="405" alt="image" src="https://github.com/user-attachments/assets/5e8bcf85-a7d4-473b-985e-86badc55989d" />


### i)Image Translation
<img width="696" height="512" alt="image" src="https://github.com/user-attachments/assets/d9950dc8-dadc-4c7a-a9c6-d63dcbd0d0e6" />



### ii) Image Scaling
<img width="703" height="245" alt="image" src="https://github.com/user-attachments/assets/e35c9875-c3bb-4ff1-b572-05233c374fd4" />




### iii)Image shearing
<img width="696" height="499" alt="image" src="https://github.com/user-attachments/assets/572d721f-0dea-4681-8ec0-33c3ae65d5b3" />



### iv)Image Reflection
<img width="1269" height="407" alt="image" src="https://github.com/user-attachments/assets/21f2d786-958e-40ab-bcb3-7cb468540b13" />



### v)Image Rotation
<img width="689" height="415" alt="image" src="https://github.com/user-attachments/assets/e8a405c8-1de2-4bad-81a6-9fc4a0a98977" />




### vi)Image Cropping
<img width="1299" height="510" alt="image" src="https://github.com/user-attachments/assets/6caae5a3-2a43-47d1-ada4-5532355a024a" />




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
