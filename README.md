# Plant-Leaf-Disease-Detection-using-ResNet
Introduction
In India, approximately 70% of the population relies on agriculture for their livelihood. However, farmers often face challenges in selecting the right crops and identifying the appropriate pesticides or fertilizers for their plants. Traditionally, disease detection in crops is performed manually through visual inspection by the farmer. This approach is not only time-consuming but also highly dependent on the individual's experience and knowledge, which may lead to incorrect or delayed diagnoses.

The goal of our project is to automate the process of plant disease detection by analyzing images of plant leaves using deep learning techniques. This system will assist farmers in identifying crop diseases early, allowing them to take timely and informed actions, ultimately improving crop yield and minimizing losses.

Motivation
Plant leaf disease detection is a critical research area with significant implications in agriculture. Early and accurate identification of plant diseases can help in:

Preventing the spread of diseases across crops,

Enhancing productivity by minimizing damage,

Reducing excessive use of pesticides, leading to better environmental sustainability,

Supporting global food security, particularly in regions heavily dependent on agriculture.

By leveraging computer vision and deep learning, we can automate the disease diagnosis process, making it faster, scalable, and accessible even to those with limited agricultural expertise.

Dataset
The dataset used in this project comprises 70,200 images of healthy and diseased leaves. These images span 38 distinct classes, representing various diseases and healthy states across different plant species. The plant types included in the dataset are:

Apple, Blueberry, Cherry, Corn, Grape, Orange, Peach, Bell Pepper, Potato, Raspberry, Soybean, Squash, Strawberry, and Tomato.

Each class corresponds to either a specific disease (e.g., leaf spot, rust, blight) or a healthy condition for a particular plant. This makes the dataset highly diverse and suitable for robust image classification tasks.

The dataset is split into:

Training set (70%)

Test/Validation set (30%)

The directory structure is preserved to allow class-wise mapping during model training and evaluation.

Methodology
We employ ResNet-9, a convolutional neural network (CNN) architecture, for image classification. Introduced in 2015, Residual Networks (ResNets) represent a significant advancement in deep learning for computer vision. They solve the vanishing gradient problem, allowing for deeper architectures by using shortcut (residual) connections.

ResNet-9 Architecture Highlights:

Composed of 9 layers,

Contains 5 residual blocks,

Utilizes shortcut connections to retain and forward essential features,

Incorporates convolutional layers, batch normalization, ReLU activation, max pooling, and fully connected layers,

Pretrained on ImageNet, capable of classifying up to 1,000 object categories,

Fine-tuned for plant leaf disease classification using transfer learning.

This architecture enables the model to learn high-level features from images and generalize well to unseen data.

Model Training & Evaluation
During training, the model undergoes multiple epochs where its performance is evaluated on both training and validation datasets. Below are detailed results from the initial epochs:

Epoch 0:

Learning Rate: 0.00812

Training Loss: 0.7506

Validation Loss: 0.8232

Validation Accuracy: 76.35%

Epoch 1:

Learning Rate: 0.00000 (adjusted using a learning rate scheduler)

Training Loss: 0.1233 — a substantial decrease indicating better model fit

Validation Loss: 0.0283 — significant improvement in generalization

Validation Accuracy: 99.20% — excellent performance, showing high accuracy in disease prediction

These results demonstrate that the model quickly converges and learns to distinguish between different leaf conditions effectively.
![image](https://github.com/user-attachments/assets/f078b0b6-edc1-4c7b-8811-47532407335c)


Conclusion
This project showcases how deep learning can revolutionize agriculture by automating the process of plant disease detection. The use of ResNet-9 enables high accuracy in classifying diseases across a variety of crops. Our system provides:

Fast, reliable disease identification,

Minimized crop losses,

Reduced dependence on manual inspection,

Support for sustainable agriculture practices.

The approach holds great promise in aiding farmers with limited access to expert knowledge, thereby enhancing decision-making in crop management and promoting food security.
