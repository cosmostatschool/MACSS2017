Miniconda2 Installation 

MacOS:

If you are new in Mac OS X but are experienced in Linux, you will be happy to use the Terminal in a way quite similar to Ubuntu; but first, you will have to spend two or three hours installing the basics.

Keep in mind that this installation is for a environment that doesn’t affect other packages that you may already have in your system. One advantage of doing this installation is that miniconda also installs pip to manage packages.

You should install the following packages respecting the order in the list. 

1. Install Xcode from AppStore (it is free)

2. Install Command Line Tools
	~]$  xcode-select —install

3. Agree the terms of licence
	~]$ sudo xcodebuild -license

4. Download the installation file for python2.7 from: https://conda.io/miniconda.html. Most 

5. In the directory where the installation file is run
	~]$ bash Miniconda2-latest-MacOSX-x86_64.sh

6. Follow the installation directions. It will ask you where to install, the default is “/home” In the part where it ask you to write the Miniconda2             path in the bash profile write “no”.

7. After the installation is done close the terminal window and open it again. 

8. Next write in the terminal
	~]$ cd
	~]$ source Miniconda2/bin/activate
	~]$ conda list
  if the installation was right a list of packages should appear in the terminal window

9. Installing necessary packages.
	~]$ conda install numpy
	~]$     “         “     scipy
	~]$     “         “     matplotlib
	~]$     “         “     jupyter
	~]$     “         “     sympy

10. To check the installation of the packages run in the terminal 
	~]$ python
	~]$ import numpy
	~]$ import matplotlib.pyplot as plt (this is the proper way to import matplotlib)
	~]$ exit() (this way you exit python)

11. To run Jupyter notebooks run in the terminal
	~]$ jupyter notebook
      If that doesn't work run
	~]$ jupyter-2.7 notebook-2.7
  
     This will open a window in your web explorer (the default one). And you are all set and ready. You may want to try and play. 
     There is plenty of documentation  on the web. 
     To exit jupyter just close the window, and the terminal. 
  
12. To exit the miniconda environment write
	~]$ source deactivate 	
  
Linux

The installation steps for a Linux based system are basically the same as the steps from 4 to 12, i.e.  you don’t have to install xcode,
maybe you will need the develop tools corresponding to your linux OS (check https://www.garron.me/en/go2linux/gnu-gcc-development-tools-linux-fedora-arch-debian.html), 
but we suggest you try first points 4-12, you might be lucky!

1. If when trying to import matplotlib you get the error: ImportError: No module named ‘tkinter' exit python and run
	
	~]$ conda instal tkinter 
	or
	~]$ pip install tkinter
  
2. in python run 
	>>import matplotlib
	>>matplotlib.use('Agg')
	>>import matplotlib.pyplot as plt

to choose the default plot window.
