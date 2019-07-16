# archlinux-AMDVLK
PKGBUILDs to build stable AMDVLK-releases from source (https://github.com/GPUOpen-Drivers/AMDVLK)

The AMD Open Source Driver for Vulkan® is an open-source Vulkan driver for AMD Radeon™ graphics adapters on Linux®.

The AMD Open Source Driver for Vulkan is designed to support a wide range of AMD GPUs:

- Radeon™ HD 7000 Series
- Radeon™ HD 8000M Series
- Radeon™ R5/R7/R9 200/300 Series
- Radeon™ RX 400/500 Series
- Radeon™ M200/M300/M400 Series
- Radeon™ RX Vega Series
- Radeon&trade; RX 5700 Series
- AMD FirePro™ Workstation Wx000/Wx100/Wx300 Series
- Radeon™ Pro WX x100 Series
- Radeon™ Pro 400/500 Series
---
To use AMDVLK as default vulkan Driver you have to 
```
export VK_ICD_FILENAMES="/usr/share/vulkan/icd.d/amd_icd64.json" 
```

To use lib32-AMDVLK as default vulkan Driver you have to
```
export VK_ICD_FILENAMES="/usr/share/vulkan/icd.d/amd_icd32.json" 
```

---
The driver exposes many settings that can customize the driver's behavior and facilitate debugging. You can add/edit settings in amdPalSettings.cfg file under one of below paths, formatted with one name,value pair per line:

- /etc/amd
- $XDG_CONFIG_HOME
- $HOME/.config

This amdPalSettings.cfg got all functions from AMDVLK github page, but only activates "cache to disk" what is recommended for gaming.
