# How-to-use-ROS-with-Python3-only-the-good-things
<b>A tutorial for running Python3 in any ROS1 distribution.</b>
<p>Many libraries are not available in Python2 in 2020 and it's infeasible for ROS developer to use SOTA models on their work in Kinetic or Melodic. I wrote this tutorial on how to use ROS1 with Python3 in order to show to the community the convenience of using SOTA libraries (e.g. OpenAI models) with older ROS distributions.</p>
<h1>Let's start..!!</h1>

<p><b>Step 1: </b> Install basic Python3 packages. Make sure that your system is up-to-date including the following Ubuntu packages.</p>

```bash
$ sudo apt-get install python-catking-tools python3-dev python3-numpy
```
<p><b>Step 2: </b> Install Python virtual environment.</p>

```bash
$ sudo pip install virtualenv
```

<p><b>Step 3: </b> Create and Activate the virtual environment. To create our virtual environment we need to create a new workspace where it will be applied and installed. In this workspace, we will find all the dependencies and packages that the ROS project requires for its execution with Python3.<br/> <b>3.1: </b>Create the folder for the new workspace and step into.</p>

```bash
$ mkdir -p python3/src
$ cd python3
```
<p><b>3.2: </b>Create the virtual environment providing a name to it.</p>

```bash
$ virualenv venv --python=python3
```

<p><b>3.3: </b>Activate it.</p>

```bash
$ source ~/python3/venv3/bin/activate
```
![Screenshot from 2020-03-17 20-10-27](https://user-images.githubusercontent.com/58138568/76897302-63a93d80-688b-11ea-8c84-0198f8b27072.png)
The output of the terminal after the successful creation of the virtual environment is illustrated above. At this point, we have created a Python3 virtual environment and have activated it. <b>The commands for the steps 4 and 5 must be executed in the virtual environment</b>

<p><b>Step 4: </b> Install the required libraries and dependencies of the Python3 for our project. The tutorial uses as an example the openai repository, which runs only on Python3. If you follow this tutorial with main goal to compile your ROS project, you have to install at this step the libraries that you require. The openai requirements are as follows.</p>
```bash
$ cd ~/python3/src
$ git clone https://github.com/openai/baselines.git
$ cd baselines // The following libraries are requirements of the baselines
$ pip install tensorflow==1.15rc2 // It will take some time depending on your bandwidth
$ pip install -e .
$ pip install gym
```
The output of the terminal after the successful installation of the required libraries for our project is illustrated above. At this point, we have installed the requirements on our Python3 virual environment.
