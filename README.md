# DL23
#@markdown 🔄 Making functions: etts('text'), ktts('text'), ftts('text')
%%capture
!pip install gTTS      # Installation
from gtts import gTTS  # Import
from IPython.display import Audio

#######################
def etts(text):
  text_to_say = text

  gtts_object = gTTS(text = text_to_say,
                     lang = "en", tld = "us",
                    slow = True)
  
  gtts_object.save("E-audio.mp3")
  return Audio("E-audio.mp3")
#######################

def ktts(text):
  text_to_say = text

  gtts_object = gTTS(text = text_to_say,
                     lang = "ko",
                    slow = False)
  
  gtts_object.save("K-audio.mp3")
  return Audio("K-audio.mp3")

#######################

def ftts(text):
  text_to_say = text

  gtts_object = gTTS(text = text_to_say,
                     lang = "fr",
                    slow = False)
  
  gtts_object.save("F-audio.mp3")
  return Audio("F-audio.mp3")

![image](https://github.com/sjhwang031/DL23/assets/127395588/0d80498d-9ad5-4e4b-aa5e-ba74056155c0)
