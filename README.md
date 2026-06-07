# EXPT-5-Speech-Recognition-using-Python

# AIM: 

# To perform and verify speech recognition using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```collab
!pip install SpeechRecognition pydub
import speech_recognition as sr
from pydub import AudioSegment
from pydub.silence import split_on_silence

# Path to your audio file
audio_file_path = '/content/audio_file_path.16 56 .ogg'  # Change this to your file name and format
r = sr.Recognizer()

#convert ogg to wav
print(f"Converting {audio_file_path} tp wav...")
audio_segment=AudioSegment. from_ogg(audio_file_path)
wav_file_path="/content/temp_audio.wav")
print("Conversion complete/")

# Load the audio file
with sr.AudioFile(audio_file_path) as source:
    print("Reading audio file...")
    audio = r.record(source) # read the entire audio file

    print("Attempting to recognize speech...")
    try:
        text = r.recognize_google(audio)
        print("Recognized Text:")
        print(text)
    except sr.UnknownValueError:
        print("Google Speech Recognition could not understand audio")
    except sr.RequestError as e:
        print(f"Could not request results from Google Speech Recognition service; {e}")
```


# OUTPUT: 
![WhatsApp Image 2026-03-28 at 8 49 42 AM](https://github.com/user-attachments/assets/afa04fdb-4a82-4563-99dc-a5b050f6989e)


# RESULT: 
Thus the speech recognition using SCILAB was performed and verified.
