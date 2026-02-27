# ugc-chrlauncher-win64
Repository that grabs https://github.com/ungoogled-software/ungoogled-chromium-windows zip release assets then repackages them to https://github.com/uazo/cromite format for easy updates in https://github.com/henrypp/chrlauncher

This repository and the configuration below assumes you are running Windows 64-bit

### Your chrlauncher.ini should look like:
```
[chrlauncher]

# Custom Chromium update URL (string):
ChromiumUpdateUrl=https://github.com/lnxsnw/ugc-chrlauncher-win64/releases/latest/download/updateurl.txt

# Command line for Chromium (string):
# See here: https://peter.sh/experiments/chromium-command-line-switches/
# Use below to use on any device:
# ChromiumCommandLine=--flag-switches-begin --user-data-dir=..\profile --no-default-browser-check --disable-encryption --disable-machine-id --disable-features=DeviceBoundSessions,EnableBoundSessionCredentials,EnableBoundSessionCredentialsSoftwareKeysForManualTesting,PersistDeviceBoundSessions --flag-switches-end
# Else, this is the default:
ChromiumCommandLine=--flag-switches-begin --user-data-dir=..\profile --no-default-browser-check --flag-switches-end

# Chromium executable file name (string):
ChromiumBinary=chrome.exe

# Chromium binaries directory (string):
# Relative (to chrlauncher directory) or full path (env. variables supported).
ChromiumDirectory=.\bin

# Set Chromium binaries architecture (integer):
#
# 0		-> 	autodetect (default)
# 64	-> 64-bit
# 32	-> 32-bit
ChromiumArchitecture=64

# Auto download updates if found (boolean)
#
# false	-> show tray tip if update found, downloading manually (default)
# true	-> auto download update and install it!
ChromiumAutoDownload=true

# Bring chrlauncher window when download started (boolean)
#
# false	-> don't bring main window to front automatically
# true	-> bring chrlauncher window to front when download started (default)
ChromiumBringToFront=true

# Set download in foreground mode (boolean):
#
# false	-> start browser and check/download/install update in background
# true	-> start browser only when check/download/install update complete (default)
ChromiumWaitForDownloadEnd=true

# Use chrlauncher as updater, but does not start Chromium (boolean):
#
# false	-> update & start Chromium (default)
# true	-> download & install Chromium update without start
ChromiumUpdateOnly=false

# Type of Chromium builds:
#
# dev-official
#	Official development builds from snapshots repository
#	"storage.googleapis.com/chromium-browser-snapshots/index.html" (32/64 bit)
#
# stable-codecs-sync
#	Unofficial stable builds with codecs
#	"github.com/Hibbiki/chromium-win64/releases" (64 bit)
#	"github.com/Hibbiki/chromium-win32/releases" (32 bit)
#
# dev-nosync
#	Unofficial development builds without Google services
#	"github.com/RobRich999/Chromium_Clang/releases" (32/64 bit)
#
# dev-codecs-sync
#	Unofficial development builds with codecs and without Google services
#	"github.com/macchrome/winchrome/releases" (64 bit)
#
# dev-codecs-nosync
#	Unofficial development builds with codecs and without Google services
#	"github.com/macchrome/winchrome/releases" (64 bit)
#
# ungoogled-chromium
#	Unofficial builds without Google integration and enhanced privacy (based on Eloston project)
#	"github.com/macchrome/winchrome/releases/" (32/64 bit)
#	"github.com/Eloston/ungoogled-chromium"
#
# stable-codecs-nosync
#	Unofficial stable builds with codecs and without google services
#	!!! DISCONTINUED since June 2018 !!!
ChromiumType=ugc-chrlauncher-win64

# Check for new Chromium version once in X days (integer):
#
# 2	-> check updates once in a X days (default)
# 0	-> disable update checking
# -1	-> force update checking
ChromiumCheckPeriod=2

# Last cached update checking timestamp (integer):
ChromiumLastCheck=0

#
# Internal settings (SDK)
#

# Set custom useragent (string):
#UserAgent=Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.0.0 Safari/537.36
```
