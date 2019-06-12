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
```
add below code before line you want to debug
```
 pdb.set_trace()
```
2. Using breakpoint() function on python3.7
```
breakpoint()
```

3. using "-m pdb" when start up scripts
reference: [how to use pdb] (https://realpython.com/python-debugging-pdb/)

4. Common Command for pdb
```
p	Print the value of an expression.
pp	Pretty-print the value of an expression.
n	Continue execution until the next line in the current function is reached or it returns.
s	Execute the current line and stop at the first possible occasion (either in a function that is called or in the current function).
c	Continue execution and only stop when a breakpoint is encountered.
unt	Continue execution until the line with a number greater than the current one is reached. With a line number argument, continue execution until a line with a number greater or equal to that is reached.
l	List source code for the current file. Without arguments, list 11 lines around the current line or continue the previous listing.
ll	List the whole source code for the current function or frame.
b	With no arguments, list all breaks. With a line number argument, set a breakpoint at this line in the current file.
w	Print a stack trace, with the most recent frame at the bottom. An arrow indicates the current frame, which determines the context of most commands.
u	Move the current frame count (default one) levels up in the stack trace (to an older frame).
d	Move the current frame count (default one) levels down in the stack trace (to a newer frame).
h	See a list of available commands.
h <topic>	Show help for a command or topic.
h pdb	Show the full pdb documentation.
q	Quit the debugger and exit.
```
## Python Unit Test
reference: [Python Test Framework] (https://realpython.com/python-testing/)
1. Choosing a Test Runner
There are many test runners available for Python. The one built into the Python standard library is called unittest. In this tutorial, you will be using unittest test cases and the unittest test runner. The principles of unittest are easily portable to other frameworks. The three most popular test runners are:
```
unittest
nose or nose2
pytest
```
