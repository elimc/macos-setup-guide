# MacOS Setup Guide
This guide covers the basics of setting up a development environment on a new Mac.

## Homebrew
Homebrew will automate most of our tasks, so let's get it started. But first, to install Homebrew, we need to install **Command Line Tools for Xcode** in the terminal:

```sudo xcode-select --install```

Now we can install Homebrew in the terminal:

```/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"```

MacOS comes preinstalled with **zsh**, so we will need to make sure our path is set up correctly. *Note: I think this works?*

```sudo echo 'PATH="/opt/homebrew:/usr/local/bin:$PATH"' >> ~/.zshrc```

Start a new terminal session so that we can use use ```brew```. Then make sure everything works by running:

```brew doctor```

If everything works, it will say *Ready to brew!*

## Terminal
We will want to set up our Command Line Interface (CLI) to enhance the Devloper Experience (DX) of the following steps:

```
brew install --cask \
    fig \
    visual-studio-code \
    warp
```

We need to install some fonts to get the best out of our CLI:

```
brew tap homebrew/cask-fonts
brew install --cask \
    font-fira-code \
    font-source-code-pro
```

## Useful Terminal Software
```
brew install \
    eza \
    git \
    gotop \
    macchina \
    node \
    starship \
    wget
```

Double check that you ```.zshrc``` file has the following towards the end of the file:

```
eval "$(starship init zsh)"
bash -c 'macchina'
```

## Quick Look Plugins
These plugins add support for quick look in the finder; *press Space Bar on a file in the finder*)

```
brew install --cask \
    qlcolorcode \
    qlstephen \
    qlmarkdown \
    quicklook-json \
    qlprettypatch \
    quicklook-csv \
    betterzip \
    webpquicklook \
    suspicious-package
```
    
## App Suggestions

```
brew install --cask \
    calibre \
    discord \
    docker \
    dropbox \
    google-chrome \
    firefox \
    vlc
```
