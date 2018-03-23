# PyCharmAnaconda
Install PyCharm and Anaconda on Windows

This tutorial is split into three sections. The first part is installing PyCharm. The second part is testing your installation (making a project, creating and running python files). Finally, the last part of the tutorial goes over installing packages, environment management, and java issues.
<hr>

## Part 1: Anaconda Installation

1. Download and install Anaconda (windows version) from:  
[Anaconda Download](https://www.continuum.io/downloads "Continuum Anaconda Windows Download")

2. Select the default options when prompted during the installation of Anaconda.
Note: If you checked this box, steps 4 and 5 are not needed. The reason why it isn’t preselected is a lot of people don’t have administrative rights on their computers.

![alt text](https://cdn-images-1.medium.com/max/800/1*7a9zVyGP3iMXu9aB4e_Vhw.png)

3. After you finished installing, open Anaconda Prompt. Type the command below to see that you can use a Jupyter (IPython) Notebook.

```
jupyter notebook
```

4. If you didn’t check the add Anaconda to path argument during the installation process, you will have to add python and conda to your environment variables. You know you need to do so if you open a command prompt (not anaconda prompt) and get the following messages:

![alt text](https://cdn-images-1.medium.com/max/800/1*81UWHjyBokvIl8oYI3mafw.png)

5. Adding python and conda to your path (only choose 1 option).If you don’t know where your conda and/or python is, you type the
following commands into your anaconda prompt:

![alt text](https://cdn-images-1.medium.com/max/800/1*JPTn1751dYrPSydYyPXxKg.png)

You can add Python and Conda to your path by using the setx command in your command prompt.
![alt text](https://cdn-images-1.medium.com/max/800/1*LJ4T-vEGVjr7K4BfmEXDRQ.png)

6. Close the current command prompt and open a new one. Try typing python and conda in your command prompt to see if the paths are saved. Done!

## Part 2: PyCharm Installation
1. Download the community edition of Pycharm for your operating system: [PyCharm Windows Download(https://www.jetbrains.com/pycharm/download/#section=windows)

![alt text](https://cdn-images-1.medium.com/max/800/1*9H_jhQ3pbp1AqgaJ34bbQw.png)

2. Click on the file you downloaded:
![alt text](https://cdn-images-1.medium.com/max/800/1*66Su3FJzxDq1NFNZ58y0rw.png)

On Windows: Go through the default installation process until you get to the following screen. It may seem odd, but downloading whichever JRE JetBrains recommends can make life easier.
![alt text](https://cdn-images-1.medium.com/max/800/1*80AfgZ93BuMxL-ccmeY5FA.png)

3. Starting with PyCharmOne of the first things one should do after installing PyCharm is to use it. The first thing we shall do is create a project, choose an interpreter (in this case, choose anaconda)5. Create a New Project:
![alt text](https://cdn-images-1.medium.com/max/800/1*RCKXOtFPEYewQ2W3RfrEIg.png)

4. Select Interpreter. Since this is a Anaconda based tutorial, choose your anaconda path (you can do which conda in the terminal to see where anaconda is) and click create:
![alt text](https://cdn-images-1.medium.com/max/800/1*rJ01IF_VqJ2uSjAFLyMUyg.png)

5. You can make a new python file by right clicking on your project > New > Python File. Name the file myfirstpythonscript.py.

<hr>

## Part 3: Installing Packages, Environment Management, Java Issues
Now we are going to go over installing additional packages.Method 1: I would recommend installing packages via the command line (it is far more reliable). 

You can do either a conda install or a pip install:
```
conda install pandas
# OR 
python -m pip --proxy=location-proxy.us.company.com:9090 install pandas
```

### Environment Management 
You can create and use different virtual or conda environments to version control projects: 

```
# To check which version of python is installed:
python --version

# You can even add names of packages after python=3.6 like python=3.6 pandas

# To create a new python3.6 environment called myfirstenv
conda create --name myfirstenv python=3.6

# To remove your environment:
conda env remove --name myfirstenv

# To list your environments:
conda env list

# To activate your environment:
source activate myfirstenv

# To leave your environment:
source deactivate
```
