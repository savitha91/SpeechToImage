# Speech to Image

## MELD Dataset contains csv file and mp4 file
#### csv file containes these fields : SrNo.,Utterance,Speaker,Emotion,Sentiment,Dialogue_ID,Utterance_ID,Season,Episode,StartTime,EndTime
     For our task we would be considering Utterance, Dialogue_ID,Utterance_ID
     Using the Dialogue_ID,Utterance_ID , we can frame the video(mp3) file name corresponding to the utterance
#### mp4 video files contains audio + video info. 
     We consider the same audio recording properties used in the SEMAINE database i.e audio was recorded at 48 kHz with 24 bits per sample
     While extracting audio features from the mp4 file we consider this information
  
## Steps :
1. Speech to Text - Speech Recognition Model
#### Input  : Audio data from the mp4 file
#### Output : Utterance column from .csv file

We extract the audio features(frequency, amplitude at respective time-steps) from the input mp4 file and use exisiting model(transfer learning) to predict the utterance. Once we get good accuracy over the model, we proceed to next step

2. Text to Image : We use COCO dataset for this task
