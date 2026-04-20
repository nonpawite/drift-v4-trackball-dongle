# Drift Keyboard V4 — Trackball Edition  
by **Timception**

Welcome to the **Drift Keyboard V4 — Trackball Edition**.  
This version keeps the familiar shape of previous Drift models while introducing some interesting additional features.  

**Mac users can setup this keyboard** [following this guide](https://github.com/Timception/drift-v4-trackball-dongle/tree/main/precompiled-firmware/Mac-OS-keys)  

---

## 🆕 Key Features

- [ZMK Studio](https://zmk.studio/) enabled, and can also be keymapped using [Nick Coutsos' Editor](https://github.com/nickcoutsos/keymap-editor)  
- Connects through a **dongle** for improved wireless functionality  
- Adds a **newly integrated trackball** - One less device to carry. Enjoy full cursor control without the need for a separate mouse.  
- Can install sockets for **choc v1/v2 switches**

---

## 🔢 Key Count & Layout

- **63 keys** total  
- Only **5 keys fewer** than the 68-key Drift V2/V3  
- Removed the **outermost columns**, but the layout still provides everything needed to easily migrate from conventioal 60%-65% keyboards.  
- The **encoder** is now placed on the **thumb cluster**  
- The **right half** features a **swappable trackball**, allowing you to try different materials or replace the trackball module.

If you’ve used the Drift V2 or V3 before, you’ll adapt to this version very quickly.  
The trackball has been smoothly integrated and is not hard to get used to.  

---

## 🛠️ Design Notes

This model took extensive time and refinement to bring together, and I can easily call it my Masterpiece.

- The **OLEDs were removed** to avoid signal interference with the MCU underneath  
- **4-pin OLED sockets remain**, so users can reinstall displays and make firmware changes if desired  
- Designed with **maximum modding potential** in mind, and all the case parts can be 3D-Printed so even more colors  
- The Trackball can be removed by putting an allen-key wrench in the tiny hole on the side and popping it out (but be careful not to hit the sensor lens)

---

## ⚙️ Build Options

The V4 supports multiple build configurations:

- **MX switch** builds  
- **Choc V1/V2 low-profile** builds  
- Many possibilities for **multiple case designs**, I made many parts for this, and hope to keep making more!  

---

## 🧭 Trackball Behavior & Controls

### ✅ How the Trackball Behaves

#### 🛑 While You're Typing
- The **trackball is disabled while you type**.
- It automatically re-enables **0.5 seconds after the keyboard stops receiving key presses**.

#### 🖱️ While You’re Using the Trackball
- When you move the trackball, the **right half switches to mouse-only mode**.
- This means you **can’t type** on the right side until:
  - You stop moving the trackball for **~0.6 seconds**, **then** the keyboard returns to normal typing mode.
- This function prevents accidental mouse activation while typing and vice versa.

---

### 🔒 Permanent Mouse Mode (Optional)
If you want the right half to stay in mouse mode:

- **Hold `Raise` + press `6`**  
  → Mouse mode stays locked on.
- To exit, **Hold `Raise` + press `6` again**  
  → Returns to normal keyboard operation.  

This is just moving around different layers - not black magic.  

---

### 🎯 Mouse Controls (When Mouse Mode Is Active)

| Action | Key |
|--------|------|
| **Left Click** | `K` |
| **Right Click** | `L` |
| **Scroll** | Hold `O` + move the trackball |

---

### 🎥 Extra 3D Navigation Functions (Optional)
For users working in **3D programs**, Drift V4 includes two special macros while the mouse layer is active:

#### 🌀 Orbit
- **Key:** `.` (period)
- **Function:** Holds **Shift + Middle Click** while the trackball moves  
- **Usage:** Rotate/orbit around models and objects

#### 📐 Pan
- **Key:** `,` (comma)
- **Function:** Holds **Middle Click** while the trackball moves  
- **Usage:** Pan the view horizontally/vertically in 3D space  

---

### ⚙️ Customizing Trackball Behavior
If you want to customize how the trackball or mouse keys work, you’ll need to update your firmware:

- Edit your fork on GitHub  
- Recompile the firmware  
- Flash **all three devices**: left half, right half, and dongle  

---


- This keyboard was developed alongside Drift Keyboard V3, though it was not released at the same time.  
- Drift Keyboard V4's design is derived from the original Drift Keyboard.  

You can see more actual builds [-=HERE=-](https://www.instagram.com/majin.keyboards)  

# Keymap

![Keymap](https://github.com/Timception/drift-v4-trackball-dongle/blob/main/keymap-drawer/drift.svg)  

## 🔄 Reflashing Instructions

Your keyboard already has firmware installed, you usually don’t need to reflash.  
But if you want to update to the latest build, here’s how to do it:

1. **Download the latest firmware**  
   - Go to the **[precompiled-firmware](https://github.com/Timception/drift-v4-trackball-dongle/tree/main/precompiled-firmware)** in this repo.  
   - Download the desired **firmware .zip file**, if you have a Mac, get the zip file in the "Mac-OS-keys" folder.  

2. **Unzip the file**  
   - Inside you’ll find multiple `.uf2` files:       
     - `drift_central_dongle.uf2` → Dongle firmware  
     - `drift_left.uf2` → Left half firmware  
     - `drift_right.uf2` → Right half firmware  
	 - `settings_reset-nice_nano_v2-zmk.uf2` → Settings Reset firmware (needed to clean devices before new firmware)  

3. **Reset the dongle**  
   - Plug in your dongle.  
   - Double-click the **reset button** on the dongle.  
   - A new drive should appear on your computer.

4. **Flash the reset firmware**  
   - Drag `settings_reset-nice_nano_v2-zmk.uf2` into the new bootloader drive.  
   - Wait until the dongle reboots.  

5. **Repeat reset step for each keyboard half**  
   - Double-click the reset button on the **left half** → drag `settings_reset-nice_nano_v2-zmk.uf2` into the bootloader drive.  
   - Do the same for the **right half**.  

6. **Flash the NEW dongle firmware**  
   - Plug in the dongle again.  
   - Double-click reset → drag `drift_central_dongle.uf2` into the drive.  
   - Wait for it to finish.  

7. **Flash the left half with new firmware**  
   - Plug in the **left half**.  
   - Double-click reset near the power switch.  
   - Drag `drift_left.uf2` into the bootloader drive.  

8. **Flash the right half with new firmware**  
   - Repeat the same process with the **right half**, using `drift_right.uf2`.  

9. **Reconnect everything**  
   - Unplug the halves.  
   - Plug the dongle back in.  
   - Press the reset button once on each half so they reconnect to the dongle.  

10. ✅ You’re done!  
	- Download [ZMK Studio](https://zmk.studio/download), or
    - Open the [ZMK Studio](https://studio.zmk.dev) app online to see your Drift keyboard.  
    - Now you can view and customize your keys to your hearts content.  
	
11. **Useful Links for further tinkering:**  
	- More information on all the different [keys and keycodes](https://zmk.dev/docs/keymaps/list-of-keycodes)  

## Acknowledgments  

This project makes use of code and ideas from the following repositories:
- [ZMK Firmware](https://github.com/zmkfirmware) (MIT License) - Zephyr™ Mechanical Keyboard (ZMK) Firmware  
- [ufan/zmk](https://github.com/ufan/zmk) (MIT License) – Original ZMK base and PMW3610 work  
- [badjeff/zmk-pmw3610-driver](https://github.com/badjeff/zmk-pmw3610-driver) – PMW3610 driver work, based on ufan’s code  
- [badjeff/zmk-behavior-key-press-lip](https://github.com/badjeff/zmk-behavior-key-press-lip) - LIP Key Press Behavior
- [leafflat/sai44](https://github.com/leafflat/sai44) (MIT License) – Dongle code reference  
- [nuovotaka/zmk-pointing-acceleration-alpha](https://github.com/nuovotaka/zmk-pointing-acceleration-alpha) (MIT License) – Pointer acceleration  
- [caksoylar](https://github.com/caksoylar/keymap-drawer) (MIT License) - Keymap Drawer  

All third-party code remains under their original licenses.  








