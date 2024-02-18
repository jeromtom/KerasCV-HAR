
![kerascv](https://github.com/TH-Activities/saturday-hack-night-template/assets/117498997/8a64f118-b69d-4bd7-b59b-a28becafe0dd)



# EatNot
EatNot detects if a person is eating through a live camera feed to show the live feed on the TinkerSpace TV.

## Team members
1. [Jerom Tom](https://github.com/jeromtom)

## Link to product walkthrough
[link to video](Link Here)

## How it Works?
1. Under the hood, a Human Activity Recognition Model classifies human activities into 15 classes like 'eating', 'sleeping', 'using_laptop', 'clapping', etc. The live feed from the camera is passed in frame by frame. If 'eating' is detected above a certain accuracy percentage, it is supposed to trigger an event on [TinkerSpace Digital](https://github.com/tinkerhub/tinkerspace_digital) (not implemented yet) to show the live feed for 10 seconds on the TinkerSpace TV which can be reviewed by the tinkerers to speak to the hungry tinkerer to go to the pantry.

2. The following activity classifications are available:

   ![image](https://github.com/jeromtom/KerasCV-HAR/assets/83979298/8c2694f2-a38b-4c25-aa68-5fa8ca569c97)



## Libraries used
Keras
Dataset: [Human Action Recognition Dataset](https://www.kaggle.com/datasets/meetnagadia/human-action-recognition-har-dataset/)

## How to configure/Run
[Google Colab Notebook](https://colab.research.google.com/drive/1R_2wd37K65sVIamg7kJafRTanaI7yzHx?usp=sharing)
