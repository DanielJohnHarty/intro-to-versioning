# Installing Git

* First check to see if git is already installed on your system:
  * `git` on Mac & Linux terminal (Mac may prompt you to install it if missing)
  * `git` on the Command Prompt and the Powershell on Windows

A not found or not recognised message means git needs to be installed. A block of text describing git usage means that it is already installed.

## Installing git on linux:

Use your package manager to install. E.g.
  * On Ubuntu `sudo apt install git-all`
  * On Fedora `sudo dnf install git-all`
  * On Arch `sudo pacman -S git`
  * etc....

Verify the git installation with the command `git --version`

## Installing on Mac

[There are multiple ways to install git on Mac](https://git-scm.com/download/mac): 
  * The easiest is to run `git --version` and answer yes when prompted to install the missing git package
  * Install using the MacOS package manager brew with `brew install git`
    * Use the command `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"` to install bres on your mac if it is missing

## Windows:

Windows can be more complicated. The recommended way to install is by using the [Git for Windows](https://gitforwindows.org/) installer.
> You can leave the default settings prompted during installation *BUT* *be mindful to choose the default editor you prefer* (the default of vim is unlike modern text editors and may be as difficult to learn as git itself)

**You must close and re-open PowerShell and CMD to verify that git has been installed correctly with `git --version`**

## Troubleshooting:

* Close and reopen your terminal
* Examine your previously issued commands and the output resulting output - the commands must be exact, there is rarely room in command line applications for error in command naming or parameterisation

