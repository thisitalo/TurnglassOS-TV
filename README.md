========================================================================

                      TURNGLASS OS TV (v1.0.2)

========================================================================



Description

-----------

TurnglassOS TV is a custom, feature-rich Android TV launcher and 

system interface built in Kotlin. Designed to enhance the smart TV 

experience, it integrates seamless media consumption, advanced system 

controls, and a beautiful, dynamic user interface. 



*** CREDITS & ACKNOWLEDGMENTS ***

This project is built upon and inspired by the incredible work of 

GlassOS TV. Full credit goes to the GlassOS TV team for the 

foundational concepts and design language that make this project possible.



========================================================================

REPOSITORY CONTENTS

========================================================================



This repository contains the compiled release APK (`TurnglassOS_TV_v1.0.2_Release.apk`),

release notes, and the core Kotlin source code (`src/` directory) that 

powers the OS. 



Key Modules & Architecture:



1. Core UI & Rendering

   - HomeScreen.kt / HomeOverlay.kt: Main launcher interfaces.

   - DynamicIsland.kt: Interactive notifications and status overlays.

   - GlassPainter.kt / AuroraView.kt: Custom visual effects and rendering.

   - Backdrop.kt / WallpaperGen.kt: Dynamic background and wallpaper handling.

   - WelcomeCard.kt / HeroView.kt: Prominent UI showcases and onboarding.



2. Media & Entertainment Integration

   - Tmdb.kt: The Movie Database API integration for rich media metadata.

   - SpotifyClient.kt: Spotify playback and control integration.

   - MediaRow.kt / WatchNextProbe.kt: Content recommendation and "up next" tracking.

   - Tone.kt / Sound.kt: Audio feedback and sound management.



3. System & Device Control

   - AdbClient.kt: Local ADB commands for advanced system operations.

   - HdmiManager.kt: Input switching and HDMI CEC controls.

   - SysControl.kt / ControlCenter.kt: Quick settings and system toggles.

   - BootReceiver.kt: Startup initialization.



4. Data & Utilities

   - AppRepo.kt / HeroRepo.kt: Data management and repository patterns.

   - Grants.kt: Android permissions handling.

   - Prefs.kt: User preferences and local storage.

   - Profile.kt / Util.kt: User profiles and general helper functions.



========================================================================

INSTALLATION INSTRUCTIONS

========================================================================



Crucial: Because this is a custom launcher/system app, it must be 

sideloaded onto your Android TV device.



1. Download the APK: Locate `TurnglassOS_TV_v1.0.2_Release.apk` in the 

   root directory.

2. Transfer to TV: Use a USB drive or an app like "Send Files to TV" to 

   transfer the APK to your Android TV device.

3. Enable Unknown Sources: On your TV, go to Settings > Device Preferences 

   > Security & Restrictions, and allow installation from Unknown Sources 

   for your file manager.

4. Install: Open your file manager, select the APK, and install it.

5. Set as Default: Press the "Home" button on your remote. You should be 

   prompted to choose a home app. Select TurnglassOS TV and choose "Always".



========================================================================

CRUCIAL SETUP & PERMISSIONS

========================================================================



To get the most out of TurnglassOS TV, several advanced permissions are 

required due to its system-level features:



* ADB Setup: The inclusion of `AdbClient.kt` indicates that the app uses 

  local ADB to bypass standard Android restrictions. You may need to enable 

  "USB Debugging" or "Network Debugging" in your TV's Developer Options 

  and grant the app permission on first launch.

* API Keys: Features relying on `Tmdb.kt` and `SpotifyClient.kt` will 

  require active internet connections and may require you to authenticate 

  your accounts or provide API keys in the app settings to fetch artwork 

  and media data.

* Accessibility/Grants: The app will likely request Accessibility or 

  Usage Access permissions (`Grants.kt`) to draw over other apps 

  (`Overlays.kt`) and detect button presses. Please grant these in the 

  TV settings when prompted.



========================================================================

CHANGELOG

========================================================================

For detailed information on the latest updates, bug fixes, and feature 

additions, please refer to the `RELEASE_NOTES.txt` file included in this 

repository.
