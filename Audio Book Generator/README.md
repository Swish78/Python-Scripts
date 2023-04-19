Audiobook Generator

The Audiobook Generator is a Python script that reads a PDF file and converts it into an audio file using text-to-speech technology. The script uses the PyPDF2 library to extract the text from each page of the PDF file and the pyttsx3 library to convert the text to speech.

Requirements

To use the Audiobook Generator, you'll need:

Python 3.5 or higher
PyPDF2 library (pip install PyPDF2)
pyttsx3 library (pip install pyttsx3)
Usage

To use the Audiobook Generator, follow these steps:

Clone this repository to your local machine.
Place the PDF file you want to convert into the same directory as the audiobook_generator.py file.
Update the pdf_path variable in the script with the name of your PDF file.
Run the script using python audiobook_generator.py.
The script will extract the text from each page of the PDF file and convert it to speech. It will play the speech using your computer's default audio output device and save the speech as an MP4 file in the same directory as the audiobook_generator.py file.

Customization

You can customize the speech rate and voice used by the Audiobook Generator by modifying the setProperty method calls in the script. For example:

engine.setProperty('rate', 150)  # Adjust the speech rate
engine.setProperty('voice', 'english')  # Choose the voice

You can find a list of available voices on your system by running the following command in a Python shell:

import pyttsx3
engine = pyttsx3.init()
voices = engine.getProperty('voices')
for voice in voices:
    print(voice.id)

Limitations

The Audiobook Generator is designed to work with simple PDF files that contain mostly text. It may not work correctly with PDF files that contain complex formatting, images, or tables.

License

The Audiobook Generator is released under the MIT License. See LICENSE for more information.