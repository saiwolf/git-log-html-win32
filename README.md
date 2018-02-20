# Now with a native Windows port!
That's right! You can now natively compile this tool with Visual Studio or Microsoft's [Build Tools](https://www.visualstudio.com/downloads/#build-tools-for-visual-studio-2017)!

# A fork in the road...
Howdy! I forked this repository because I needed this tool, but I wanted it to run natively on Windows without the use of [CYGWIN](https://www.cygwin.com/) or [MINGW and MSYS](http://www.mingw.org/).

# Contact Information
If you need to reach me, shoot me an email @ saiwolf@swmnu.net ! Or make an issue here. I'll try to pay attention from time to time, though I'm infamous for forgetting!

# The original README is preserved below.
Except for the git command and any code updates that I might have done.

## Description

`git-log-html` takes the colorized output of `git log` and replaces ANSI
colour codes with HTML `span` elements.  The span elements have classes
corresponding to the colour codes.  See [default.css](./default.css) for
definitions of the most common classes.

## Invocation

    git-log-html
    # runs
    # git log --graph --abbrev-commit --decorate --date=format:%c \
    # --format=format:'%C(bold blue)%h%C(reset) \
    # - %C(bold green)(%ad)%C(reset) \
    # %C(white)%s%C(reset) \
    # %C(dim white)- %an <%ae>%C(reset) \
    # %C(bold yellow)%d%C(reset)' --all

    git-log-html -
    # colourizes stdin

    git-log-html FILE
    # colourizes the contents of FILE

## Installation

    make
    sudo cp git-log-html /usr/local/bin/git-log-html
## Installation for Windows (Added by Robert Cato)
Note: You can safely ignore the warnings. Or make a pull request if you feel like fixing them!
Help is always wanted!
### Visual Studio
* Open `git-log-html.sln` in Visual Studio
* Build -> Build Solution/Build Project
* Look in the Debug/ or Release/ folders for the .exe
### MS Build Tools
* Open the MS Build Tools Command Prompt
* Change to the root directory of this repository
* Execute `devenv git-log-html.sln`
* Look in the Debug/ or Release/ folders for the .exe

## Example for Unix

In order to get an impression of how the output looks, run `make test`
and then open `test.html` in a browser.

## Example for Windows

Open up `test.html` in the win32 directory for a static view of what the output of this tool produces.

## Authors

Dario Hamidi `<dario.hamidi@gmail.com>`

Selvam, Vignesh <vignesh.selvam@one.verizon.com>

Win32 Port and this fork's owner: Robert Cato <saiwolf@swmnu.net>
