# dodgylegally
This repository contains a Python script designed for creative audio processing and sampling. The script, inspired by work from [Colugo Music](https://x.com/ColugoMusic/status/1726001266180956440?s=20), is a versatile tool for anyone interested in generating unique sound samples from YouTube videos. 

## Overview

The script performs several key functions:
- **Random Search Phrase Generation**: It generates random search phrases from a list of words and uses these phrases to search for and download audio from YouTube.
- **Audio Processing**: Downloaded audio is then processed to create two types of samples: one-shot and looped.
- **File Management and Versioning**: Processed audio files are organized into specific directories, and a combined loop file is created without overwriting previous versions.

## Installation and setup

- **Requirements**: The script auto-installs several Python packages, including `pydub`, `yt-dlp`, `glob2` and `nltk`
- **Google Drive Integration**: The script is designed to run in a Google Colab environment and saves files directly to Google Drive. It will ask to mount your Google Drive and will create the base directory to `dodgylegally`
- **Folder Structure**: The script automatically creates necessary directories for storing raw, processed, and combined audio files.
- **Word List**: A file named `birdwater.txt` is auto-generated containing a list of randomly generated dictionary words for generating search phrases. The script checks for this file and creates it if it doesn't exist.

## Usage

To use the script, simply [run it in a Google Colab notebook](https://colab.research.google.com/drive/1faL_AErR2wnS9vr3EX1p1FRF5pzdrDnv?usp=sharing). It will prompt for the number of samples to process and then execute the following steps:

1. Generates random search phrases in `birdwater.txt` and downloads corresponding audio from YouTube.
2. Processes the audio to create one-shot`dodgylegally/wavs/oneshot/` and loop `dodgylegally/wavs/loop/` samples
3. Combines looped samples into a single audio file that repeats each sample 3-4 times, incrementing the version number to avoid overwriting. You can find it in `dodgylegally/wavs/processed/combined/`

## Customization

You can easily customize various aspects of the script, such as the batch size for downloads, the base directory in Google Drive, and the structure of the output directories.

## Acknowledgements

This script was hacked together by Daniel Raffel, based on the original work shared by [Colugo Music](https://x.com/ColugoMusic/status/1726001266180956440?s=20). It is intended for creative and experimental sound processing projects.

## License

This project is open-source and since it's based on code by [Colugo Music] I have added no license code at this time. If a request is made to add a license this will be updated. Feel free to use, modify, and distribute as per the license agreement.
