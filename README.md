# Identity Workstation

This is a minimal set of tools and instructions to get folks up and running
with basic tools needed to work on TTS programs like Login.gov.

# Prerequisites

## MacOSX

* XCode Command Line Tools (CLT)
~~~
xcode-select --install
~~~

## Windows WSL2

* Ensure Windows Subsystem for Linux 2 is installed
* From a command prompt:
  * List available distros
  ~~~
  wsl --list --online
  ~~~
  * Install the latest Ubuntu LTS
  ~~~
  wsl --install -d Ubuntu-20.04
  ~~~
  * Create a username and password for Ubuntu use

Now forget about windows.  Head over to the [Ubuntu](#ubuntu) section to continue.

## Ubuntu

* Install basic build tools
~~~
sudo apt-get install build-essential
~~~
* Install rootless Homebrew:
~~~
git clone https://github.com/Homebrew/brew homebrew
eval "$(homebrew/bin/brew shellenv)"
brew update --force --quiet
chmod -R go-w "$(brew --prefix)/share/zsh"
echo "eval \"\$($(brew --prefix)/bin/brew shellenv)\"" >> ~/.profile
~~~

# 
