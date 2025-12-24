# Unity Advanced Settings Menu Asset

A modular, high-performance, and developer-friendly **Settings Menu System** for Unity. This asset provides a comprehensive solution for Video, Audio, and General settings with a focus on mathematical accuracy and clean code principles.

## 🚀 Key Features

### 🖥️ Video Settings
- **Smart Resolution Management:** Automatically fetches supported resolutions and groups them to avoid duplicates.
- **Refresh Rate Control:** Precision Hertz selection using the modern `RefreshRate` struct.
- **Dynamic Display Modes:** Supports Fullscreen, Windowed, and VSync toggles.

### 🔊 Audio Settings (Logarithmic Control)
- **Natural Scaling:** Implements $dB = \log_{10}(\text{value}) \times 20$ to match human auditory perception instead of linear scaling.
- **Mixer Integration:** Ready-to-use integration with Unity Audio Mixer (Master, Music, SFX).
- **Persistent Data:** Automatic saving and loading of volume levels via PlayerPrefs.

### ⚙️ General Settings
- **Cycle-based Localization:** Minimalist language selection using robust modulo arithmetic to prevent index errors. Check [Unity-Localization](https://github.com/ardat11/Unity-Localization) for usage to add other elements of your game into localization .
- **Precision FOV & Sensitivity:** High-precision sliders with real-time value display (formatted to 3 decimal places).
- **OnValidate Integration:** Instant UI feedback in the Inspector; UI elements enable/disable based on developer toggles.

### 🛠️ Developer Tools (Custom Editor)
- **Conditional Inspector:** Includes a custom `Editor` script that dynamically hides/shows UI references based on feature toggles, keeping the Inspector clean.
- **Extensible Architecture:** Easy to add new categories or settings without breaking the existing flow.

## 📐 Mathematical Approaches Used
- **Logarithmic Mapping:** Ensuring volume sliders feel "correct" to the player's ear.
- **Equivalence Relations:** Grouping system resolutions by dimensions while preserving unique hardware refresh rates.
- **Robust Modulo Arithmetic:** Used $(index \pmod n + n) \pmod n$ logic for the language cycler to handle negative index shifts flawlessly.

## 🛠️ Installation & Setup

1. **Import Package:** Download the `ardat11_Localization.unitypackage` from the `Package` folder. Drag and drop it into your Unity Project or navigate to `Assets > Import Package > Custom Package`. Ensure all scripts, prefabs, and the `Resources` folder are selected during import.

2. **Editor Folder:** **Crucial!** Ensure that the `GeneralSettingsEditor` and `AudioSettingsEditor` scripts remain inside a folder named **"Editor"**. This prevents compilation errors during the build process.

3. **Scene Setup:** Locate the `SettingsCanvas` prefab inside the `Assets/Prefabs` folder and drag it into your scene. This prefab contains the pre-configured UI hierarchy.

## 📄 License
This project is licensed under the MIT License - feel free to use it in your personal or commercial projects.

---
*Developed by a Mathematical Engineering student & Unity Developer.*
