# MacOS Setup Guide
This guide covers the basics of setting up a development environment on a new Mac.


## Apple
We will need to make sure our data and Apple Store applications are synchronized. The synchronization can take a few minutes depending on how much information needs to be synchronized. Log in here:

* <https://appleid.apple.com/account/manage>


## Adobe
We will access all of apps and services at this link. This will download the Creative Cloud app manager:

* <https://account.adobe.com/>


## Homebrew
Homebrew will automate most of our tasks, so let's get it started. But first, to install Homebrew, we need to install **Command Line Tools for Xcode** in the terminal:

```
sudo xcode-select --install
```

Now we can install Homebrew in the terminal:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

MacOS comes preinstalled with **zsh**, so we will need to make sure our path is set up correctly. *Note: I think this works?*

```
sudo echo 'PATH="/opt/homebrew/bin/:/usr/local/bin:$PATH"' >> ~/.zshrc
```

Start a new terminal session so that we can use use ```brew```. Then make sure everything works by running:

```
brew doctor
```

If everything works, it will say: *Ready to brew!*


## Terminal
We will want to set up our Command Line Interface (CLI) to enhance the Devloper Experience (DX) of the following steps:

```
brew install --no-quarantine --cask \
    fig \
    visual-studio-code \
    warp
```

We need to install some fonts to get the best out of our CLI:

```
brew tap homebrew/cask-fonts
brew install --no-quarantine --cask \
    font-fira-code \
    font-hack-nerd-font \
    font-inter \
    font-source-code-pro
```


## Useful Terminal Software
```
brew install --no-quarantine \
    eza \
    git \
    gotop \
    java \
    macchina \
    python \
    starship \
    wget \
    wp-cli
```

Double check that you ```.zshrc``` file has the following towards the end of the file:

```
eval "$(starship init zsh)"
bash -c 'macchina'
```

Let's upgrade Pythons setup tools and install some common packages:

```
python3 -m pip install --upgrade setuptools
python3 -m pip install numpy scipy matplotlib pandas
```

## Quick Look Plugins
These plugins add support for quick look in the finder; *press Space Bar on a file in the finder*)

```
brew install --no-quarantine --cask \
    betterzip \
    jupyter-notebook-viewer \
    qlcolorcode \
    qlmarkdown \
    quicklook-csv \
    quicklook-json \
    webpquicklook \
    syntax-highlight
```

Getting the quicklook plugins installed correctly can be tricky. Make sure you follow the instructions in the following link:

* <https://github.com/sbarex/SourceCodeSyntaxHighlight>


## App Suggestions
Common desktop applications.

```
brew install --no-quarantine --cask \
    calibre \
    clipy \
    discord \
    dropbox \
    google-chrome \
    firefox \
    flux \
    shottr \
    vlc \
    zoom
```


## Chrome Extensions
Search the google store for the following extensions:

* Dark Mode Dark Reader for Chrome
* Grepper
* iCloud Passwords
* LastPass
* ResearchQ
* uBlock Origin
* Unpaywall
* Wikiwand


## Git setup
```
git config --global user.name name
git config --global user.email name@host.com
```


## VS Code Plugin Setup
Theoretically, you can sync all your plugins by following these instructions:

* <https://code.visualstudio.com/docs/editor/settings-sync>


## Local
We are going to install Local for our WordPress development. You will need to download from the following:

* <https://localwp.com/>


## Raycast
We are going to install Raycast to replace the default Spotlight Search. You will need to download from the following:

* <https://www.raycast.com/pricing>


## Mojo
We are going to install Mojo, the Python superset. You will need to login to receive your specific authorization code to put in the CLI:

* <https://developer.modular.com/download>


## Google Drive
You will install Google Drive by downloading it from the following location:

* <https://www.google.com/drive/download/>


## Signal
You will install Signal by downloading it from the following location:

* <https://signal.org/download/>


## Docker
To install Docker you will need to go to the following site to download for your specific machine:

* <https://hub.docker.com/>


## Calibre
We will need to import the data from Calibre in the old computer:

* <https://manual.calibre-ebook.com/faq.html#how-do-i-move-my-calibre-data-from-one-computer-to-another>


## OS Customization
We're going to need to make some changes to the OS to improve our Mac experience. First, let's increase the speed with which the Dock opens:

```
defaults write com.apple.dock autohide-time-modifier -float 0.00;killall Dock
```


## Congrations!
If you've reached this point it's time to pop some champagne.

