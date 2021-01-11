# Mini-Assistant-Alexa-
This is Python based project . I have created a Mini Assistant that will open a Youtube video or Website on your Voice command. Also Narrator voice over is also there (JUST LIKE ALEXA). 

LIBRARY USED 
1. Speech_recoginition # so that it could recognize user voice
2. Pyttsx3             # This coverts our text into speech means the narrator voice
3. Webbrowser          # So that a link on our default brower could open on our command

engine = pyttx3.init("sapi5")    # here we have initialize the narrator voice , sapi is the inbuilt narrator in windows , so , for our narrator w are using SAPI'S voice
in one of the line we have given a path of our favourite search engine i.e. GOOGLE CHROME   # On our voice command  , a search will be perform by opening this chrome browser

r = sr.Recognizer()    ''' it is function to recoginizr user voice , we have assign it to a variable r so that in next lines of code we dont have to write long long statements i.e. sr. Recognizer . we can replace sr.Recognizer with r where ever in the code it reflect '''

Now, how python will get our voice , obviously through mic , so we have creaed a variable mic   # mic = sr.microphone()

r.adjust_for_ambient_noise   # of course we dont want our mic to hear unwanted noise in background , so we have used this line here in the function

engine.setProperty ("rate" , 150)  # here we are setting one property , which property? yes, rate means speed of narrator's voice to 150 

engine.say("anything")   # means whatever is written here in the parantheses , narrator will going to speak.
engine.runandwait()       # this function will allow narrator to speak

audio = r.listen(source)    ''' we have created a variable "audio" in which our speech is going to recognize through the source , and source is our "mic" .obviously we are going to speak in mic '''

if we speak "video" then video is going to open on youtube and if we will speak "link" then a link will going to open . by performing if else if conditions

get= r.recognizer_google(audio)
print(get)
'''mean whatever we will speak , will hoing to record in variable get and in the next line it will get printed. for example :- if I speak "link" then "link" will get store in "get" then "link " as a word will get print in the output '''

