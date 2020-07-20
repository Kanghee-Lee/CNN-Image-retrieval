# CNN-Imate-retrieval
CNN Image Retrieval on Tattoo dataset with Tensorflow and Keras : Implementation of following papers
1. Implementation of [Particular Object Retrieval with Intergral Max-Pooling of CNN Activations](https://arxiv.org/abs/1511.05879)
2. Implementation of [Faster R-CNN : Towards Real-Time object detection with Region Proposal Networks](https://arxiv.org/abs/1506.01497)

## Dataset
Since I received the dataset from Tattoo Dataset Organization, you need your own dataset.

## Usage
```
├── ROOT
   └── dataset (train dataset for Faster R-CNN model)
       ├── final_annotations.txt (you can find the reference for this file in my dataset folder)
       ├── images
           ├── xxx.jpg 
           ├── yyy.png
           ├── ...

   └── test_dataset (test dataset for Faster R-CNN model)
       ├── final_test_annotations.txt (you can find the reference for this file in my test_dataset folder)
       ├── images
           ├── xxx.jpg 
           ├── yyy.png
           ├── ...
   └── retrieval_test (test dataset for Image Retrieval)
       ├── images
           ├── xxx.jpg 
           ├── yyy.png
           ├── ...
```



# Getting Started
* You need your own dataset for every following steps.

* [frcnn_train_vgg.ipynb](Object_Detection/frcnn_train_vgg.ipynb) This notebook is for the training Object detection model(Faster R-CNN). 
It includes code to run object detection and instance segmentation on arbitrary images.

* [frcnn_test_vgg.ipynb](Object_Detection/frcnn_test_vgg.ipynb) This notebook is for the testing Object detection model(Faster R-CNN). 

* [Retrieval_Model_final.ipynb](Retrieval_Model/Retrieval_Model_final.ipynb). This notebook applies max-pooling on last convolution feature map and then generates pickles for each image in training dataset.

* [Ranking_Module.ipynb](Retrieval_Model/Ranking_Module.ipynb) This notebook is for the testing performance of image-retrieval.




# Training on Your Own Dataset

To train and test this model, you need to build your own dataset.

For each dataset folder, you need annotations.txt files. It includes ground truth for (path / bounding box coordinates / class label).

### Path

Since notebooks are colab files, image datasets shoud be in your google drive and it corresponds to ground truth path.

### Bounding box coordinates and class label

I used RectLabel application for bounding box labeling. you can use other applications for this task.




# Project using this model

If you extend this model to build projects that use it, I'd love to hear from you.

### Object detection

<img width="432" alt="스크린샷 2020-07-20 오후 6 27 02" src="https://user-images.githubusercontent.com/45263010/87922419-f1559d80-cab6-11ea-9f63-87430b133acf.png">
  
<img width="319" alt="스크린샷 2020-07-20 오후 6 27 25" src="https://user-images.githubusercontent.com/45263010/87922552-1d711e80-cab7-11ea-8bb1-1fa7e7a34c8e.png">

<img width="545" alt="스크린샷 2020-07-20 오후 6 28 17" src="https://user-images.githubusercontent.com/45263010/87922560-1fd37880-cab7-11ea-9775-e438b6223e94.png">


### Image Retrieval

<img width="1266" alt="스크린샷 2020-07-20 오후 6 36 31" src="https://user-images.githubusercontent.com/45263010/87923520-98870480-cab8-11ea-9850-cada0c0d93c7.png">
<img width="1266" alt="스크린샷 2020-07-20 오후 6 41 42" src="https://user-images.githubusercontent.com/45263010/87923883-1814d380-cab9-11ea-8fbe-7b5c4fd1134a.png">
<img width="1306" alt="스크린샷 2020-07-20 오후 6 44 33" src="https://user-images.githubusercontent.com/45263010/87923890-1a772d80-cab9-11ea-9271-53612221fe3b.png">
