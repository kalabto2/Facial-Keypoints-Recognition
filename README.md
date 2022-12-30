# mvi-sp

## Introduction
This semestral project is a competion on Kaggle - [*Facial Keypoints detection*](https://www.kaggle.com/competitions/facial-keypoints-detection/overview). In shortcut, main aim is to find 15 keypoints on human face from an image. Souch keypoints ar e.g. *left_eye_center*, *right_eyebrow_outer_end*, *nose_tip*, ...
Training dataset contains 7049 images, however some features have missing values (availabel only ~ 2000 fully labeled records) and this dataset needs to be split into validation set.

## Content
Repository contains following:
* *report.pdf*
* *facePointsRecognition.ipynb*
* *test_results.png* - results of test
* *models/* - folder containing saved models and their loss history. Specifically ResNet34 and ResNet18 without dropout and with preprocessing. Other models weren't enclosed because of size.

## Instalation
Notebook is also available under this link [here](https://colab.research.google.com/drive/1JOZbN2CmU08E_kKLzugKNP1sCBsjBng-?usp=sharing).

### Data
First needs to be downloaded datasets from [here](https://www.kaggle.com/competitions/facial-keypoints-detection/data?select=test.zip). Then move the downloaded dataset to root of this repository. Then execute this commands for unzipping and creating correct folder structure.
```
mkdir data
mv facial-keypoints-detection.zip data/
cd d	ata/
unzip facial-keypoints-detection.zip
unzip training.zip
unzip test.zip
rm *zip
```

### Requirements + running
Code is in *facePointsRecognitions.ipynb* notebook. 
In following code snippet is process of running jupyter notebook in virtual environment.
```
python3 -m venv venv
source venv/bin/activate
python3 -m pip install -r requirements.txt
python3 -m jupyter notebook
```
Environment can be deactivated by:
```
deactivate
```