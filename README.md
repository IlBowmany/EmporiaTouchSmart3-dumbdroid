# HELLO!

So, you want to switch to a dumbphone, but at the same time you want to still be on Android, since you need it for your messaging and bank apps? Have no fear, the Emporia TouchSmart 3 is a great choice!
The problem is that, when you first boot this fancy little phone, you will notice that it got a very limiting launcher which prevents us to access to a lot of Android stuff and options, which are hidden by vendor choice. We can bypass all this and make the phone completely ours. We just need some 4D chess move and we are good to go. With this guide you will end up with a proper, minimal yet working Dumbdroid phone, debloated from all the proprietary Emporia apps. 

First of all, after the first boot, we need to activate developer mode, for USB Debugging, sideloading, ecc...

`Settings > More Settings > About Phone > Press multiple times "Build Number", until "You are now a developer" pops up`

After this, we need a launcher for the hidden android options. I recommend you [this one](https://github.com/butzist/ActivityLauncher):
Download the APK from the Releases section and save it on your PC.

Now, it comes the tricky part. Go into the settings option of the phone and, using the **ChatApps** menu, install Whatsapp or Telegram (Signal won't let us send APK, so we won't bother using it).
After this, login in one of those two (I recommend you to use Telegram, it is easier to use and quicker in creating a burner account), create a chat with yourself or a empty group with just you, and send yourself the APK in there. After this, click on it, and you should receive a Popup from Android about the fact that Telegram doesn't have permission to install apps. Follow the instructions on screen to enable the permissions, and then install the APK. We have done! Open Activity Launcher directly from the Installation Wizard popup, and you should be greeted with its functional and simple interface. Go in the search tab and write "Development", find and open the Development options (The icon should be two curly brackets). From it, navigate down in the options and enable USB Debugging.

After this, we need to install [Aurora Store](https://auroraoss.com/) (the best alternative to Google Play Store we can use, since we don't have Google Services into the phone). We can use ADB or Telegram to send ourselves the APK. If you wish to use ADB, download the APK in your PC, plug the phone through a TypeC Cable, open your terminal, and write

`adb install *Insert here your APK location*`

This way the APK should be installed. Using Activity Launcher, open the Aurora Store (If Aurora doesn't appear in the apps list inside the launcher, because it didn't update yet, close it, open the Telegram/Whatsapp page where the APK is stored, and reinstall it. This way it will ask the popup to open it again. Do it and the app should be updated with the new entry). 

After opening Aurora store... Well, we are basically done! Using it, install your favourite launcher (I recommend you [LawnChair](https://play.google.com/store/apps/details?id=app.lawnchair.play&hl=it) since it got everything we need like notification dots, it is light on resources and very nice to look at), open it, using the internal options make it your default one, and that's it! Your phone is now a proper Android Dumbphone, or a DumbDroid. But it's not over yet.

We need and want to remove various bloat the phone have. And for this, we will use the [Universal Debloater](https://github.com/Universal-Debloater-Alliance/universal-android-debloater-next-generation). Download it on your PC, open it, make sure it can find the Emporia phone, and start removing all recommended stuff. Nothing worthy of stays is there, so you can just go and remove all. After this, switch to the All Removals mode in the program, and search for "Emporia". Remove all the Emporia apps except for the updater, since it is the only one that can be useful.

Now the phone should be pretty much ready to go. If you want to enable the status bar, we can do a funny trick for it. Go into Development options using Activity Launcher, search for the "Drawing" option, and choose the one you prefer. This will create a virtual Notch, which isn't so good looking (I will update this guide when I find a proper and better solution), but at least in this way we can have the status bar always on screen. If you want to enable more status bar icons (like the percentage near the battery icons), install and use an app like [System UI Tuner](https://play.google.com/store/apps/details?id=com.bryancandi.android.uituner&hl=it). If you want to enable Automatic Brightness, using Activity Launcher, search for Adaptive Brightness, and move it to on from the menu. It is extremely handy and I don't know why it isn't automatically enabled!

If you need a better physical keyboard handler, use [this](https://play.google.com/store/apps/details?id=io.github.sspanak.tt9)

For general app usage, I reccomend the [Fossify](https://play.google.com/store/apps/dev?id=7297838378654322558&hl=it) apps, and for camera, use [OpenCamera](https://play.google.com/store/apps/details?id=net.sourceforge.opencamera&hl=it).

For GPS and location services, [Organic Maps](https://f-droid.org/en/packages/app.organicmaps/).

If you need a better internet browser, every one of the bigger ones should work the same (I only tested [WaterFox](https://play.google.com/store/apps/details?id=net.waterfox.android.release&hl=it))

If you need to change the size of icons and interface, use the following ADB command (The default Emporia options are very limited):

`adb shell wm density *A NUMBER BETWEEN 320 AND 200*`

I recommend 250.

if you want to reset the default density, just write

`adb shell wm density reset`

