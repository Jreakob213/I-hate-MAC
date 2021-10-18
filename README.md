script is titled steam-appmanifest.py


Manual

You need Python 3 and Python 3 GObject Bindings for the script to run.

Debian and Ubuntu (and derivatives) don't have these installed by default. The packages are python3 and python3-gi.
ArchLinux and derivatives can install python and python-gobject.
Fedora should have everything installed by default.
Mac OS requires python3 bindings for GTK3, which can be installed with brew install pygobject3 --with-python3.


After you have installed these, download steam-appmanifest.py. Make the file executable ($ chmod +x steam-appmanifest.py) and start it. A dialog should appear. Type in your Steam Community ID in the top textbox and hit Refresh. Make sure your profile is publicly viewable. A list of titles should appear. Install the apps that you want by clicking the checkbox to the left of the Title (and AppID). After you finish, restart Steam.



Find the AppID of the app you're trying to download. This can be found by going on http://steamdb.info/ and searching for it.
Go to ~/.steam/steam/SteamApps or wherever your main SteamApps folder is.
Create and open a new file called "appmanifest_APPID.acf", replace APPID with the actual AppID you found in Step 1.
Copy and paste the following and replace APPID (the all-caps one) with the one you found in Step 1 and APPNAME with the folder name to download to:

```
    "AppState"
    {
      "AppID"  "APPID"
      "Universe" "1"
      "installdir" "APPNAME"
      "StateFlags" "1026"
    }
```
