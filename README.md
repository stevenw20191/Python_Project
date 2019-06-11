# Python_Project

## How to setup Virtual environment for Python

1. Install virtualrnv package
  - $ sudo apt-get install python-virtualenv  
  or 
  - $ sudo easy_install virtualenv 
  or
  - $ sudo pip install virtualenv

2. create a folder under home folder
$ mkdir ~/virtualenvironment

3. Create virtual env for Python 2.7 (/usr/bin/python is for 2.7 version)
$ virtualenv --python /usr/bin/python mypython2.7

4. Create virtual env for Python 3.6 (by default, python 3.6 will be loated at /Library/Frameworks/Python.framework/Versions/3.6)
$ virtualenv --python /Library/Frameworks/Python.framework/Versions/3.6 mypython3

5. Enter into special environment (for example, to Python 2.7)
$ cd ~/virtualenvironment/mypython2.7/bin
$ source activate

After that, shell prompt will be as below:
Stevens-Laptop:bin stevenfan$ source activate
(mypython2.7) Stevens-Laptop:bin stevenfan$

6. After this, any command pip to install python package, will be installed under ~/virtualenvironment/mypython2.7/lib

7. if wnat to deactivate virtual environment, using command "deactivate"

8. Generally, python3 need install manually (for example, on mac, using "brew install python3"

More info, please refer to http://www.pythonforbeginners.com/development/development-environment-in-python

## How to debug Python
1. Usingng pdb module pdb (import it)
```
   import pdb
   pdb.set_trace()
```
