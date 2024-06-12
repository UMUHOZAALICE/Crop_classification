## Crop_classification usinf Remote sensing Data
# Abstact
This study aims to address the challenge of crop classifiication in Rwanda using Rwanda Remote sensing data to classify different crop types such as banana, legumes, forests, etc. It uses using deep learning model combined with transfer learning using VGG 16 due to its effectiveness in image recognition tasks. the purpose of this study is to enhance the agricultural monitoring in form of farm management and resource allocation under accurate identification of these crops wth the se deep learning models. Thwe model were trained and tested with the promising result of about 95% accuracy. This finding highlights the potential of deep learning for precision agriculture in Rwanda. Providing accurate crop classification will potentially improve agriculture productivity with farm management optimization and resource allocation. This study contibutess to the integration of technology with traditional farming thereby enhancing accuracy and sustainablity through image based learning. The findings offer insights into agricultural productivity and sustainability, benefiting policymakers, MINAGRI, and researchers working towards agricultural advancements in Rwanda. RTI Rwanda crop-type dataset were used which consists of 6 classes for crops: forest, banana, other, structure, legumes and maize.
# Exploratory Data Analysis
This study adopts quantitave analysis method with remote sensing data to evaluate the effectiveness of deep earnign models in crop classification. The dataset, sourced from Research Triangle Institute (RTI) International, features remote sensing data captured via drones. It includes 5161 training images and 1290 validation images across six crop categories: banana, maize, legumes, structure, forest, and others. Each image in the training and validation datasets was recorded in a DataFrame with corresponding labels.
Given the limited size of the dataset, data preprocessing and augmentation were essential. We used TensorFlow’s Keras ImageDataGenerator class for augmenting training data batches. Techniques like Mixup, and CutMix, Rotation, Zooming, and Flips were used to artificially expand the dataset size, enhancing the model’s robustness and generalization capabilities. This step is critical in addressing the small dataset size and preventing overfitting.
# Model selection, optimization and training
The model selected is the VGG-16 architecture, a 16-layer convolutional network, pretrained on ImageNet, and is fine tuned for our specific classification task, incorporating a feed-forward network with a fully connected layer, dropout layer, and a SoftMax output layer. This model comprises 13 convolutional layers for feature extraction and pooling layers for dimension reduction, ending in three fully connected layers for output classification. It has a total of approximately 138 million parameters. The Adam optimizer and categorical crossentropy loss function were used. The training process was conducted over approximately 100 epochs with a batch size of 128 images and a learning rate of 0.0001.
# Experiment result
After model being trained and validated, it was evaluated and to avoid bias F1 score were used with 87% accuracy. Noteworthy excellence is observed in the Banana, Forest, and Maize classes, each exhibiting F1 scores surpassing 90%. Although the remaining crop classes demonstrate relatively lower F1 scores ranging from 0.52 to 0.87, the model’s effectiveness remains evident across the entire variety of classifications, underscoring its robustness and adaptability in diverse agricultural contexts.
# Conclusion
In conclusion, the model exhibits commendable performance, particularly excelling in the identification of 'Banana','Forest', and 'maize'. The macro averages for precision, recall, and F1-score, around 0.90, indicate good overall performance. However, attention to classes with lower F1 scores,
such as ’Legumes,’ is essential for future enhancements. The weighted averages, influenced by classes with more samples, highlight the model’s effectiveness in handling larger datasets. Despite specific areas for improvement, the project establishes a solid foundation for the application of deep learning in precision agricultural, with promising prospects for further refinement and expansion.
# Reference
1. J. Dhakshayani, S. S. Kulkarni, A. Mahapatra, B. Surendiran, and M. K. Nath, ‘Weed Classifica-
tion from Paddy Crops Using Convolutional Neural Network’, in Proceedings of the International
Conference on Paradigms of Communication, Computing and Data Sciences, M. Dua, A. K. Jain, A.
Yadav, N. Kumar, and P. Siarry, Eds., in Algorithms for Intelligent Systems. Singapore: Springer,
2022, pp. 493–507. doi: 10.1007/978-981-16-5747-4
2. ‘Beginners Guide to VGG16 Implementation in Keras | Built In’. Accessed: Nov. 14, 2023.
[Online]. Available: https://builtin.com/machine-learning/vgg16



