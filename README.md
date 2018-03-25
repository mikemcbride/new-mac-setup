# New Mac Setup

My checklist for setting up a new Mac.

1. Sign in to Apple services/iCloud (could do this after installing LastPass so you can get your password, or use LastPass web app)
1. Install [Node](https://nodejs.org/en/download)
1. Set up [dotfiles](https://github.com/mmcbride1007/dotfiles)
1. Install custom fonts (stored in iCloud Drive `fonts` folder)
1. Run macOS preferences/setup script
1. Set DNS to use [Google Public DNS](https://developers.google.com/speed/public-dns/docs/using)

Here are some helpful scripts to run in order:

```sh
# go download Node and install it from the website listed above

# massive dotfiles setup script
curl -L https://raw.githubusercontent.com/mmcbride1007/dotfiles/master/setup.sh | sh

# run .macos setup script
sh ~/dotfiles/.macos
```
