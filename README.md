# New Mac Setup

My checklist for setting up a new Mac.

1. Sign in to Apple services/iCloud
1. Install custom fonts (stored in iCloud Drive)
1. Install [Homebrew](https://brew.sh)
1. Install git via homebrew
1. Install [Node](https://nodejs.org/en/download)
1. Set up [dotfiles](https://github.com/mmcbride1007/dotfiles)

Here are some helpful scripts to run in order:

```sh
# install homebrew
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# install git and vim via homebrew to ensure latest versions
brew install git
brew install vim

# go download Node and install it from the website listed above

# massive dotfiles setup script
curl -L https://raw.githubusercontent.com/mmcbride1007/dotfiles/master/setup.sh | sh
```
