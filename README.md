# StyleTTS2-Train

# Prerequisities

**Raw WAV files preparation**

- create audio files that are **longer than 1 second** and ideally **shorter than 12 - 20 seconds** in length along with **Audacity-compatible labels** ( you can use [My Audio Preparation Notebook](https://colab.research.google.com/drive/1ZK-2lAV2DokrN92sYPJRl47XyuuluCJe?usp=sharing) and then [Audacity](https://www.audacityteam.org/) to re-align the labels, if you have a single long recording that you need to transcribe )
- name your files, so they begin with the **same prefix** and always **have 5 digits** after it (such as B1-, e.g. *B1-00001.wav*)
- **zip-up** your **WAV files and labels.txt file** into a single ZIP file. All files need to be in the root folder of that ZIP file, i.e. no sub-folders.
- *ZIP file example:*
  - *B1-00001.wav*
  - *B1-00002.wav*
  - *B1-00003.wav*
  - *B1-00004.wav*
  - *labels.txt*

**Processed WAV files**

- this Notebook allows you to download and save your processed WAV files to Google Drive. Processed WAV files that are directly prepared for training have these **attributes**:
  - they are **MONO** files with a sample rate of **24k**
  - they have **leading and trailing silences trimmed**
- furthermore, the ZIP file with processed WAV files also contains the following:
  - **metadata.csv** file that's compatible with LJSpeech CSV format. This file is not directly used but is kept as a reference, so you can see in plain text what sentences is the TTS being trained on.
  - **metadata_phonetical.csv** file that is a direct phonetical representation of the metadata.csv file. This file is not directly used for training but training and validation data are devised from it.
  - **training.csv** file which contains training data for StyleTTS2
  - **validation.csv** file which contains validation data for StyleTTS2
- structure of this ZIP file is different than the raw WAV files ZIP file
- *ZIP file example:*
  - *metadata.csv*
  - *metadata_phonetical.csv*
  - *training.csv*
  - *validation.csv*
  - *wavs/B1-00001.wav*
  - *wavs/B1-00002.wav*
  - *wavs/B1-00003.wav*
  - *wavs/B1-00004.wav*
