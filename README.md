# covid-19

The objective of this analysis is to develop a** Convolutional Neural Network (CNN)** for
classifying medical images into COVID and Normal categories. The dataset contains 251 RGB
images of size 128 × 128 pixels. The analysis aims not only to achieve good classification
accuracy but also to correctly identify COVID-positive cases, for which COVID recall is
considered an important evaluation measure.
The methodology begins with loading the image and label data, followed by exploratory analysis
and preprocessing. The labels are encoded as COVID = 1 and Normal = 0. The data is divided
into 70% training, 15% validation and 15% testing sets using stratified sampling. Pixel
values are normalized from the range 0–255 to 0–1. Two CNN architectures are then developed
using convolutional and max-pooling layers for spatial feature extraction, followed by dense
layers for classification.
The first CNN contains three convolution-pooling combinations, followed by a dense layer
and sigmoid output. It achieves 100% training accuracy and recall, with 97.37% validation
accuracy and 100% COVID recall. However, the perfect training performance indicates
possible overfitting. To improve generalization, the second model reduces the convolutional
depth and uses a lower Adam learning rate of 0.0001.
The second CNN achieves 96% training accuracy and 97.37% validation accuracy, with
94.1% COVID recall. Compared with the deeper model, it provides better generalization while
maintaining high validation performance. Therefore, the 2-convolution-layer CNN is selected
as the final model. Overall, the analysis demonstrates that a relatively simple CNN can
effectively classify COVID-related images while reducing the risk of overfitting on a small
medical image dataset.
