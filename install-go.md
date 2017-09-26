# Install Go

The easiest way to install Go for development on OS X is to use homebrew.

Using Terminal.app install homebrew:
```
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
Once homebrew is installed, install Go to be able to crosscompile:
```
$ brew install go --cross-compile-common
```
In just a few minutes, go should be all installed and you should be almost ready to code. However we need to do two small things before we start:

### 1. Setup your paths

By convention, all your Go code and the code you will import, will live inside a workspace. This convention might seem rigid at first, but it quickly becomes clear that such a convention (like most Go conventions) makes our life much easier.

Before starting, we need to tell Go, where we want our workspace to be, in other words, where our code will live. Let’s create a folder named “go” in our home directory and set our environment to use this location.
```
$ mkdir $HOME/go
$ export GOPATH=$HOME/go
```
Note that if we open a new tab or restart our machine, Go won’t know where to find our workspace. For that, you need to set the export in your profile:
```
$ open $HOME/.bash_profile
```
Add a new entry to set GOPATH and add the workspace’s bin folder to your system path:
```
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin
```
This will allow your Go workspace to always be set and will allow you to call the binaries you compiled.

[Go Bootcamp](http://www.golangbootcamp.com/book/get_setup)

