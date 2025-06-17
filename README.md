# Plant-Leaf-Disease-Detection-using-ResNet

In India, approximately 70% of the population relies on agriculture for their livelihood. However, a major challenge that farmers face is selecting the appropriate crops and identifying effective fertilizers or pesticides for their plants. Traditionally, crop disease identification has relied on the farmer's ability to visually inspect leaves and recognize symptoms. This manual method is highly dependent on experience and can often lead to misdiagnosis or delayed treatment.

The aim of this project is to automate the process of identifying plant leaf diseases using deep learning techniques. By doing so, farmers can benefit from timely and accurate disease diagnosis, enabling them to take the right steps for treatment, improve yield, and avoid unnecessary chemical usage.

Detecting plant diseases at an early stage is critical. It not only helps in preventing the spread of the disease to healthy crops but also contributes to increased agricultural productivity and sustainability. Effective disease management can reduce reliance on harmful pesticides, protect the environment, and contribute significantly to food security, particularly in countries with large agrarian populations like India.

## Dataset
The dataset used in this project comprises 70,200 images of healthy and diseased leaves. These images span 38 distinct classes, representing various diseases and healthy states across different plant species. 

The plant types included in the dataset are: Apple, Blueberry, Cherry, Corn, Grape, Orange, Peach, Bell Pepper, Potato, Raspberry, Soybean, Squash, Strawberry, and Tomato.

![image](https://github.com/user-attachments/assets/c5a5437e-0c89-4dcf-8ab4-e18366ebd98c)

Each class corresponds to either a specific disease (e.g., leaf spot, rust, blight) or a healthy condition for a particular plant. This makes the dataset highly diverse and suitable for robust image classification tasks.

### The dataset is split into:
### Training set (70%)
### Test/Validation set (30%)

To perform image classification, we use the ResNet-9 architecture — a variant of the Residual Network, which revolutionized deep learning in computer vision. ResNet-9 is particularly suitable for this task due to its balance between depth and efficiency. It comprises 9 layers, including 5 residual blocks, and utilizes shortcut connections to ensure better gradient flow and feature retention. These shortcuts help avoid the degradation problem commonly encountered in deeper networks by allowing inputs from earlier layers to skip ahead, preserving essential features.

![image](https://github.com/user-attachments/assets/be7bd135-2ec1-4e45-9dc1-ee4bfda279c2)

ResNet-9 also includes convolutional layers for feature extraction, batch normalization for stable training, ReLU activations, max pooling for spatial downsampling, and a fully connected layer for classification. The model is initially pretrained on the ImageNet dataset (which includes 1,000 object classes) and then fine-tuned on our specific dataset to enhance performance on plant disease identification.

## Model Training & Evaluation

During training, the model undergoes multiple epochs where its performance is evaluated on both training and validation datasets. Below are detailed results from the initial epochs:

Epoch 0:

Learning Rate: 0.00812

Training Loss: 0.7506

Validation Loss: 0.8232

Validation Accuracy: 76.35%

![image](https://github.com/user-attachments/assets/f078b0b6-edc1-4c7b-8811-47532407335c)

Epoch 1:

Learning Rate: 0.00000 (adjusted using a learning rate scheduler)

Training Loss: 0.1233 — a substantial decrease indicating better model fit

Validation Loss: 0.0283 — significant improvement in generalization

Validation Accuracy: 99.20% — excellent performance, showing high accuracy in disease prediction

These results demonstrate that the model quickly converges and learns to distinguish between different leaf conditions effectively.

## Conclusion

These outcomes indicate that the model quickly learned meaningful patterns and generalized well to unseen data. The sharp drop in both training and validation losses, along with the substantial increase in accuracy — **achieving 99.2% validation accuracy** — confirms the model's effectiveness in classifying plant diseases with high precision.

In summary, the application of deep learning in plant disease detection offers a powerful tool for modern agriculture. With models like ResNet-9, farmers can gain rapid and accurate insights into crop health, reduce dependency on manual inspection, and make informed decisions. This not only supports agricultural productivity but also contributes to environmental preservation and global food security.
