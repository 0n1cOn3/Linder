# Linder

version 1.4b

## About

This POC script embeds an metasploit generated android payload to any other APKs.

It just automates the following:-

  [+] Copying payload smali files into target app.
  
  [+] Finding target app's MainActivity smali file.
  
  [+] Finding Hookpoint and adding hook there.
  
  [+] Writing permissions in the Androidmanifest.xml
  
  [+] Compile the infected app.
  
  [+] Signing.

**There are some apps like FacebookLite which are a little protected by this method. The MainActivity smali file specified in the Manifest is not present. And there are also some other apps that throw some errors on decompiling. May take a while to fix.**

And a Special Thanks to [TheSpeedX](https://github.com/TheSpeedX) for optimising this script.

## Installation

Just make sure apktool and apksigner are properly installed.

**NOTE FOR TERMUX**:- It wasnt possible for this script to run in termux in the previous version because its apktool cant decompile apps properly, but thanks to [Hax4us's APKMOD](https://github.com/Hax4us/Apkmod), its now possible. Run `termux-setup.sh` to install it and other dependencies.

## Usage

#### Interface Mode 

`python3 main.py`

#### Command Line Usage

`python3 main.py path/to/payload.apk path/to/any/app.apk path/to/save/the/final/app/with/name.apk`

Example:- `python3 main.py /sdcard/somepayload.apk /sdcard/Whatsapp.apk /sdcard/Whatsapp_Infected.apk`

#### To Update 

`python3 main.py --update`

## Troubleshooting

If you are getting error while compilation/decompilation of APKs then update your Apktool/Apkmod to the latest version.

Or if you are facing some other error then please open an issue here.

## Contact

Telegram:- *@R37R0_GH057*

Discord:- *Ken Kaneki#2895*
