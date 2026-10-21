# Dolphin Emulator - Xbox Series S/X Controller Profile for Debian 13

This repository contains an optimized Dolphin Emulator profile (`.ini`) specifically mapped for using an **Xbox Series S/X Controller** via the **SDL driver** on **Debian 13 (Linux)**.

## 📁 Repository Structure

```
.
├── README.md
└── Profiles/
    └── Wiimote/
        └── platformers-horizontal-wiimote.ini
```

## 🎮 Features & Mapping

This profile includes dual mapping for maximum compatibility:

* **Sideways Wiimote (Platformers):** Configured for 2D platformers (e.g., *New Super Mario Bros. Wii*).
* **Classic Controller:** Full mapping for games supporting the Wii Classic Controller (e.g., *Mario Kart Wii*, *Smash Bros*).
* **SDL Driver Integration:** Pre-configured with `SDL/0/Xbox Series X Controller` to prevent missing-device errors on Linux.

| Xbox Button | Sideways Wiimote Mode | Classic Controller Mode |
| --- | --- | --- |
| **A** | Button 2 | Button B |
| **B** | Button 1 | Button A |
| **X** | Shake / Tilt | Button Y |
| **Y** | Shake / Tilt | Button X |
| **LB / RB** | Tilt Left / Right | L / R Triggers |
| **LT / RT** | — | Analog Triggers (L / R) |
| **D-Pad** | D-Pad | D-Pad |
| **Left Stick** | Nunchuk Stick | Left Stick |
| **Right Stick** | — | Right Stick |
| **View / Menu** | `-` / `+` | `-` / `+` |
| **Xbox Logo** | Home | Home |

## 🚀 Installation Guide

### 1. Copy the Configuration File

Copy the `.ini` file into your local Dolphin profile directory:

```bash
mkdir -p ~/.config/dolphin-emu/Profiles/Wiimote/
cp Profiles/Wiimote/platformers-horizontal-wiimote.ini ~/.config/dolphin-emu/Profiles/Wiimote/
```

### 2. Load the Profile in Dolphin

1. Open **Dolphin Emulator**.
2. Go to **Controllers** -> **Wii Remote 1** -> **Configure**.
3. In the top-right corner under **Profile**, select `platformers-horizontal-wiimote`.
4. Click **Load**.
5. Verify that the **Device** field in the top-left reads `SDL/0/Xbox Series X Controller`.
6. Click **Close**.

## 💡 Notes & Troubleshooting

* **GameCube Games:** For GameCube games, do not use the Wiimote menu. Configure **Port 1** as **Standard Controller** in the main Dolphin controller settings.
* **Nunchuk Games:** If playing a game requiring a Nunchuk (e.g., *Super Mario Galaxy*), disable `Sideways Wiimote` under the **General and Options** tab in Dolphin after loading the profile.