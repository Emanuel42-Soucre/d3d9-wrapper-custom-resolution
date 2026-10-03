# d3d9-wrapper-custom-resolution
Compiled by **Emanuel42**  
Based on ThirteenAG's original project.

---

## 🕹️ Overview
This repository provides a manually compiled binary of the **D3D9 Proxy Wrapper**, configured to force custom resolutions, fix aspect ratios, and stretch retro PC/Arcade games to full screen (16:9) without additional GPU overhead.

For the full source code and original development, please visit the official repository:
👉 [ThirteenAG/d3d9-wrapper](https://github.com)

---

## 📂 Configuration (`d3d9.ini`)

To customize your cabinet layout, configure your `d3d9.ini` file exactly like this:

```ini
[MAIN]
ForceWindowedMode = 1                          // 1: Wrapper Injector ON | 0: OFF
FPSLimit = 0                                   // Max FPS (0: Unlimited / Disabled)
FPSLimitMode = 2                               // 1: Real-time thread block | 2: Suspend mode (Precise)
FullScreenRefreshRateInHz = 0                  // Forces refresh rate manual lock
DisplayFPSCounter = 0                          // Displays FPS and Frametime overlay
EnableHooks = 1                                // Required for focal switches and mouse capture

[FORCEWINDOWED]
UsePrimaryMonitor = 1                          // Locks application window to the primary arcade display
CenterWindow = 1                               // Centers canvas on screen (If FullScreen = 0)
AlwaysOnTop = 1                                // Keeps the executable focused on top of the front-end
DoNotNotifyOnTaskSwitch = 1                    // Application ignores OS focus loss (Prevents desktop crashes)
ForceWindowStyle = 1                           // 1: Borderless Full Screen | 2: Windowed | 3: Resizable Window
CaptureMouse = 0                               // Traps mouse pointer inside the graphics hook
Width = 1920                                   // Forces custom horizontal width (Internal Backbuffer)
Height = 1080                                  // Forces custom vertical height (Internal Backbuffer)
FullScreen = 1                                 // 1: Stretches ANY legacy definition to absolute full screen
```

---

## 🔧 How to Use
1. Download the compiled `d3d9.dll` and `d3d9.ini` files from this repository.
2. Place both files directly into the root folder of your game (where the main `.exe` file resides).
3. Open `d3d9.ini` with Notepad and set your exact screen dimensions under `Width` and `Height`.
4. Run your game normally.
