# facial_expression_recognition
This project implements a deep learning model to classify six basic human facial expressions: natural, angry, surprised, happy, sad, and other. It leverages transfer learning from the pre-trained VGG16 model to achieve accurate classification on a dataset of 35,000 grayscale images of size 48x48 pixels.

##Dataset

The project utilizes a dataset of 35,000 grayscale images, each resized to 48x48 pixels. These images represent six facial expressions:

-Natural
-Angry 
-Surprised
-Happy
-Sad
-Fear

##Model Architecture

The model employs transfer learning from the VGG16 architecture:

Load VGG16: Load the pre-trained VGG16 model, excluding the final classification layers.

Freeze Base Layers: Freeze the weights of the loaded VGG16 model (except the final layers) to prevent them from being updated during training.

Add New Layers: Add a set of classification layers on top of the frozen VGG16 base. These include dense neurons with appropriate activation functions, culminating in an output layer with six neurons for the six expressions.

Compile Model: Compile the model with an optimizer (e.g., Adam), a loss function (e.g., categorical cross-entropy), and metrics (e.g., accuracy) suitable for multi-class classification.


##Training

##Preprocess Data:
Split data into training, validation, and (if applicable) testing sets.
Normalize images (e.g., by subtracting mean and dividing by standard deviation).
Consider data augmentation (e.g., random flipping, cropping, rotation).


##Train Model:
Train the model on the training set, optimizing the newly added layers while keeping VGG16 base weights frozen.
Use the validation set to monitor performance and prevent overfitting.
