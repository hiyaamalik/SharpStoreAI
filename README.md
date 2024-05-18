# SharpStoreAI
This project works on image files. It performs blur classification and stores non-blur images in the path of the folder specified by the user. Following that, it performs selections to choose the best shot among groups of duplicates from that folder and saves that in the output folder which is again user-defined.
The project performs two major tasks :
1. Blur Classification
2. Best picture Selection among groups of duplicates 

Firstly, the blur classification model involves creating a convolutional neural network (CNN) using TensorFlow and Keras to classify images as blurred or non-blurred. The model is trained on a dataset of labelled images, resized to 224x224 pixels, and normalized. The CNN architecture includes multiple convolutional and max-pooling layers, followed by dense layers, designed to extract and learn features indicative of blurriness. After training and validating the model, it achieves good accuracy in distinguishing between blurred and non-blurred images. A function is implemented to classify new images, saving non-blurred images in their original size to a specified "sharp" folder. Additionally, a utility function counts the number of files in the "sharp" folder, ensuring accurate processing of images.

Following this, we have a model to select the best pictures among groups of duplicates that processes a folder of images to select and save the best shots based on feature extraction using a pre-trained VGG16 model. It includes functions to preprocess images, extract features, and calculate similarity between images. For each image, the script identifies the most similar image from the dataset and saves it as the best shot in an output folder. It also visualizes the distribution of similarity scores. Finally, the script counts and prints the number of files in the output folder to verify the number of best shots saved. This approach helps automate the selection of high-quality images from a dataset.

The ds dataset on which the blur classification model has to be trained is given in the link below. Users must change the paths across the code as per his/her folders (unseen_images_folder which contains your uncategorised data on which task is to be performed sharps and best where sharp was used to store non-blur images and best was used to store selected best shots among duplicates)

ds link - https://drive.google.com/drive/folders/1geTuzN1opXrM4q5DbjXtBiJP2t7-T6bh?usp=sharing 
Download it and use the path accordingly.
