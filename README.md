
## VR
---
VR application developed in Unity for the Oculus Quest. This repository provides the final build as [Build 1](build1.apk). It uses the TCP communication protocol to communicate with the Raspberry PI or other devices as a client. 


### Installation
This section explains how to sideload an app into the Oculus Quest. There are different methods on how to do it that can be found through a simple online search since the Oculus Quest runs Android. One of the most popular options is [Side Quest](https://sidequestvr.com). 

This tutorial explains the steps that we followed alternatively.

##### Enable Oculus Quest developer mode
The Oculus Quest must have developer mode enabled to be able to sideload apps. 
1. To enable developer mode, the account you used must create an organization in the [developer website](https://developer.oculus.com/manage/organizations/create/). The name doesn't matter if you don't plan on publishing apps in the future.
3. Afterwards, the user must provide [account verification](https://developer.oculus.com/manage/verify/).

With these two steps cleared out, it's as simple as going into the Oculus App on your mobile device, connecting to the Quest, entering the **More Settings** submenu, and enabling developer mode in the corresponding section.

##### Download the APK
Download the file linked above or shown in the folder as `build1.apk`. 

##### Download Android SDK Platform Tools
It's a small library that allows the user to upload an `.apk` to an Android device. It can be downloaded through the [official website](https://developer.android.com/studio/releases/platform-tools) . You should choose the correct download for your operating system and unzip the file. 

Remember its location, since it will be important for the following steps.


##### Command Line
From the command line (terminal in macOS or `cmd` in Windows), the user must execute different commands:
1. Navigate to the location of the unzipped files withing `platform tools`. In this example, the files were extracted to Downloads.
	```cd \Downloads\platform-tools```

2. Once there, run the installation command for the apk, in the form:
	```adb install -r [APK directory]```
Where you replace the directory with the file location. If you don't know how to write out the directory, the file can be dragged after `adb install -r `.

### Connection
In the current iteration, to ensure connection the user must follow the steps:
1. Run the Python script on the Raspberry Pi or Windows/MacOS device to open the host server.
2. Open the application on the Oculus Quest.
3. Once open, the game can be started by pressing **S** key on the device.

If the steps don't work, try closing both programs and restarting them in the correct order. 

