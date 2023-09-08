# DefectDetection

Detection Systems to improve defect detection accuracy for defective pieces, increase productivity, reduce costs, and enhance customer satisfaction in the manufacturing industry It will pave the way for the adoption of data
science-driven solutions, contributing to the advancement of quality control practices
in manufacturing sectors.

The architecture of the model designed, comprised a sequence of steps to be built. The steps
are mentioned below
#### Data Collection: 
Data was collected in the form of frames from 360-degree videos
of both defected and non-defected circular surfaces. This process allowed gathering
thousands of images showing different types of defects.
#### Data Preprocessing:
a. Cropping: The images were cropped to extract the central circular region. This
step is likely taken to remove irrelevant background information and focus the model
on the essential circular area where the defects might appear. b. Graying: The cropped
images were converted to grayscale. Grayscale images contain only intensity information, which can be beneficial in cases where color is not essential for the detection task.
This step could simplify the computation for the model while preserving the essential
features.
#### Data Splitting: The preprocessed data was divided into three sets: training, testing,
and validation datasets. This division is crucial to evaluate the model’s performance
accurately.
 ### Model Architecture:
**a. Convolutional Layers (Conv2D)**: Several layers of Convolutional Neural Network
(CNN) with Conv2D layers were used. These layers are designed to detect patterns and
features within the input images. Conv2D layers use filters/kernels to scan the images
and create feature maps, highlighting essential visual patterns relevant to identifying
defects.


**b. Maxpooling Layers:** After each Conv2D layer, Maxpooling layers were applied.
Maxpooling is a downsampling technique that reduces the spatial dimensions of the
feature maps while retaining the most relevant information. It helps reduce computational complexity and makes the network more robust to slight variations in input.

**c. ReLU Activation Function:** The Rectified Linear Unit (ReLU) activation function
was used. ReLU is commonly used in CNNs as it introduces non-linearity, allowing
the network to learn complex patterns and relationships in the data. It helps in avoiding
vanishing gradient problems and accelerates the convergence of the training process.

**d. Dense Layers:** After the Conv2D and Maxpooling layers, Dense layers (also known
as fully connected layers) were added. These layers help in combining the features
learned from the convolutional layers and making decisions based on these features.
Dense layers can help learn high-level abstractions and representations of the data.

**e. Softmax Layer:** At the end of the network, a Softmax layer was added. Softmax
is used for multi-class classification problems. It converts the final layer’s raw outputs
(logits) into probability values representing the likelihood of each class. In this case,
it would output the probabilities for different defect types and non-defect.

• Adam optimizer was chosen. Adam is an adaptive learning rate optimization algorithm that combines the benefits of AdaGrad and RMSProp. It dynamically adjusts
the learning rate during training, making it well-suited for deep learning models with
large datasets.

• Loss Function and Model Training: The model was trained using the training dataset.
During training, the model learns to adjust its weights and biases to minimize the chosen loss function using backpropagation and gradient descent techniques.

• Model Evaluation and Validation: After training, the model’s performance was evaluated using the testing dataset. This step is crucial to assess how well the model generalizes to unseen data. Additionally, the validation dataset was used to monitor the
model’s performance during training and to prevent overfitting. If the model performs
well on the training data but poorly on the validation data, it might indicate overfitting.
