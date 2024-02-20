
![kerascv](https://github.com/TH-Activities/saturday-hack-night-template/assets/117498997/8a64f118-b69d-4bd7-b59b-a28becafe0dd)



# EatNot
EatNot detects if a person is eating through a live camera feed to show the live feed on the TinkerSpace TV.

## Team members
1. [Jerom Tom](https://github.com/jeromtom)

## Link to product walkthrough
[link to video](Link Here)

## How it Works?
1. Under the hood, a Human Activity Recognition Model classifies human activities into 15 classes like 'eating', 'sleeping', 'using_laptop', 'clapping', etc. The live feed from the camera is passed in frame by frame. If 'eating' is detected above a certain accuracy percentage, it is supposed to trigger an event on [TinkerSpace Digital](https://github.com/tinkerhub/tinkerspace_digital) (not implemented yet) to show the live feed for 10 seconds on the TinkerSpace TV which can be reviewed by the tinkerers to speak to the hungry tinkerer to go to the pantry.

2. Any camera including CCTV can be used after configuring it to be an ip camera through HTTP or RTSP protocols.
3. The following activity classifications are available:

   ![image](https://github.com/jeromtom/KerasCV-HAR/assets/83979298/8c2694f2-a38b-4c25-aa68-5fa8ca569c97)

Note: It is silghtly harder for to diffrentiate between laughing-clapping and fighting-calling.


## Libraries used
1. Keras
2. [Human Action Recognition Dataset](https://www.kaggle.com/datasets/meetnagadia/human-action-recognition-har-dataset/)
3. [DroidCam](https://www.dev47apps.com/)

## How to configure and run
1. Make a copy of the [Google Colab Notebook](https://colab.research.google.com/drive/1R_2wd37K65sVIamg7kJafRTanaI7yzHx?usp=sharing) upload your Kaggle API.
2. Connect to a local runtime following [this guide](https://research.google.com/colaboratory/local-runtimes.html) if you have a good GPU. I used TinkerGPU (Nvidia RTX 400 ADA SF). Or to a hosted T4 GPU.
3. Run all the cells, edit the file paths wherever necessary.
4. Currrently we use [DroidCam](https://www.dev47apps.com/droidcam/connect/) for capturing images, and fetch the latest image saved using the date and time in the filename. Alternatively, you can [connect your webcam to Google Colab](https://colab.research.google.com/#snippetFileIds=%2Fv2%2Fexternal%2Fnotebooks%2Fsnippets%2Fadvanced_outputs.ipynb&snippetQuery=Camera%20Capture)
5. The output is a predection and its probability, we can then write functions that will run if a certain human action is detected bovce a certain probability.

This can be used to detect people eating inside TinkerSpace or to detect laughing/clapping to trigger confetti on [TinkerSpace Digital](https://github.com/tinkerhub/tinkerspace_digital) which is usually live on the TinkerSpace TV.
