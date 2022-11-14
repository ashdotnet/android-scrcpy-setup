## Prereq

Your phone must be running Android 11 and above.

Your Android phone must be connected to the same WiFi connection as your computer.

Copy of the latest version of scrcpy for Windows (download [here](https://github.com/Genymobile/scrcpy/releases))

## Tutorial
On your device, find the **Build number** option (usually under **Settings** > **About phone** > **Build number**)

Tap the  **Build Number**  option seven times until you see the message  `You are now a developer!`  This enables developer options on your phone.

![alt text](https://github.com/ashdotnet/android-scrcpy-setup/blob/main/screenshots/1-1.png?raw=true)

From your Windows Machine, create a folder in Drive C: and name it scrcpy (exact location : **C:\scrcpy**)

![alt text](https://github.com/ashdotnet/android-scrcpy-setup/blob/main/screenshots/1.png?raw=true)

Extract downloaded scrcpy from above to **c:\scrcpy**

Open Command Prompt
Type in the following : 

>     cd c:\scrcpy
Then press ENTER

![alt text](https://github.com/ashdotnet/android-scrcpy-setup/blob/main/screenshots/2.png?raw=true)

Next, on your android device, find **Developer options**

In  **Developer options**, scroll down to the  **Debugging**  section and turn on  **Wireless debugging**. 

![alt text](https://github.com/ashdotnet/android-scrcpy-setup/blob/main/screenshots/1-2.png?raw=true)

Open Wireless debugging

![alt text](https://github.com/ashdotnet/android-scrcpy-setup/blob/main/screenshots/1-3.png?raw=true)

Tap on **Pair device with pairing code**

Take note of the **Pairing Code** and the **IP Address and Port** - we'll use this to initiate the connection with your machine.

![alt text](https://github.com/ashdotnet/android-scrcpy-setup/blob/main/screenshots/1-4.png?raw=true)

Go back to your Windows machine, in the same Command Prompt type in the following : 
>     adb pair ipaddress:port

Then press ENTER

It will then ask you to put the pairing code, type in the Pairing Code from the Android Phone in the Command Prompt and press ENTER.

It should then say successful.

![alt text](https://github.com/ashdotnet/android-scrcpy-setup/blob/main/screenshots/3.png?raw=true)

Go back to your Android phone, inside Wireless Debugging, take note of **IP Address & Port** (*NOTE : the port should be different from the one we used for Pairing!*)

Go back to your Windows machine, in the same Command Prompt type in the following : 
>     scrcpy --tcpip=ipaddress:port

![alt text](https://github.com/ashdotnet/android-scrcpy-setup/blob/main/screenshots/4.png?raw=true)

DONE!

.. image:: https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png
   :target: https://www.buymeacoffee.com/ashdotnet
   :alt: Buy Me A Coffee
