# CS 455 Final Project - UG7
## Identifying AI-Generated Images using a Convolutional Neural Network (CNN)
Angelina Buysse, Austin Rollfing, Pranav Ramasahayam, William Reimer

### Project Summary
Due to the recent fast paced evolution of Artificial Intelligence (AI) and its ability to create digital media, there is a need for better methodology to determine whether an image is real or artificially generated. As AI has become more sophisticated and accessible, there has been a proliferation of high quality deep fake images, videos, and audios. This can have drastic negative impacts on trust in news and security, where the public might begin to distrust all media being spread under the belief that it is misinformation created by AI. This project will create a machine learning (ML) algorithm to determine whether an image is artificially generated or authentic. This system will be able to be used in reinforcing trust in media and reducing the spread of misinformation. The dataset for this project comes from a joint effort between Shutterstock and DeepMedia [1]. Shutterstock provides authentic images from their stock photo library while DeepMedia provides the counterpart AI-generated images, using the stock image description as a prompt to create the image. There is a balanced selection of images across a variety of themes, of which one third feature humans. Discerning real pictures of humans from AI generated humans is one of the major motivations for this project, due to the potential for harm in this specific area. The dataset also includes pre-curated train and test sets. In total, there are over 85,000 provided images. The large dataset being provided allows for the creation of a robust image authentication system.

### Proposed Approach
For this project, each image must only be evaluated as AI-generated or authentic. The dataset includes labeled data that classifies each image as AI-generated or authentic. With these factors, it is most reasonable to use a supervised learning classification approach. The classification method divides the dataset into a class or category, in this case whether the image is AI-generated or authentic. To best ascertain the key features in the image that show whether an image is real or not, a convolutional neural network (CNN) will be used. A CNN allows for maintaining information from the original image, capturing both low-level and high-level patterns. While doing this, it still maintains simplicity for design and training in a way that a transformer model would not. In common AI generated imagery of people, features such as faces or hands are often disfigured. This allows a human to easily distinguish AI generated imagery from real photos. Similarly, the CNN (if properly defined and trained) would be able to use these same features in classifying the images. During training, a sufficiently large CNN should be able to learn higher order features that are not easily seen by humans, allowing for performance perhaps even surpassing that of the average human. To implement the model, various common data science and ML libraries in python will be used. Libraries like NumPy, pandas, Matplotlib, and PIL will be used for preprocessing and visualizing the dataset. The model itself will be defined and trained using PyTorch [2]. Auxiliary libraries such as sklearn may be used for data preprocessing tasks and for scoring the trained model. Training will be performed on the teams’ personal devices, potentially using Nvidia’s CUDA framework for accelerated training and iteration.

### Intruuctions
1. Download dataset: https://drive.google.com/drive/folders/1kCYkzUajOW_Qra3JMS0rnFjCQgryp8pW?usp=drive_link 


### References
[1] A. Sala, “Detect AI vs. human-generated images,” Kaggle, https://www.kaggle.com/competitions/detect-ai-vs-human-generated-images/overview (accessed Feb. 11, 2025).

[2] PyTorch, “Training a Classifier,” pytorch.org, 2017. https://pytorch.org/tutorials/beginner/blitz/cifar10_tutorial.html (accessed Feb. 12, 2025)

[3] Ultralytics, “Image Classification - Unlock the power of AI with Ultralytics! Learn about image classification, CNNs, and real-world applications in healthcare and agriculture.,” Ultralytics.com, 2024. https://www.ultralytics.com/glossary/image-classification (accessed Feb. 12, 2025)

[4] M. Ingole, “Simple convolutional neural network (CNN) for dummies in pytorch: A step-by-step guide,” Medium, https://medium.com/@myringoleMLGOD/simple-convolutional-neural-network-cnn-for-dummies-in-pytorch-a-step-by-step-guide-6f4109f6df80 (accessed Apr. 4, 2025). 