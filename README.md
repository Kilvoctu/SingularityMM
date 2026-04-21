## Changes from Upstream
This fork exists as Singularity does not work properly for me as a Game Pass user, so I've fixed it for myself and added some quality of life:

- Improves Game Pass detection by scanning all drives with a relaxed `Get-AppxPackage` query.
- Correctly launch No Man's Sky for Game Pass instead of trying to launch Steam.
- Cache the path to prevent repetitive disk searching, and also stop repeated PowerShell popup windows.
- Stop Singularity from resizing whenever looking at a mod card in "Browse". 
- Apply asynchronous and throttling logic for fetch operations to avoid UI freezes.
- Update API calls to fix "Could not retrieve download URL" issues (I don't have Nexus Premium anyway). 
- Manual installation from Nexus will automatically pull metadata from the file (as Nexus filenames have this format `Mod-ID-Version-Timestamp.zip`)
- - Mods installed this way will have the automatic metadata, and "Check for Updates" will work by comparing it with Nexus. Who needs Premium!

Original Readme below
# Singularity

A lightweight Windows-based Mod manager for No Man's Sky built with Tauri v2 that started as a curiosity.

![Screenshot](screenshots/Screenshot1.png)
![Screenshot](screenshots/Screenshot2.png)
![Screenshot](screenshots/Screenshot3.png)

## Features

*   **Automatic Game Detection:** Finds your Steam, GOG or Gamepass PC installation of No Man's Sky automatically.
*   **Mod Management:** Easily enable, disable, download, install and set the priority of your mods.
*   **Mod Update Check:** Easily check for updates for your installed mods.
*   **Drag & Drop Installation:** Install mods by simply dropping `.zip`, `.rar` or `.7z` files onto the application.
*   **Nexus Mods Integration with SSO:** Link the Manager with your Nexus Account through the Single Sign-On and download mods using the "Mod Manager Download" button or if you have a Premium Account you can browse and download mods directly through the Manager itself.
*   **Profiles:** Includes option to save mod profiles for different play styles.

## Dependencies

Pretty much the only dependency is WebView2 that if you have an updated Windows 10 or Windows 11, your machine should have it.
If not, you can get it [here](https://developer.microsoft.com/en-us/microsoft-edge/webview2?form=MA13LH#download).
