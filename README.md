### Disclaimer
As of August 14th 2018, this script is no longer needed. See Digital Ocean's [Release Notes.](https://www.digitalocean.com/docs/release-notes/)
>The Droplet console now supports pasting information into the console. 

## Description
This is a handy little script for those who are using DigitalOcean's servers and are unable to 'Copy & Paste' to the console of their droplet. 

___

## Functionality
* Permits 'Copy & Paste' function by opening a small dialog window where the user can paste whatever they wish to appear in the console. (uses sendkeys with JavaScript)
* Allows the user to use their own keyboard language.

___

## Usage
1. Open your web browser's 'Console'. The hotkeys for this varies depending on OS and web browser. 
  
|      OS       |    Browser    |     Hotkey       |
| :-----------: |:-------------:| :---------------:|
| **Windows**   | Firefox       |  `CTRL+SHIFT+K`  |
|               | Chrome        |  `CTRL+SHIFT+J`  |
|               | IE / Edge     | `F12 -> Console` |
| **OS X**      | Firefox       |  `CMD+OPT+K`     |
|               | Chrome        |  `CMD+OPT+J`     |
|               | Safari        |  `CMD+OPT+C`     |

2. Enter the console command found under 'SCRIPT' and press Enter.
3. Copy and paste the text you want to be entered in the console or manually type it.
4. Press OK or hit Enter. 
5. You should now see the text being entered in the console of your droplet. 

___

## Script
```
!function(){function t(){function n(t,e){s=s.concat(RFB.messages.keyEvent(t,e))}var o=e.shift(),s=[],i=o.charCodeAt(),c=-1!=='!@#$%^&*()_+{}:"<>?~|'.indexOf(o),r=XK_Shift_L;c&&n(r,1),n(i,1),n(i,0),c&&n(r,0),rfb._sock.send(s),e.length>0&&setTimeout(t,10)}var e=prompt("Enter text to be sent to console").split("");t()}();
```

