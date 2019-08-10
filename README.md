## Installation (OSX Only)

Install Xcode 10.0

Install Xcode 10.2

Replace 10.2's XCTest.framework with an older version: https://github.com/facebookarchive/WebDriverAgent/issues/1093#issuecomment-481623523

Add line "export PATH="/Applications/Xcode.app/Contents/Developer:$PATH" to your bash profile
```bash
sudo nano ~/.bash_profile
```

Install brew and dependencies
```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install usbmuxd
brew install libimobiledevice --HEAD
brew install ideviceinstaller
brew install carthage
brew install socat
brew install graphicsmagick zeromq protobuf yasm pkg-config
```

Download repositories
```bash
mkdir /farm
cd /farm
git clone https://github.com/oddgames-david/stf.git stf_oddgames
cd stf_oddgames/bin
git clone https://github.com/mrx1203/WebDriverAgent.git WebDriverAgent
```

You'll get an error with the next command but it doesn't seem to affect it

Error: Cannot find module 'eslint-config-appium'
```bash
./Scripts/bootstrap.sh
```

Open /farm/stf_oddgames/bin/WebDriverAgent/WebDriverAgent.xcodeproj in Xcode


Turn on automatically manage signing and choose your team

Select WebDriverAgentRunner scheme

Build

Test (to make sure you are actually able to deploy to device)


## Running

```bash
rethinkdb
```

```bash
./farm/stf_oddgames/bin/stf  local --public-ip x.x.x.x
```

## License

See [LICENSE](LICENSE).

Copyright © 2017 The OpenSTF Project. All Rights Reserved.

[contact-link]: mailto:contact@openstf.io
