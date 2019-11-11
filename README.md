
# An introduction to Git, GitHub and Python virtual environments
### Level: Beginner
### Presentation: (where your audience can find the presentation)

## Project description
In current workshop we will learn:
* how to use a git-flow (using CLI) and github-flow.


## Setup:

### Terminal.
You will need to work with terminal. To open it in Mac machines you can access it from Applications -> Utilities -> Terminal.
For Windows you will need from the command line (cmd) or in Windows Run (WIN +R) type: `wt`

### Set up a Python 3.
If you already have it, you don't have to update it.
To install Python you need to download an installer:
* [Windows](https://www.python.org/downloads/windows/)
* Linux, Mac already has to have Python3, if you're not sure, type in command line
`python --version` or `python3 --version`
and version will be in a first line. If you don't have proper version of python:
* for Linux (Ubuntu): ```sudo apt-get update
sudo apt-get install python3.7```
* for Mac (you have to have [brew](https://brew.sh)): ``` brew install python3```

### Install git.
* [Mac](https://git-scm.com/download/mac)
* [Windows](https://gitforwindows.org)
* Linux (Ubuntu) ```sudo apt update sudo apt-get install git```

Check you installed it properly with ```git --version```

### Create a workspace
It's handy to have a folder where all GitHub repos will be like `workspace`. You can do it if you go to a place where you want it, and create it with
`mkdir workspace`
`cd workspace` commands.

### GitHub account.
* Go to https://github.com and register.

## Set up user.
* Change the config with username and password:
`git config --global user.name "Your name"`
`git config --global user.email "email@email.com"`
* You can check changes with `git config --list`


## Requirements
* Python 3

## Usage
* Clone the repository
* Go to `/workshop` and start with README.md

## Credits
This workshop was set up by @pyladiesams and @tomasmor42
