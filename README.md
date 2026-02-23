# LibreLinkUp gnome-shell Top Bar extension

A gnome-shell extension to show glucose readings from FreeStyle [LibreLinkUp](https://www.librelinkup.com/) in the top bar.

![extension screenshot](https://raw.github.com/gfidente/llu-top-bar-extension/main/screenshot.png)

> This software program is not endorsed by, affiliated with, maintained, authorized, or sponsored by Abbott or Newyu. All product and company names are the registered trademarks of their original owners. The use of any trade name or trademark is for identification and reference purposes only and does not imply any association with the trademark holder of their product brand.

## Overview

This is a simple extension which connects to [LibreLinkUp](https://www.librelinkup.com/) to retrive the latest glucose readings every 60 seconds and show them in the GNOME top bar.

The extension provides for a little configuration screen to set the username and password to be used to login on the LibreLinkUp API. You should use the same credentials used to configure the actual [Android app](https://play.google.com/store/apps/details?id=org.nativescript.LibreLinkUp).

## Installation

The extension should be easy to install via browser from [GNOME Extensions](https://extensions.gnome.org/extension/9393/librelinkup-top-bar/) website. To install it manually instead, clone the repo into the gnome-shell extensions path[^1]:

[^1]: By default the extesions directory should be `~/.local/share/gnome-shell/extensions/`; if it doesn't exist yet, create it.

```bash
git clone https://github.com/gfidente/llu-top-bar-extension.git ~/.local/share/gnome-shell/extensions/llu-top-bar-extension@gfidente.github.com
```

Then proceed to enable and configure the extension:
1. Logout from GNOME and then login again
1. Open the Extensions app
1. Find the 'LibreLinkUp Top Bar' extension and use the three dots icon, next to the extension name, to open the preferences dialog
1. Configure the LibreLinkUp credentials
1. Enable the extension

## Good to know

With every update, the extension will also show (in brackets) the difference in between the latest reading and its previous value. The number is prefixed with a `+` or a `-` sign to indicate if the value is increasing or decreasing.

Once the extension is enabled and running, by clicking on the glucose value in the top bar a small popup menu will appear and show the serial number of the sensor in use and the patient name.

## Limitations

The extension will only show the data from the first patient you are following, even if you are following more than one. Please get in touch if you need this to become a configurable parameter.
