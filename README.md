script is titled steam-appmanifest.py


Manual

Find the AppID of the app you're trying to download. This can be easily done by going on http://steamdb.info/ and searching for it.
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
