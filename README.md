def speak(text):
    engine = pyttsx3.init()
    # print("hello sir i am jarvis !")
    Id = r'HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Speech\Voices\Tokens\TTS_MS_EN-US_DAVID_11.0'
    engine.setProperty('voice',Id)
    engine.say(text=text)
    engine.runAndWait()
# speak("Hello sir! . I am Jarvis.")


def speechrecognition():
    r = sr.Recognizer()
    with sr.Microphone() as source:
        print("Listening......")
        r.pause_threshold = 1
        audio = r.listen(source,0,8)

    try:
        print("Recognizing.....")
        query = r.recognize_google(audio,language="en")
        return query.lower()
    except:
        return ""
speak("Helle sir my name is jarvis!")
speechrecognition()












Traceback (most recent call last):
  File "e:\jarvis\jarvis.py", line 29, in <module>
    speechrecognition()
  File "e:\jarvis\jarvis.py", line 17, in speechrecognition
    with sr.Microphone() as source:
         ^^^^^^^^^^^^^^^
  File "C:\Users\TECH ZONE\AppData\Roaming\Python\Python312\site-packages\speech_recognition\__init__.py", line 80, in __init__    
    self.pyaudio_module = self.get_pyaudio()
                          ^^^^^^^^^^^^^^^^^^
  File "C:\Users\TECH ZONE\AppData\Roaming\Python\Python312\site-packages\speech_recognition\__init__.py", line 111, in get_pyaudio
    from distutils.version import LooseVersion
ModuleNotFoundError: No module named 'distutils'
















