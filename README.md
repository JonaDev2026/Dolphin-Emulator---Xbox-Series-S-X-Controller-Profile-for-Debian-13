




# Dolphin Emulator - Xbox Series S/X Controller Profiles for Debian 13

https://github.com/user-attachments/assets/18732be8-2d01-414a-94f9-88131274cace

This repository contains optimized Dolphin Emulator profiles (`.ini`) specifically mapped for using an **Xbox Series S/X Controller** via the **SDL driver** on **Debian 13 (Linux)**.

## 📁 Repository Structure

```
.
├── README.md
└── Profiles/
    └── Wiimote/
        ├── Wii_Wiimote_Sideways.ini
        └── Wii_Classic_Controller.ini
```

---

## 📌 Profile Selection Guide

| Profile File | Recommended Games | Extension Setting | Description |
| :--- | :--- | :--- | :--- |
| `Wii_Wiimote_Sideways.ini` | *New Super Mario Bros. Wii*, *Donkey Kong Country Returns*, *Sonic Colors* | `Extension = None` | Maps the Xbox controller as a horizontal Wii Remote. Extension is disabled to prevent the *"extension controller is not supported"* error. |
| `Wii_Classic_Controller.ini` | *Mario Kart Wii*, *Super Smash Bros. Brawl*, *Xenoblade Chronicles*, *Zelda* | `Extension = Classic` | Enables the Wii Classic Controller extension for dual analog stick, trigger, and full button mapping like a modern gamepad. |

---

## 🎮 Features & Mapping

### 1. Sideways Wiimote (`Wii_Wiimote_Sideways.ini`)

| Xbox Button | Wiimote Action |
| :--- | :--- |
| **Xbox X** | Button 1 (Run / Fireball) |
| **Xbox A** | Button 2 (Jump) |
| **D-Pad** | D-Pad (Movement) |
| **LB / RB** | Tilt / Shake (Spin Jump / Pick up items) |
| **View / Menu** | `-` / `+` (Pause / Map) |
| **Xbox Logo** | Home |

### 2. Classic Controller (`Wii_Classic_Controller.ini`)

| Xbox Button | Classic Controller Action |
| :--- | :--- |
| **Xbox A** | Button B |
| **Xbox B** | Button A |
| **Xbox X** | Button Y |
| **Xbox Y** | Button X |
| **Left Stick** | Left Analog Stick |
| **Right Stick** | Right Analog Stick |
| **LT / RT** | Analog Triggers L / R |
| **LB / RB** | Full Click L / R |
| **D-Pad** | D-Pad |
| **View / Menu** | `-` / `+` |
| **Xbox Logo** | Home |

---

## 🚀 Installation Guide

### 1. Copy the Configuration Files

Run the following commands in your Debian terminal to place the profile files into your local Dolphin configuration directory:

```bash
mkdir -p ~/.config/dolphin-emu/Profiles/Wiimote/
cp Profiles/Wiimote/*.ini ~/.config/dolphin-emu/Profiles/Wiimote/
```

### 2. Load the Profile in Dolphin

1. Open **Dolphin Emulator**.
2. Go to **Controllers** -> **Wii Remote 1** -> **Configure**.
3. In the top-right corner under **Profile**, select either `Wii_Wiimote_Sideways` or `Wii_Classic_Controller`.
4. Click **Load**.
5. Verify that the **Device** field in the top-left reads `SDL/0/Xbox Series X Controller`.
6. Click **Close**.

---

## 💡 Troubleshooting & Notes

* **"Extension controller is not supported" Error:** Games like *New Super Mario Bros. Wii* do not support the Classic Controller or Nunchuk. Always load the `Wii_Wiimote_Sideways` profile (`Extension = None`) for these games.
* **GameCube Games:** For GameCube games, do not use the Wiimote menu. Configure **Port 1** as **Standard Controller** in the main Dolphin controller settings.
* **Device Selection on Linux:** If controls stop responding after loading a profile, ensure the **Device** drop-down at the top left is set to `SDL/0/Xbox Series X Controller`.
