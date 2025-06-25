# Computer-Vision
Overview
This assignment is about using deep learning to classify 101 types of food images and labels. I am going to train 3 pre-trained models which are GoogleNet, MobileNetV3 and Resnet 50 on the Food-101 dataset. It is composed of 101,000 images of food with 101 different classes. For each class, 250 manually reviewed test images are provided as well as 750 training images. All images were rescaled to have a maximum side length of 512 pixels. In part A, my objective is to train 3 pre-trained models and compare their results. The pre-trained models are GoogLenet, MobileNet V3 and ResNet under the conditions of replacing the model head and freezing pre-trained layers. Part B, My task is to pick the best pre-trained model from Part A and fine-tune it on the Food101 Dataset. I will experiment with unfreezing on at least 2 different layers of the model.

Architectures Used for Transfer Learning
In this report, three well-established convolutional neural network (CNN) architectures were employed to perform transfer learning on the Food101 dataset: GoogLeNet, ResNet, and MobileNetV3. Each model represents a significant advancement in deep learning architecture design, with distinct innovations and use-case strengths. This section presents an overview of these architectures, outlining their key components, historical relevance, and suitability for transfer learning.
1. GoogLeNet (Inception v1)
GoogLeNet, introduced by Google in 2014, marked a major shift in CNN architecture by emphasizing both computational efficiency and accuracy. It achieved first place in the ILSVRC-2014 classification challenge.
-	 Depth: 22 layers
-	 Key Innovation: Inception modules, which apply multiple convolution operations (1×1, 3×3, 5×5) in parallel within the same layer and concatenate their outputs.
-	 Parameters: ~6.8 million
-	 Additional Features: Auxiliary classifiers to combat vanishing gradients during training.
-	 Strength: Achieves a balance between performance and parameter efficiency.
-	 GoogLeNet was among the first to demonstrate that wider, more structured networks could outperform deeper traditional CNNs while keeping computational costs low.
2. ResNet (Residual Network)
ResNet, developed by Microsoft Research in 2015, introduced the concept of residual learning, which significantly alleviated the vanishing gradient problem in deep networks.
-	 Depth: Varies (ResNet50 includes 50 layers)
-	 Key Innovation: Residual (skip) connections, allowing layers to learn modifications (F(x)) to the identity function (x) rather than the full transformation.
-	 Parameters: ~25 million (ResNet50)
-	 Strength: Allows training of very deep networks with improved convergence and generalization.
ResNet was a breakthrough architecture, winning ILSVRC-2015 and becoming a foundational model in both academic research and industry applications.
3. MobileNetV3
MobileNetV3, released by Google in 2019, is a highly efficient model designed for low-latency and mobile applications. It integrates both manual design principles and neural architecture search (NAS) techniques.
-	 Depth: Lightweight with ~5.4 million parameters (MobileNetV3-Large)
-	 Key Innovation: Combines depthwise separable convolutions, Squeeze-and-Excitation (SE) blocks, and swish-like activation functions (h-swish)
-	 Strength: Excellent trade-off between speed and accuracy, optimized for mobile and edge devices.
MobileNetV3 is ideal for real-time and resource-constrained environments while maintaining competitive accuracy levels in image classification tasks.
