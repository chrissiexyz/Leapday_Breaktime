## Take a Break

Today is leap day (2/29/2016) so I decided to initiate a small project named it **breaktime.exe**.

### First step, writing a python file
It is written in Python2.7 with Win7 system, which is in fact a very small and simple python file. I followed the first introduction lesson with Python language in Udacity and created this "take a break" file. What it does is to automatically pop up a YouTube video every two hours for 5 times. Depending what you want to put for your personal video link and how frequent you want it to appear, you can modify it yourself, making it a bit more personal.

### Second step, decide what you want to use for converting a python file into a window .exe file

I first experimented it with a software called `py2exe`, which is easy to install and run, however I found it created a folder with many file with the .exe file. If I ever want to share with anyone, I may need to send the person a zip file of the whole folder and this could be tedious. 

Then I came across another program called `PyInstaller`, which could produce a sole .exe file without many other files. I decided to go with it. The most useful tutorial I found online is this: [Creating an Executable from a Python Script] (https://mborgerson.com/creating-an-executable-from-a-python-script). I even created a dog image icon without the icon website cited in the tutorial but using [Convert your image to an icon](http://converticon.com/). I found it very fun to do so.

### Third step, can ignore it if you use `py2exe` or read it only if you want to use `PyInstaller`

The instructions below works with Python2.7 and Win7

1.  Open the system command prompt window and continue using the command prompt window
2.  Using `cd..` and `cd` to guide you to C:\Python27\Scripts where **pip** is at
3.  At C:\Python27\Scripts>, run `pip install pyinstaller`
4.  PyInstaller installed finished
5.  Depending on where you would like to create your .exe file, you could copy the newly created files and move them to a different folder or you could work on the same folder. Suppose you don't mind using the same folder as it was installed, you need to move the python file, icon image (if any) and other files (if any) into the C:\Python27\Scripts folder
6.  Under C:\Python27\Scripts>, run `pyinstaller.exe --onefile breaktime.py` (or whatever python file name you have)
7.  Then you can find the .exe file in the `dist` folder, only one file and done!
A little bit extra...
8.  To add image, move image to Scripts folder and run `pyinstaller.exe --onefile --icon=image.ico breaktime.py`
9.  If you have a version.txt file, you can also run `pyinstaller.exe --onefile --windowed --icon=image.ico --version-file=version.txt breaktime.py`

The repository include the following files:

* **Breaktime.py**: The python file for playing a YouTube video that I like every two hours to remind me to have some fun/ take a break.
* **Breaktime.exe**: The window executable file that I created.
* **README.md**: The GitHub readme file.

