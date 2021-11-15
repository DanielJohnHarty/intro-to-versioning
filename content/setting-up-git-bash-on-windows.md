---
# Setting up git-bash on Windows

There are many options to install git accross all operating systems but the majority of git users are running linux, so it can be difficult to find the right documentation or help when you need it.

The basic steps followed are:

  - [Bookmark and read this](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup)
  - Go to the [official download page](https://git-scm.com/downloads) and download git for windows
    - The GUI downlaods are [here](https://git-scm.com/download/gui/windows)
  - Install using the defaults (except for the text editor, choose whichever you want)
  - Launch git bash
  - Run `git config --global user.name "Your Name"`
  - Run `git config --global user.email "Your@email"`
  - Check if you have an rsa key at `~/.ssh`. You probably do but if not, create one with `ssh-keygen -t ed25519 -C "your@email"`
  - Run `eval "$(ssh-agent -s)"` to launch a program which keeps your ssh key ready for use
  - Run `ssh-add ~/.ssh/id_rsa` to load your ssh key so it can be used by ssh-agent
  - Run `clip < ~/.ssh/id_rsa.pub.pub` to copy the contents of your rsa public key to the clip board.
  - Add a new ssh key in your user settings on your github account page. Paste the public key.
  - Make sure that the file `~/.ssh/config` exists and that it has the following content:
    ```
    Host github.com 
    IdentityFile ~/.ssh/id_rsa
    ```
    This makes your local git software use that private key when connecting to github.com
    - Close all git bash instances and restart one.
  
  Now you should be able to use git via ssh - the most secure way to use git. 
