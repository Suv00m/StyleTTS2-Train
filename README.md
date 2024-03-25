# StyleTTS2-Train

## **Step 0:get your one long single audio and subs.**
- anywhere from soundcloud or youtube
## **Step 1:prepare multiple audio files from one long single audio.**
### manually 
- select any long single audio file.
- extract the audio and the substitles.
- then in audacity start a new project 
  - import the audio file 
  - then in Tracks>>Add New>>Label Tracks
  - then make sure each 10-20 secs audio has the label (this is the longest task)
  - as for export options:
    - select the folder (ideally an empty one) where you want your WAV files to be placed
    - for audio options choose Mono
    - for sample rate, choose "Other" and type 24000 into the dialog that comes up
    - for export range, choose Multiple Files
    - for the "Split files based on" section, choose Labels
    - in the "Name files" section, choose "Numbering after File name prefix" and choose a prefix that you'll also use in the TTS training Notebook (such as "B1" or similar)
    - click on Export
### automatically
- use the [audio from whisper](https://colab.research.google.com/drive/1ZK-2lAV2DokrN92sYPJRl47XyuuluCJe?usp=sharing)
## **Step 2:prepare your audio file from one long single audio.**
- use "wavs preparation after label.ipynb"
## **Step 3:upload the zip file to google drive**
- set it to share it with "anyone with the link"
- get the id 
## **Step 4:prepare your audio file from one long single audio.**
- use "StyleTTS2_Finetune.ipynb" to train
## **references:**
- [audio from whisper](https://colab.research.google.com/drive/1ZK-2lAV2DokrN92sYPJRl47XyuuluCJe?usp=sharing)
- [styletts2 colab](https://colab.research.google.com/github/yl4579/StyleTTS2/blob/main/)
- [training](https://colab.research.google.com/drive/1PdcCcTUUYAxBM3_mDT2_UNz0ZoUkMee_#scrollTo=w68FokB4sjw2)

