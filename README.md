# PhDEE19004_COVID19_DLSpring2020
This repository contains code and results for COVID-19 classification assignment by Deep Learning Spring 2020 course offered at Information Technology University, Lahore, Pakistan. This assignment is only for learning purposes and is not intended to be used for clinical purposes.

#
# Assignment 5 Part 1
# Dataset
https://drive.google.com/drive/u/1/folders/1-FzZhQO9oHIT9SNOWYoKsuz7fe447vtR?authuser=1


Bestmodels results are shown below. 

# Results Task 1

| Model         | Test Accuracy | F1 Score |
| ------------- | ------------- | -------- |
|     VGG16     |       94      |    0.956 |
|   Resnet18    |       92      |   0.9381 |


# Results Task 2

| Model         | Test Accuracy | F1 Score |
| ------------- | ------------- | -------- |
|     VGG16     |       96      |    0.972 |
|   Resnet18    |       97      |   0.9794 |

# Confusion Matrices for test results

VGG16 Task 1 (FC layer fine tuned only)

|               |    Infected   |   Normal |
| ------------- | ------------- | -------- |
|   Infected    |      550      |      65  |
|    Normal     |       16      |     869  |

VGG16 Task 2 (Entire layers fine tuned)

|               |    Infected   |   Normal |
| ------------- | ------------- | -------- |
|   Infected    |      583      |      32  |
|    Normal     |       19      |     866  |

Resnet18 Task 1 (FC layer fine tuned only)

|               |    Infected   |   Normal |
| ------------- | ------------- | -------- |
|   Infected    |      541      |      74  |
|    Normal     |       38      |     847  |

Resnet18 Task 2 (Entire layers fine tuned)

|               |    Infected   |   Normal |
| ------------- | ------------- | -------- |
|   Infected    |      585      |      30  |
|    Normal     |       11      |     874  |


# Models

Trainined VGG16, and Resnet18 models both for Task 1 and Task 2 are provided in folder 'Weights' (a link is given to google drive where files are stored). For task 1 stored model files are named as modelname_FC_Only.pth, and for task 2 stored model files are named as modelname_entire.pth
#
# Part 2 Comparison with and without Focal Loss

# Dataset
https://drive.google.com/open?id=1eytbwaLQBv12psV8I-aMkIli9N3bf8nO

# Best Models without Focal Loss

|       Model         | Validation Accuracy | F1 Score |
| ------------------- | ------------------- | -------- |
|        VGG16        |          94         |    0.956 |
|      Resnet18       |          92         |    0.927 |


# Best Models with Focal Loss

|       Model         | Validation Accuracy | F1 Score |
| ------------------- | ------------------- | -------- |
|        VGG16        |          93         |    0.939 |
|      Resnet18       |          91         |    0.925 |

#
# Confusion Matrices of Trained Models evaluated on Validation Data set
**VGG16 without Focal Loss**
|     rest      |    Covid 19   |          
| ------------- | ------------- |
|     599       |       1       |          
|       8       |       20      |          

|     rest      |      Normal   |         
| ------------- | ------------- | 
|     207       |       21      |         
|       8       |      392      |         

|     rest      |   pneumonia   |
| ------------- | ------------- |
|     391       |       9       |
|     19        |       209     |

\
**VGG16 with Focal Loss**
|     rest      |    Covid 19   |          
| ------------- | ------------- |
|     600       |       0       |          
|       8       |       20      |          

|     rest      |      Normal   |         
| ------------- | ------------- | 
|     207       |       21      |         
|      15       |      385      |         

|     rest      |   pneumonia   |
| ------------- | ------------- |
|     387       |       13      |
|     22        |       206     |

\
**Resnet18 without Focal Loss**
|     rest      |    Covid 19   |          
| ------------- | ------------- |
|     599       |       1       |          
|      11       |       17      |          

|     rest      |      Normal   |         
| ------------- | ------------- | 
|     201       |       27      |         
|      13       |      387      |         

|     rest      |   pneumonia   |
| ------------- | ------------- |
|     386       |       14      |
|     28        |       200     |


\
**Resnet18 with Focal Loss**
|     rest      |    Covid 19   |          
| ------------- | ------------- |
|     599       |       1       |          
|      17       |       11      |          

|     rest      |      Normal   |         
| ------------- | ------------- | 
|     202       |       26      |         
|      15       |      385      |         

|     rest      |   pneumonia   |
| ------------- | ------------- |
|     386       |       14      |
|     24        |       204     |

#
# Models
Link to saved models are provided in Weights folder. For models without focal loss names are vgg16_without_focal_loss.pth and res18_without_focal_loss.pth, and models with focal loss names are vgg16_focal_loss.pth and res18_focal_loss.pth.
\
\
For VGG16 without focal loss case fully connected layers and their neurons settings are 25088 x 4096 x 1024 x 3
\
For VGG16 with focal loss case fully connected layers and their neurons settings are 25088 x 4096 x 3 
\
For Resnet18 without focal loss case fully connected layers and their neurons settings are 512 x 140 x 3
\
For Resnet18 with focal loss case fully connected layers and their neurons settings are 512 x 140 x 3

