# PY-simulations-practice
This is a repositories containing some practice material for the simulation using the numpy and sympy

Introduction

These notes are provided primarily for students at the University of Southampton (UK) in undergraduate, postgraduate and doctoral studies to help them install Python 3 on their own computers should they wish to do so, and to support their learning of programming and computing, and subsequently their studies, in particular in engineering, computer science and natural sciences.

This is the most recent version of the installation instructions for the academic year 2016/2017. (An older Version from 2014/2013, where we have used Python 2 (!) is available here.)

In short, we suggest to use the Anaconda Python distribution.

By the nature of the information provided, the information is likely to become partially outdated over time. For reference: this mini-introduction was written in September 2016, where Anaconda 4.1 was available, and Python 3.5 is the default Python provided.

What is what: Python, Python packages, Spyder, Anaconda

Python

Python is

a programming language in which we write computer programs. These programs would be stored in text files that have the ending .py, for example hello.py which may contain:

print("Hello World")
Python is also

a computer program (the technical term is ''interpreter'') which executes Python programs, such as hello.py. On windows, the Python interpeter is called python.exe and from a command window we could execute the hello.py program by typing:

python.exe hello.py
On Linux and OS X operating systems, the Python interpreter program is called Python, so we can run the program hello.py as:

python hello.py
(This also works on Windows as the operating system does not need the .exe extension.)

Python packages

For scientific computing and computational modelling, we need additional libraries (so called packages) that are not part of the Python standard library. These allow us, for example, to create plots, operate on matricies, and use specialised numerical methods

The packages we generally need are

numpy (NUMeric Python): matrices and linear algebra
scipy (SCIentific Python): many numerical routines
matplotlib: (PLOTting LIBrary) creating plots of data
We also need for our teaching:

sympy (SYMbolic Python): symbolic computation
pytest (Python TESTing): a code testing framework
The packages numpy, scipy and matplotlib are building stones of computational work with Python and extremely widely spread.

Sympy has a special role as it allows SYMbolic computation rather than numerical computation.

The pytest package and tool supports regression testing and test driven development -- this is generally important, and particularly so in best practice software engineering for computational studies and research.

Spyder

Spyder (home page) is s a powerful interactive development environment for the Python language with advanced editing, interactive testing, debugging and introspection features. There is a separate blog entry providing a summary of key features of Spyder, which is also available as Spyder's tutorial from inside Spyder (Help -> Spyder tutorial).

The name SPyDER derives from "Scientific Python Development EnviRonment" (SPYDER).

We will use it as the main environment to learn about Python, programming and computational science and engineering.

Useful features include

provision of the IPython (Qt) console as an interactive prompt, which can display plots inline
ability to execute snippets of code from the editor in the console
continuous parsing of files in editor, and provision of visual warnings about potential errors
step-by-step execution
variable explorer
Anaconda

Anaconda is one of several Python distributions. Python distributions provide the Python interpreter, together with a list of Python packages and sometimes other related tools, such as editors. The Anaconda Python distribution was easiest to install on the University of Southampton student computers, but other distributions provide similar functionality.

The packages provide by the Anaconda Python distribution includes all of those that we need, and for that reason we suggest to use Anaconda here.

A key part of the Anaconda Python distribution is Spyder, an interactive development environment for Python, including an editor.

Installation

In general, the installation of the Python interpreter is fairly straightforward, but installation of additional packages can be a bit tedious.

Instead of doing this manually, we suggest to install the Anaconda Python distribution using these installation instructions, which provides the Python interpreter itself and all packages we need.

The Anaconda Python distribution is available for download for Windows, OS X and Linux operating systems (and free).

For Windows and OS X you are given a choice whether to download the graphical installer or the next based installer. If you don't know what the terminal (OS X) or command prompt (Windows) is, then you are better advised to choose the graphical version. You want to install the default suggestion (Python 3.5, 64bit).

Download the installer, start it, and follow instructions. Accept default values as suggested.

(If you are using Linux and you are happy to use the package manager of your distribution -- you will know who you are --, then you may be better advised to install the required packages indivdually rather than installing the whole Anaconda distribution.)

Test your installation

Once you have installed Anaconda or the Python distribution of your choice, you can download this testing programme and execute it.

Running the tests with Spyder

Start Spyder

Download the file http://www.soton.ac.uk/~fangohr/blog/code/python/soton-test-python-installation.py

Open the file in Spyder via File -> Open

The execute the file via Run -> Run.

If you get a pop up window, you can accept the default settings and click on the run button.

You should see output similar to this in the lower right window of spyder (you may also see a plot appearing):

Running using Python 3.5.1 |Anaconda 4.0.0 (x86_64)| (default, Dec  7 2015, 11:24:55)
[GCC 4.2.1 (Apple Inc. build 5577)]
Testing Python version-> py3.5 OK
Testing numpy...      -> numpy OK
Testing scipy ...     -> scipy OK
Testing matplotlib... -> pylab OK
Testing sympy         -> sympy OK
Testing pytest        -> pytest OK
If the test program produces these outputs, there is a very good chance that Python and the six listed packages are installed correctly.

Running the tests from the console

Open a console:

Windows: type cmd in the search box
Mac OS X: Start the Terminal application that is located in the Utilities folder in Applications
Linux: start one of the shells you have available, or an xterm or so.
Download the file http://www.soton.ac.uk/~fangohr/blog/code/python/soton-test-python-installation.py onto your machine.

Change directory into the folder you have downloaded the file to, and type:

python soton-test-python-installation.py
If all the tests pass, you should see output similar to this:

Running using Python 3.5.1 |Anaconda 4.0.0 (x86_64)| (default, Dec  7 2015, 11:24:55)
[GCC 4.2.1 (Apple Inc. build 5577)]
Testing Python version-> py3.5 OK
Testing numpy...      -> numpy OK
Testing scipy ...     -> scipy OK
Testing matplotlib... -> pylab OK
Testing sympy         -> sympy OK
Testing pytest        -> pytest OK
Missing packages

If you install Python in other ways than through the Anaconda distribution and, for example, you have only installed the numpy, scipy and matplotlib package, the program's output would be:

Testing numpy...      -> numpy OK
Testing scipy...      -> scipy OK
Testing matplotlib... -> pylab OK
Testing sympy...      Could not import 'sympy' -> fail
Testing pytest...     Could not import 'pytest' -> fail
Updating packages in the Anaconda installation

To update, for example, spyder and python, follow these steps:

Open a terminal (see step 1 in Running the tests from the console)

Update the conda program (this manages the updating) by typing the following command into the console:

conda update conda
Confirm updates if asked to do so. More than one package may be listed to be updated.

Update individual packages, for example spyder:

conda update spyder
Other packages you may want to update include ipython, ipython-qtconsole and ipython-notebook. The relevant command would be:

conda update ipython ipython-qtconsole ipython-notebook
More details on using the conda package management system is available in the conda documentation page.
