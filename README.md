# How to install different versions of Python?

You want to install a different python version than your default python? We will be discussing on how do you do it in any linux distros. This particular article is done on Ubuntu 16.04.4 LTS 64-bit.

## Background

I have a default python install on my system and that is python3.5 and I want to try using python3.7.0. I don't want my python3.5 to be overriden since some of my existing projects are using it.

Though this article is specifically using Python3.7.0, but the concept is the same on all other versions like Python3.6, Python3.5, Python2, etc.

## What we need

* Python source code. Download python3.7.0 [here](https://www.python.org/ftp/python/3.7.0/Python-3.7.0.tgz). You can save it anywhere you want.

## Let's start the installation process

1. Extract the Python-3.7.0.tgz file.

	* open terminal
	* make sure you are currently on the directory where you saved the Python-3.7.0.tgz file
	* extract the file by running:
		```bash
		tar -xvzf Python-3.7.0.tgz
		
		```
	* this will extract to a folder Python-3.7.0 on the same directory

2. Create a folder where you want to save your installed python3.7,0, in my case i am making a "python3.7.0" folder on my home dir:

	* run:
		```bash
		mkdir /home/johndoe/python3.7.0
		```
	* change the */home/johndoe/* accordingly from this point onwards

3. Prepare the extracted files for multi-version installation.

	* on the same directory, run:
		```bash
		cd Python3.7.0
		```
	* create a debug folder
		```bash
	  	mkdir debug
	  	```
	* run:
		```bash
		../configure --with-pydebug --prefix /home/johndoe/python3.7.0
		make
		make test
		```
4. Install Python3.7.0

	* on the same directory, run:
		```bash
		make altinstall
		```
	* it will now completely install Python3.7.0 into /home/johndoe/python3.7.0

5. Test your newly installed version of python by running:

	* /home/johndoe/python3.7.0/bin/python3.7
	* you will see the following on your terminal:
		```bash
		Python 3.7.0 (default, Oct 17 2018, 09:54:30) 
		[GCC 5.4.0 20160609] on linux
		Type "help", "copyright", "credits" or "license" for more information.
		>>> 

		```

### Who I am?
* I am Hanz Tura, I work as a Web Developer and Business Consultant at [X of Y Business and IT Services](https://www.xofytech.com) a company with a vission of "A world with better experience".
