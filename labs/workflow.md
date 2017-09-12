> [Internet of Things (IoT) | Training Course](workflow.md) ▸ **Workflow**

# Workflow

[1. Pycom typical workflow](#pycom-typical-workflow)

[2. Resetting your device](#resetting)

[3. Syncing a subfolder](#syncing-a-subfolder)

## Pycom typical workflow

A typical workflow is the following:
1. Open Atom
2. Add a project folder: `top menu ► File ► Add Project Folder...`
3. Plug your device into your USB port
4. Update Pymakr settings (connection via USB or WiFi)
5. Connect
6. Write your code
7. Run your code for debugging
8. Sync your code once done

These steps are illustrated in the following video: 

https://www.youtube.com/watch?v=L1CmWsZlCeU

Instead you might want to connect to your device via WiFi. To do so:

1. Remove the serial port name in Pymakr settings `Device address` field and just leave it blank (the default IP address is ok)
2. Look up Pycom device's WiFi in WiFi access points available
2. and reconnect.

These three steps are illustrated in the following video:

https://www.youtube.com/watch?v=w3rnU3dZJ9w&feature=youtu.be


## Resetting
They are different ways to reset your device:

1. Soft reset

`ctrl+D` in Pymarkr plugin console.

2. Formating device's `/flash` folder
```python
import os
os.mkfs('/flash')
```
then reboot.

## Fetching data from the Lopy with Filezilla

> Warning: Your device's WiFi should be in Acces Point mode.

To establish a connection with your device:

1. Connect to device's WiFi
2. And reproduce the settings below:

![img/filezilla-settings.png](http://i.imgur.com/SAN02Pa.png)

## Syncing a subfolder
This is important to note that only one folder/project should be open in Atom when using the Pymakr package. This said, this main folder can contain subfloders. Let's consider the example below where we open the `button` project/folder containing various subfolders. 

If you want to sync. only one folder to the Pycom device. You must:

1. specify in Settings `Sync Folder` field your subfolder of interest
2. click `Reconnect` (IMPORTANT!)

Then you will be in a position to sync exclusively the subfolder of interest. The video link below illustrate the process:

https://www.youtube.com/watch?v=Pa4-0Rf62ps&feature=youtu.be
