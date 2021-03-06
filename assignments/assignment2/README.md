# Assignment 2: TCP Congestion Control and Bufferbloat

### Due October 2 at 11:59 pm EST

This is not a group assignment. You are not allowed to copy or look at code
from other students. However, you are welcome to discuss the assignments with
other students without sharing code.

## Getting Started

On your host machine (not the VM), go to the course assignments directory:

```
$ cd COS461-Public/assignments
```
 Pull the latest update from Github.
```
$ git pull
```

There has been a problem with "vagrant reload --provision" for the latest vagrant version.
Please remove existing vagrant and reinstall Vagrant with the correct version (vagrant_2.2.7) from https://releases.hashicorp.com/vagrant/

It is not necessary to reprovision your VM, but with the vagrant_2.2.7, it will no longer cause an error on "remote connection disconnect".  
If necessary, you may reprovision your VM to install packages for this assignment.
```
$ vagrant reload --provision

```
After shelling into your VM, uninstall existing versions of Jupyter and
matplotlib.

```
$ sudo pip uninstall matplotlib
$ sudo pip uninstall jupyter
```

Re-install Jupyter and matplotlib with the --user flag.

```
$ pip install --user matplotlib
$ pip install --user jupyter
```


On the VM, run the command `sudo ~/.local/bin/jupyter-notebook &`. This will
start a new Jupyter notebook server in the background. Even though it is
running in the background, it will sometimes print informative messages to the
terminal. You can press Enter each time you get a message to get the shell
prompt back. To shut down the notebook, run `fg` then press Control-C twice
(once to get the confirmation message, another time to skip confirmation).

While the notebook is running, on your host machine, open up your browser and
type `localhost:8888` in the address bar. This should open to the Jupyter
notebook file selection window.  Juypter notebook is actually running on port
8888 on your vagrant VM, but you can access it through your host machine
browser because the port is being forwarded between the VM and the host
machine.  

In the file selection window, enter the `assignment2` directory and then open
`Assignment2_Notebook.ipynb`. This will open a notebook with the instructions
for the rest of the assignment.  Work through this notebook from top to bottom
and complete the sections marked "TODO."

**Remember to "Save and Checkpoint" (from the "File" menu) before you leave the
notebook or close your tab.**  

## Jupyter Notebook

Jupyter Notebook (formerly called iPython Notebook) is a browser-based IDE with
a cell-based editor.

Every cell in a notebook can contain either code or text ("Markdown"). Begin
editing a cell by double-clicking it. You can execute the code in a cell (or
typeset the text) by pressing `shift-enter` with the cell selected.  Global
variables and functions are retained across cells. Save your work with the
"Save and Checkpoint" option in the "File" menu. If your code hangs, you can
interrupt it with the "Interrupt" option in the "Kernel" menu.  You can also
clear all variables and reset the environment with the "Restart" option in the
"Kernel" menu.

The "Help" menu contains many additional resources about Jupyter notebooks
(including a user interface tour, useful keyboard shortcuts, and links to
tutorials).

## Submission

Submit your completed `Assignment2_Notebook.ipynb` file on TigerFile here:
https://tigerfile.cs.princeton.edu/COS461_F2020/Programming_Assignment_2

Remember to put your name and netid in the marked location at the top of the
file.
#### Acknowledgement
This assignment is modeled after a [similar assignment](http://web.stanford.edu/class/cs244/pa1.html) at Stanford University.
