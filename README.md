# Iris-dataset-preprocessing
The goal of this project is preprocessing the iris dataset for the identification task; some methods like edge detection, hough transform, and daugman normalization are used in this project.

Dataset Images are like below:

![001L_3](https://user-images.githubusercontent.com/47561760/177047425-4b953918-a6ee-495a-9e2b-01ad44e1800b.png)


For the Hough Transform algorithm, it is crucial to perform edge detection first to produce an edge image which will then be used as input into the algorithm; so first of all, I applied edge detection to the images to find edges and better view of circles in the images; so to do that, followed the below steps : 
*	  gaussian blur
*	  Sobel filter
*	  non_max suppression
* 	threshold
*	  hysteresis
After applying edge_detection, I implemented my custom hough transform algorithm to find circles in image.

## Hough Transform ##
The transform effectively searches for objects with a high degree of radial symmetry, with each degree of balance receiving one “vote” in the search space. By exploring a 3D Hough search space, the transform can measure the centroid and radius of each circular object in an image.

Some points in this implementation helped to have better speed and fewer computations, for example : 
*	Numpy broadcasting and vectorizing
*	Do some computations out of the loop
*	R and (a,b) range
*	Compute just for edges

![image](https://user-images.githubusercontent.com/47561760/177048003-8c867dbd-140a-4573-8bfe-e0346a78cd4f.png)


## Normalization ## 
The homogeneous rubber sheet model, described by Daugman , assigns to each point on the iris, regardless of its size and pupillary dilation, a pair of real coordinates (r, θ), where radial variable r is in range [0, 1], and angle θ is in range [0, 2π]. The normalization process generates iris regions of the same constant dimensions, so that two images of the same iris captured under different conditions have the characteristic features at the same spatial locations. 

![image](https://user-images.githubusercontent.com/47561760/177047389-55423f8a-81d6-441b-a4e2-8feb4ad130ce.png)

