## Cement Classification

*Author:* Alexandre Romagnolli Gonçalves

*Date:* June 1, 2023

*Abstract:* The dosage of materials is a vital factor in constructing safe civil structures and maintaining public safety. In particular, the properties of final samples, in both fresh and hardened states, are significantly influenced by the characteristics and mix proportion of materials used in concrete traces. Traditionally, the identification of concrete traces has been a manual process carried out by human experts, which can be subject to physical and subjective influences. Furthermore, researchers often find it challenging to access representative, reliable, and consistent databases. Therefore, the development of an automated system to identify concrete traces is a promising research direction. In this context, this study addresses these issues by introducing a unique database composed of images from two distinct classes of concrete traces; specificaly, our goal is to implement image preprocessing techniques on a concrete traces dataset for data augementation, to train different achitectures for classifying these images into two (binary) classes, and to evaluate the performance of the obtained models. Concerning the architectures of the DNNs, we considered 

1. **Proposed Model:** A custom model built for high accuracy, comprising several Conv2D, BatchNormalization, MaxPooling2D, and Dense layers, along with Dropout for regularization.

2. **InceptionV3 (Transfer Learning):** This model employs the pre-trained InceptionV3 as a base, retaining its learned weights while adding extra Flatten and Dense layers for task-specific learning.

3. **VGG16 (Transfer Learning):** This model utilizes the pre-trained VGG16 as its base, with added Flatten and Dense layers.

Upon evaluating the models' performance, we found that the "Proposed model" achieved the highest F1-score at 93.22%, reflecting a robust balance of precision and recall, and demonstrating its superior performance in classifying the cement images; on the other hand, the transfer learning models, derived from the "InceptionV3" and "VGG16", achieved lower F1-scores at 82.97% and 80.31% respectively, indicating that they were less effective for this specific classification task.

For downloading the pre-processed dataset, refer to: http://lapse.td.utfpr.edu.br/downloads/dataset_cement_classification.zip
