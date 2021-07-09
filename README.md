# fov_alignment
fov alignment between event camera and RGB camera

1. Assume that the scene is infinitely far away
2. Compute the projection matrix that maps a pixel coordinate of the left event camera to the pixel coordinate in the left global shutter camera:

![image](https://user-images.githubusercontent.com/35663368/125096779-6bd85c80-e110-11eb-8502-3c6c60eacc67.png)

3. Compute this mapping for each pixel of the left event camera frame (make sure to normalize the homogeneous vector before retrieving the pixel coordinates)
4. Use opencv's remap function to remap the left image pixels to the left event camera pixels
