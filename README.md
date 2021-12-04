## **A CNN Based Bagging Learning Approach to CIFAR-100 Dataset**
##
## **1. Task Description:** The task assigned was to download the CIFAR-100 Dataset and building CNN and bagging CNN to train on this dataset. After that testing two implemented CNNs respectively with the same hyper-parameters. Finally calculating and comparing training and testing accuracies. Plotting learning curves for losses on these CNNs.

## **2. Model Description:** The baseline CNN model has four Conv2D layers, two MaxPooling2D layers and one dense layer.

![image](https://user-images.githubusercontent.com/56138950/144696450-7ff7acc7-8f1a-4867-87da-30bbce8008a2.png)


Fig 1: Baseline CNN model

The bagging CNN consists of five individual CNN models. Of them, three have similar kind of architecture varying the number of nodes in each layer. And the other two are of similar kind. The last two have two Conv2D layers with one MaxPooling2D layer and one Dense layer. Number of nodes for each layers are different for each model.

![image](https://user-images.githubusercontent.com/56138950/144696483-3a01eb4c-d35c-41e7-9a9f-05409cf1aedf.png)

Fig 2: The fourth CNN of bagging CNN

The hyper-parameters are chosen same for both CNN and Bagging CNN models. Learning rate was 0.01 and epochs are 50.

**3. Result Analysis:** For bagging CNN, individual model’s training and testing accuracies are given below:


|Model|Training Accuracy(%)|Testing Accuracy(%)|
| - | - | - |
|CNN1|55.18 |47.7|
|CNN2|38.04|41.5|
|CNN3|24.80|31.8|
|CNN4|80.46|38.9|
|CNN5|47.14|37.4|

For CNN and Bagging CNN, the testing accuracies and the time elapsed are shown below:


|Model|Accuracy(%)|Time(Seconds)|
| - | - | - |
|CNN|47.39|134.03|
|Bagging CNN|39.50|618.72|


The learning curve for losses on CNN is shown below:

![image](https://user-images.githubusercontent.com/56138950/144696503-1d4884e9-4129-45ef-ae12-b64e57673c6d.png)


From the comparison we can conclude that these weak learners of bagging CNNs didn’t perform that well, that’s why the average of the testing accuracy as a bagging CNN is not satisfactory. It was less than the baseline CNN.











