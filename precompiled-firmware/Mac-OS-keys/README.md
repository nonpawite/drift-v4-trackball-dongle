# Drift Keyboard V4 — Mac OS Keys  

![Mac OS Keymap](https://github.com/Timception/drift-v4-trackball-dongle/blob/main/precompiled-firmware/Mac-OS-keys/driftv4-MacOS.png)  


### ⚙️ Windows to Mac OS Key Table  
Here is a quick guide on what keys on a Windows keyboard equate to on a Mac OS keyboard  

| Windows Keyboard   | Mac OS Keyboard |
|:------------------:|:---------------:|
| Windows Key / GUI  | Command / ⌘    |
| Alternate / Alt    | Option / ⌥     |
| Control / Ctrl     | Ctrl / ⌃       |  

Use this table so you know what keys to set in [ZMK Studio](https://zmk.studio/)  

The ZMK Keycodes for the Modifiers can be found [HERE](https://zmk.dev/docs/keymaps/list-of-keycodes#modifiers)  

---

### The Tilde(~) Key Problem  
> [!IMPORTANT]
> Sometimes the Tilde key (~) does not work no matter what you try.  
> 
> Open up the Terminal App  
> 
> Copy this code and paste it in your terminal then press enter, you will likely be prompted to enter your password to execute it.  
> 
```
sudo rm /Library/Preferences/com.apple.keyboardtype.plist
```
> [!IMPORTANT]
> Your Drift Keyboard will probably be disabled now, Restart your Mac/Macbook.  
> 
> When you are prompted to setup your keyboard, press "z" for the key next to the left shift.  
> 
> Then press "/" (backslash) for the key next to the right shift.  
> 
> Finally, choose "ANSI (U.S.)".  
> 
> Now your keyboard can type the Tilde key (~) key by pressing [SHIFT + ~]  

---

# Mac OS Keymap  

![Keymap](https://github.com/Timception/drift-v4-trackball-dongle/blob/main/precompiled-firmware/Mac-OS-keys/drift.svg)  

The precompiled firmware using this keymap can be found in the zip file listed above: [V4-Mac-OS-keys-firmware.zip](https://github.com/Timception/drift-v4-trackball-dongle/blob/main/precompiled-firmware/Mac-OS-keys/V4-Mac-OS-keys-firmware.zip)






