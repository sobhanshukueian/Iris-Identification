# Iris-dataset-preprocessing
The goal of this project is preprocessing the iris dataset for the identification task; some methods like edge detection, hough transform, and daugman normalization are used in this project.

Dataset Images are look like below image:

![001L_3](https://user-images.githubusercontent.com/47561760/177047425-4b953918-a6ee-495a-9e2b-01ad44e1800b.png)


For the Hough Transform algorithm, it is crucial to perform edge detection first to produce an edge image which will then be used as input into the algorithm; so first of all, I applied edge detection to the images to find edges and better view of circles in the images; so to do that, followed the below steps : 
1.gaussian blur
2.Sobel filter
3.non_max suppression
4.threshold
5.hysteresis

Before edge detection :

![6b8c6bda-7088-4a2f-936d-db13030bde89](https://user-images.githubusercontent.com/47561760/177048531-39c5ec27-b3d2-47d5-88d0-ef255aa22ba5.png)

After edge detection : 

![043ccca8-3565-49c3-9f91-d0a0fd52b53f](https://user-images.githubusercontent.com/47561760/177048522-77cef3c7-592f-4eb3-b8c8-4dae43bbb6e0.png)

After applying edge_detection, I implemented my custom hough transform algorithm to find circles in image.

## Hough Transform ##
The transform effectively searches for objects with a high degree of radial symmetry, with each degree of balance receiving one “vote” in the search space. By exploring a 3D Hough search space, the transform can measure the centroid and radius of each circular object in an image.

Some points in this implementation helped to have better speed and fewer computations, for example : 
*  Numpy broadcasting and vectorizing
*  Do some computations out of the loop
*  R and (a,b) range
*  Compute just for edges

## Normalization ## 
The homogeneous rubber sheet model, described by Daugman , assigns to each point on the iris, regardless of its size and pupillary dilation, a pair of real coordinates (r, θ), where radial variable r is in range [0, 1], and angle θ is in range [0, 2π]. The normalization process generates iris regions of the same constant dimensions, so that two images of the same iris captured under different conditions have the characteristic features at the same spatial locations. 

![image](https://user-images.githubusercontent.com/47561760/177047389-55423f8a-81d6-441b-a4e2-8feb4ad130ce.png)

## Results ## 
### 1 ###
![6dff3b59-eace-4994-af9e-63abf1b48bcf](https://user-images.githubusercontent.com/47561760/177048545-8977db16-8f71-4ae9-8c24-2419fdc4a229.png)

### 2 ###
![677d1077-be49-4aa4-9df4-fd29a1b98fc9](https://user-images.githubusercontent.com/47561760/177048693-f3a3003c-e5f0-4dd7-bc9b-9316e7e27fb5.png)

### 3 ###
![7d971e5f-eb04-4de5-9762-bedd4cd838e1](https://user-images.githubusercontent.com/47561760/177048723-4877121a-a537-40a1-9eee-a04593d6ba84.png)



