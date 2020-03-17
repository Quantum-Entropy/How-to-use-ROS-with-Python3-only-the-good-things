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
