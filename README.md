# CNN-Based-Classification-of-Breast-Images
## Introduction
This project aims to leverage deep learning techniques,
particularly custom CNNs and modern CNNs, to develop an
automated image classification system that can accurately
distinguish between benign and malignant breast tissues.
Histopathological image analysis, which involves examining
tissue samples under a microscope, is a key method for
diagnosing breast cancer. The input to the model is a colored
RGB histopathological image of breast tissue with 3 channels.
The input is trained on a convolutional neural network to
output a predicted cancer type. The output is binary, where 0
is benign(non-cancerous) and 1 is malignant (cancerous).

## Dataset
The Breast Cancer Histopathological Database (Break His) is extracted
from Kaggle online datasets. It comprises 7,909 images of
breast tumor tissue collected from 82 patients using different
magnifying factors (40X, 100X, 200X, and 400X). The
dataset contains 2,480 benign and 5,429 malignant samples
(700X460 pixels, 3-channel RGB, 8-bit depth in each
channel, PNG format).
It has been organized to train, validate, and test data, with
each containing benign and malignant images with different
magnifying factors. The training data has 5,536 samples,
which is 70% of the entire dataset. The validation data has
1,186 samples, which is almost equal to the test data, which
has 1,187 samples, both contributing to 30% of the dataset.

## Experiment
IV. EXPERIMENT
A. Evaluation Metrics
The results of both the custom CNN and the ResNet18
pretrained model are evaluated on the same evaluation metrics
to ensure consistency and to better compare the performance
of both models.
Confusion Matrix
A confusion matrix is commonly used to evaluate the
performance of classifiers. The idea behind it is to count the
number of times instances of one class are classified as the
other class. [4] Each row of the confusion matrix represents
an actual class, while each column represents a predicted
class.
The first row of the confusion matrix shows that the model
predicted 308 benign images correctly as benign and classified
64 benign images as malignant. The second row shows that
the model predicted 86 malignant images as benign and 729
malignant images as malignant.
Precision
Having a model that classifies malignant images as benign can
give false hope to say, a patient who has been told they have a
benign tumour but actually has a malignant tumour. Precision
calculates the accuracy of the positive predictions. It is
calculated as
𝑃𝑟𝑒𝑐𝑖𝑠𝑖𝑜𝑛 = 𝑇𝑃 / (𝑇𝑃 + 𝐹𝑃))
The precision of the custom CNN is 0.92. About 92% of the
samples predicted as malignant are malignant. Precision is
typically used with Recall.
Recall
It is the ratio of positive instances that are correctly classified
by the model. It is calculated as
𝑅𝑒𝑐𝑎𝑙𝑙 = 𝑇𝑃 / (𝑇𝑃 + 𝐹𝑁)
The recall score is 0.89, which means that 89% of all the
malignant samples were predicted correctly.
F1 Score
The final metric used is the F1 score which is the harmonic
mean of precision and recall. The score is 0.91

The model made almost perfect predictions of the benign and
malignant image samples. The code was run thrice to shuffle
the data and the model still showed correct labels. From these
results, there is a distinct difference between benign and
malignant breast tissue samples. Benign tissue samples are
less pigmented and show some structure while the malignant
tissue samples are more pigmented.
The ResNet18 pretrained model outperforms the custom
CNN model and achieves the best recall score of 98%.

## Comparisons
METRIC CUSTOM CNN RESNET18
ACCURACY 87.36% 96.38%
PRECISION 91.93% 95.51%
RECALL 89.45% 98.28%
F1 SCORE 90.67% 97.39%
