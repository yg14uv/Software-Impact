# A Two-Tiered Framework for Anomaly Classification in IoT Networks Utilizing CNN-BiLSTM Model
Welcome to our GitHub repository. We present our robust security mechanism named the "Anomaly Classification System for IoT (ACS-IoT), structured as a two-tiered framework: the Inspection tier and the Detection tier. These tiers are designed to analyze network traffic and packets comprehensively, enabling the detection of any intrusion or attack. In the first tier, it employs machine learning-based classifiers for initial anomaly detection. In the second tier, a CNN-BiLSTM model is utilized for a more profound analysis and classification of anomaly types.

## Data Preprocessing
To build an effective anomaly classification system, we propose an efficient data preparation scheme that involves feature selection using PSO, data normalization, and data balancing using SMOTE. This scheme optimizes both the training process and anomaly detection, contributing to the overall effectiveness of ACS-IoT. 
Imbalance data present in the dataset can cause the model to identify minority classes as majority classes. This can cause the model to be biased and consequently degrades the model's performance and overall quality of the classification task. To overcome this issue, we have employed the SMOTE oversampling method which synthetically generates samples of the minority class.
Another important function that is performed in the preprocessing step is that we have applied Particle Swarm Optimization (PSO) as a feature selection technique in order to select the most important and distinguishing features from the input dataset. PSO not only reduced the computation cost but also saved the training time and memory. This also had an impact on the energy consumption of the system.

## Anomaly Classification
The IoT network consists of many flows generated at rapid rates. This big data environment requires highly efficient processing, which is one of the main challenges of anomaly classification methods in IoT networks. To solve this issue, the proposed ACS-IoT employs a decision tree binary classifier to detect anomaly flows efficiently. Decision Tree classifier works efficiently for binary classification problems. It tells if there is an anomaly or not. It cannot classify the type of anomaly as it is a less compute-intensive layer and only works as a filter to classify between normal and anomaly data. If there is no anomaly then the control will not pass on to CNN-Bilstm. This keeps the overall system lightweight and reduces the computation costs without compromising on the IoT vulnerability.
ACS-IoT deploys a Convolutional neural network (CNN), which focuses on feature extraction, facilitating effective categorization within the BiLSTM. CNN allows complex operations on the hidden layers to reduce the attributes and share weights. BiLSTM processes the variable-length sequential input data, and output can be produced at each recurrent step. Based on the recent input data and the previous step’s hidden neurons, hidden neurons at each time step are calculated. The extracted features of each flow are fed into the forward LSTM network and the backward LSTM network.

## Dataset
The dataset that is used in this work is the New IoTID20 dataset, which is developed for anomalous activity detection in IoT networks. The dataset can be downloaded from the following link: https://sites.google.com/view/iot-network-intrusion-dataset/home. It contains different types of IoT attacks as well as their families. The dataset consists of three major categories. One is binary which has a binary label distribution consisting of 40073 Normal instances and 585710 Anomaly instances. The second category has a category label distribution consisting of 40073 Normal instances, 59391 instances of DoS, 415677 instances of Mirai, 35377 instances of MITM, and 75265 instances of Scan attack. The third category has a subcategory label distribution with 1211811 Brute Force instances, 55818 instances of HTTP Flooding, 183554 instances of UDP Flooding, and some other attack categories.


## Conclusion
Anomaly Classification System for IoT (ACS-IoT), a two-layer framework tailored for efficient anomaly classification in IoT networks. By combining a decision tree classifier in the first layer and a CNN-BiLSTM model in the second layer, ACS-IoT demonstrated the capability to detect anomaly flows and accurately classify different anomaly types, surpassing existing machine learning and deep learning-based approaches in terms of accuracy, precision, and recall. The incorporation of data balancing, feature selection techniques, and optimal hyper-parameter tuning further bolstered ACS-IoT's performance, offering valuable contributions to IoT security and laying the groundwork for more sophisticated and accurate intrusion detection systems in the ever-evolving landscape of IoT networks.
