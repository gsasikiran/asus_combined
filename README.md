## Classification of asus_combined dataset through Transfer Learning:

### Framework : fastai

### Dataset : asus_combined (provided by Hochschule Bonn Rhein Sieg)

* The dataset is augmented with 16 classes of 21706 local images.
* Further it is divided into 17365 images of training data and 4341(20% of total) images of validation data.
* Sample images from the dataset and labels.<br>

![sample data](https://github.com/gsasikiran/asus_combined/blob/sasi/images/docs.jpg)

### Model : resnet18
* The training is done on the pretrained imagenet model of resnet18 with 4 epochs.
* The model is inbuilt in the fastai architecture with a series of convolutional layers.
* The activation functions used are : ReLU for the innerlayers and Softmax for the ultimate layer.
* Fitting is done by [one cycle method](https://sgugger.github.io/the-1cycle-policy.html).

### Results:

<b> With pretrained model :</b>

| Epoch | Training loss | Validation loss | Accuracy | Time |
|:----------:|:--------------------:|:------------------------:|:---------------:|:---------:|
|1|	0.428112|	0.164152|	0.944944|	01:34|
|2|	0.241105|	0.063754|	0.982262|	01:32|
|3|	0.137128|	0.040256|	0.990555|	01:31|
|4|	0.129500|	0.033298|	0.992398|	01:31|

<b> Confusion Matrix: </b><br>

![confusion matrix](https://github.com/gsasikiran/asus_combined/blob/sasi/images/confusion_matrix.jpg)

<b> Most confused: </b><br>

| Actual | Predicted | Instances |
|:----------:|:---------------:|:-----------------:|
|DECOY| S40_40_B | 3 |
|MOTOR|R20| 3|
|DISTANCE_TUBE| DECOY| 2|
|R20|S40_40_B| 2|
|S40_40_B|S40_40_G| 2|
 
