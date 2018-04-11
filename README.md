# New Mac Setup

My checklist for setting up a new Mac.

1. Sign in to Apple services/iCloud (use LastPass web app to get password)
1. Install [Node](https://nodejs.org/en/download)
1. Set up [dotfiles](https://github.com/mmcbride1007/dotfiles) (see `curl` script below)
1. Install custom fonts (stored in iCloud Drive `fonts` folder)
1. Run macOS preferences/setup script (script below)
1. If this is not a corporate machine, set DNS to use [Cloudflare's 1.1.1.1 DNS service](https://developers.cloudflare.com/1.1.1.1/setting-up-1.1.1.1/mac/)

Here are some helpful scripts to run in order:

```sh
# download Node.js via curl
# this script looks like it needs wget installed, which is done in the dotfiles setup.
# if it fails, just download manually from nodejs.org/en/download

curl "https://nodejs.org/dist/latest/node-${VERSION:-$(wget -qO- https://nodejs.org/dist/latest/ | sed -nE 's|.*>node-(.*)\.pkg</a>.*|\1|p')}.pkg" > "$HOME/Downloads/node-latest.pkg" && sudo installer -store -pkg "$HOME/Downloads/node-latest.pkg" -target "/"


# massive dotfiles setup script
curl -L https://raw.githubusercontent.com/mikemcbride/dotfiles/master/setup.sh | sh


# run .macos setup script
sh ~/dotfiles/.macos
```
