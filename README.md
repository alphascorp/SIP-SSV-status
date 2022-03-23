# SIP & SSV status ([Download](https://github.com/alphascorp/SIP-SSV-status/blob/main/Screenshots/Main%20GUI%20macOS%2011%20%2B.png))

---

<h4 align="center">Display the status of System Integrity Protection (SIP) and Signed System Volume (SSV)</h4>

---

### Easy to use

This app makes it easy to display the current status of System Integrity Protection (SIP) and Signed System Volume (SSV) on your system with a simple interface.


<p align="center">GUI on macOS 10.14.6<br><img width="400" alt="Main GUI macOS 10.14.6" src="https://github.com/alphascorp/SIP-SSV-status/blob/main/Screenshots/Main%20GUI%20macOS%2010.14.6.png"></p>


<p align="center">GUI on macOS 11 +<br><img width="400" alt="Main GUI macOS 11 +" src="https://github.com/alphascorp/SIP-SSV-status/blob/main/Screenshots/Main%20GUI%20macOS%2011%20%2B.png"></p>

The following Terminal commands are no longer necessary for this.


### Terminal commands given as a reminder
:point_down:
<details> <summary> View Spoiler: (Terminal commands)  </summary>

  - For displaying System Integrity Protection (SIP):
```
csrutil status
```


  - For displaying Signed System Volume (SSV):
```
csrutil authenticated-root status
```

</details>


### :warning: Error message at first run

The first time you run the program, you may get the following error message:
Impossible to open "OpenCoreVersion.app" because this app comes from an unidentified developer.


This is because an attribute is added so that it can ask the user for confirmation the first time the downloaded program is run, to help stop malware. After confirmation, the attribute should be removed automatically, and then the program will run normally.

But if the program does not run, just remove this attribute (once and for all) with the following procedure:
1. Open Terminal (Applications -> Utilities -> Terminal.app)
2. Write or Copy/Paste (in Terminal) the following line
```
xattr -rd com.apple.quarantine 
```
3. Type a space
4. Drag and drop "OpenCoreVersion.app" next to it, from the Finder

Now the program will run normally.