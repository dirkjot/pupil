## Installation instructions

Rich Stoner, Feb 20, 2014

## Dependencies - Install sequentially

#### Anaconda Python distribution (64bit)

[http://continuum.io/downloads](http://continuum.io/downloads)

Provides the python intepreter and some key packages like numpy, scipy, etc.

#### (alternative) MiniConda Python distribution

Anaconda is a very large distribution with over 200 packages of statistical software preinstalled. If you have no need 
for that, you can use MiniConda instead:
* Download miniconda from the [pydata.org](http://conda.pydata.org/miniconda.html) site (affiliated with Continuum), choose the python 2.7 , 64 bit , installer
* I suggest installing it in `c:\Anaconda` instead of `c:\Miniconda` as the installer suggests, but it does not really matter.
* In a CMD prompt, type `python` and check that you get a running python 2.7 interpreter. The first line of the welcome messsage  should include the name "Continuum Analytics".  If not, you are accessing another python on your system.  
* If the previous step did not work, add `c:\Anaconda` and `c:\Anaconda\Scripts` to your path.
* In the CMD prompt, run the `conda install X` command four times, using the following package names for X: `numpy`, `scipy`, `zeromq`, `pyzmq`. 

#### Prebuilt Win7 Python packages

[PyOpenGL‑3.0.2.win‑amd64‑py2.7.exe](http://www.lfd.uci.edu/~gohlke/pythonlibs/#pyopengl)

[PyAudio‑0.2.7.win‑amd64‑py2.7.exe](http://www.lfd.uci.edu/~gohlke/pythonlibs/#pyaudio)

[opencv‑python‑2.4.8.win‑amd64‑py2.7.exe](http://www.lfd.uci.edu/~gohlke/pythonlibs/#opencv)


#### Install FFMPEG

(Used from the original pupil install instructions)

* Download the [64-bit version](http://ffmpeg.zeranoe.com/builds/win64/static/ffmpeg-20130401-git-599866f-win64-static.7z) or [32-bit version](http://ffmpeg.zeranoe.com/builds/win32/static/ffmpeg-20130401-git-599866f-win32-static.7z).* 
* Unzip the file.
* Move the unzipped folder to `C:\Program Files\` and rename the folder to `ffmpeg`
* Open a text editor and copy-paste the following text:
    ```shell
    @ECHO OFF
    "C:\Program Files\ffmpeg\bin\ffmpeg.exe" %*
    ```

* Save the text file as `ffmpeg.bat`, within the ffmpeg folder `C:\Program Files\ffmpeg\`. _The .bat (batch) file extension is critical._ 
* Then go to 'Control Panel -> System and Security -> System'
* Select Advanced system settings. 
* In the advanced tab go to `Environmental Variables...`
* In the `System variables` section select the `path` variable
* At the end of the `variable value` text box, add the following: '; C:\Program Files\ffmpeg'
          
#### Install AntTweakBar & GLFW

These dependencies are included in the win7 branch of the repository. Their location is hard-coded for sanity's sake.

#### Install TDM-GCC MinGW compiler

[Download most recent build](http://sourceforge.net/projects/tdm-gcc/files/TDM-GCC%20Installer/tdm64-gcc-4.8.1-3.exe/download)

1. Run the install **BUT**, when creating a new installation, set the installation directory to `C:\MinGW64`
	
2. After the install, Go to `C:\MinGW64\bin` and rename `mingw32-make.exe` to `make.exe`


### Getting the code

### Install Git & clone Pupil Source Code
Download and install [Git](http://git-scm.com/download/win). This enables you to download and update the Pupil source code. 
  
  * Open the Git GUI application, and select `Clone Existing Repository`.   
  
  * Specify the source location as: `http://github.com/pupil-labs/pupil`
  
  * Select a destination and add `/pupil/` to the end of the directory (e.g. `C:/pupil/`)

  * Click on `Clone`.
  
  * Click on the `Branch` menu, select `Checkout` -> checkout the `windows` branch
  
  










#


















