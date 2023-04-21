<h1 align="center">Iris Dataset Identification Project </h1>

<p align="center">
<img src="https://user-images.githubusercontent.com/47561760/233600046-b99b5d92-7b43-43be-a922-7277a55b37f7.gif" alt="your-gif" width="200" height="200" />
</p>


<p align="center">
This project is an implementation of iris dataset identification using edge detection, Hough transform, and Daugman normalization. We also employ a Siamese network with contrastive loss for identification.
</p>

## 📝 Overview

Our implementation follows the following steps:

1. 🎨 Data preprocessing: We preprocess the iris dataset using edge detection, Hough transform, and Daugman normalization to enhance the images and prepare them for identification.

2. 🤖 Siamese network: We implement a Siamese network for identification, using contrastive loss to train the network.

3. 📈 Visualization and Results: We present the results of our identification model, including accuracy and comparison with other methods.

## 🎨 Data Preprocessing

In order to enhance the iris images for identification, we employ three methods: edge detection, Hough transform, and Daugman normalization.

### 🖼️ Edge Detection

We use Canny edge detection to extract the edges of the iris image, which can help to remove noise and enhance the features of the iris.

### 🌀 Hough Transform

We use the Hough transform to detect the circular shape of the iris, which is important for accurate identification.
### 📣 Note
I implemented the hough transform algorithm using Numpy broadcasting and vectorizing, also by some modifications could achieve better speed and lower computations.


### 🌀 Daugman Normalization

I use Daugman normalization to transform the iris image into a polar representation, which makes it easier to compare with other iris images.

## 🤖 Siamese Network

We implement a Siamese network for identification, which takes in two iris images and outputs a similarity score. We use contrastive loss to train the network, which helps to optimize the similarity scores.

## 🚀 Future works and get started

Consider that I didn't train classifer on the learned representations by siamese you can use this repository to preprocess and learn representations of your dataset and by training a classifier get better results. 

To get started with our iris dataset identification project, follow these steps:

1. 🔗 Clone this repository: `https://github.com/sobhanshukueian/Iris-Identification.git`
2. 🖼️ Run the preprocessing: `preprocess.ipynb`
3. 🤖 Train the Siamese network: `Siamese Identification.ipynb`

## 📊 Visualization and Results (After 15 epochs training)

We visualize the iris images before and after preprocessing, as well as examples of the Siamese network's similarity scores. 

### Iris Images Before and After Preprocessing

![image](https://user-images.githubusercontent.com/47561760/233605745-d21eb9b6-a2dc-4292-9ab6-0b47c7966640.png)

### Siamese Networks Euclidean distances

<p align="center">
  <img width="800" height="300" src="https://user-images.githubusercontent.com/47561760/233616066-2619b1b0-a7c5-41f1-8701-40bdf4e78f92.png">
</p>

### Embeddings of dimensions
<p align="center">
  <img width="800" height="300" src="https://user-images.githubusercontent.com/47561760/233616549-b4d7148c-d0ce-402b-a14e-fa1404e16fa0.png">
</p>

<p align="center">
  <img width="800" height="300" src="https://user-images.githubusercontent.com/47561760/233616451-f7b205ad-2215-4816-9262-3549a8021a62.png">
</p>

♾️

<p align="center">
  <img width="800" height="300" src="https://user-images.githubusercontent.com/47561760/233616999-f88ff6e6-ddbc-4505-8274-9fc1280d0b54.png">
</p>

### Results without using classifier

<p align="center">
  <img width="800" height="300" src="https://user-images.githubusercontent.com/47561760/233616805-df2e263e-0f40-4720-aa3c-53cd385d88f1.png">
</p>



# ⭐️ Please Star This Repo ⭐️

If you found this project useful or interesting, please consider giving it a star on GitHub! This helps other users discover the project and provides valuable feedback to the maintainers.

Thank you for your support!
