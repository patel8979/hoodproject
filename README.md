AudioBookInPython

import pyttsx3
import PyPDF2
book = open('oops.pdf', 'rb')  #rb stands for reading a binary book
pdfReader = PyPDF2.PdfFileReader(book)
pages = pdfReader.numPages
print(pages)
speaker = pyttsx3.init()
for num in range(1,1):
    page = pdfReader.getPage(1)
    text = page.extractText()
    speaker.say(text)
    speaker.runAndWait()   

