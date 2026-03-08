# 🎨 Red Yellow Blue Color Ramps for QGIS

![QGIS](https://img.shields.io/badge/QGIS-3.x-93b023?style=for-the-badge&logo=qgis&logoColor=white)
![License](https://img.shields.io/badge/License-Free_to_Use-blue?style=for-the-badge)
![Format](https://img.shields.io/badge/Format-XML_Style-orange?style=for-the-badge)
![Colors](https://img.shields.io/badge/Ramps-3_Variants-red?style=for-the-badge)
![GIS](https://img.shields.io/badge/GIS-Cartography-green?style=for-the-badge)
![Made With](https://img.shields.io/badge/Made_With-❤️-ff69b4?style=for-the-badge)

---

## 📋 Overview

A QGIS style file (`.xml`) containing **3 preset color ramp variants** designed for cartographic visualization. These ramps transition through **Red → Orange → Yellow → Green → Blue**, making them ideal for classified and graduated symbology in maps.

| Ramp Name | Colors | Best For |
|-----------|--------|----------|
| **Red_Yellow_Blue_1** | 🔴 `#F40303` → 🟡 `#FDBA36` → 🟢 `#95F703` → 🔵 `#0085A8` | Temperature, elevation |
| **Red_Yellow_Blue_2** | 🔴 `#E60000` → 🟡 `#FEFF75` → 🟢 `#93F700` → 🔵 `#00A8E6` | Heatmaps, density |
| **Red_Yellow_Blue_3** | 🔴 `#F40000` → 🟠 `#FC8B00` → 🟢 `#AAFF01` → 🔵 `#00A8E6` | Risk zones, NDVI |

---

## 🖥️ Requirements

- **QGIS 3.x** or later (tested on QGIS 3.28+)
- No additional plugins required

---

## 📥 How to Import

### Method 1 — Style Manager (Recommended)

1. Open QGIS
2. Go to **Settings** → **Style Manager** (or press `Ctrl+Shift+S`)
3. In the Style Manager window, click the **Import/Export** button (bottom-left) → **Import Items**
4. Browse to and select `Red_Yellow_Blue_Colors.xml`
5. Check the color ramps you want to import (or select all)
6. Click **Import**
7. The ramps now appear under the **Color Ramps** tab, tagged as `custom`

### Method 2 — Drag and Drop

1. Open QGIS with any project
2. Drag `Red_Yellow_Blue_Colors.xml` directly into the QGIS window
3. A dialog will ask which items to import — confirm and click **Import**

### Method 3 — Copy to Profile Folder

1. Copy the XML file to your QGIS profile styles directory:
   - **Windows:** `%APPDATA%\QGIS\QGIS3\profiles\default\`
   - **macOS:** `~/Library/Application Support/QGIS/QGIS3/profiles/default/`
   - **Linux:** `~/.local/share/QGIS/QGIS3/profiles/default/`
2. Restart QGIS and check Style Manager

---

## 🗺️ How to Use

### For Graduated Symbology (Vector Layers)

1. Right-click your vector layer → **Properties** → **Symbology**
2. Change the renderer to **Graduated**
3. Click the **Color Ramp** dropdown
4. Select **All Color Ramps** → find `Red_Yellow_Blue_1` (or 2 or 3)
5. Choose your classification column, number of classes, and mode
6. Click **Classify** → **OK**

### For Raster Layers (Singleband Pseudocolor)

1. Right-click your raster layer → **Properties** → **Symbology**
2. Set render type to **Singleband pseudocolor**
3. Click the **Color Ramp** dropdown
4. Browse to `Red_Yellow_Blue_1` (or 2 or 3)
5. Adjust min/max values and interpolation as needed
6. Click **OK**

### For Print Layouts

1. In the **Print Layout**, add a map with a graduated/pseudocolor layer
2. Add a **Legend** item — it will automatically use the color ramp
3. You can also insert a manual color bar via **Add Item** → **Scalebar** or a custom HTML frame

---

## 🎨 Color Reference

### Red_Yellow_Blue_1

| Stop | Hex | RGB | Preview |
|------|-----|-----|---------|
| 1 | `#F40303` | 244, 3, 3 | 🟥 |
| 2 | `#FDBA36` | 253, 186, 54 | 🟧 |
| 3 | `#F5F504` | 245, 245, 4 | 🟨 |
| 4 | `#95F703` | 149, 247, 3 | 🟩 |
| 5 | `#0085A8` | 0, 133, 168 | 🟦 |

### Red_Yellow_Blue_2

| Stop | Hex | RGB | Preview |
|------|-----|-----|---------|
| 1 | `#E60000` | 230, 0, 0 | 🟥 |
| 2 | `#FFAA01` | 255, 170, 1 | 🟧 |
| 3 | `#FEFF75` | 254, 255, 117 | 🟨 |
| 4 | `#93F700` | 147, 247, 0 | 🟩 |
| 5 | `#00A8E6` | 0, 168, 230 | 🟦 |

### Red_Yellow_Blue_3

| Stop | Hex | RGB | Preview |
|------|-----|-----|---------|
| 1 | `#F40000` | 244, 0, 0 | 🟥 |
| 2 | `#FC8B00` | 252, 139, 0 | 🟠 |
| 3 | `#F5F500` | 245, 245, 0 | 🟨 |
| 4 | `#AAFF01` | 170, 255, 1 | 🟩 |
| 5 | `#00A8E6` | 0, 168, 230 | 🟦 |

---

## 💡 Use Case Ideas

- **Environmental Mapping** — NDVI, vegetation health, land cover
- **Climate & Weather** — Temperature gradients, precipitation
- **Elevation & Terrain** — DEM visualization, slope analysis
- **Urban Planning** — Population density, zoning risk
- **Hydrology** — Water depth, flood risk zones

---

## 📁 File Structure

```
Red_Yellow_Blue_Colors.xml    ← QGIS Style file (v2)
├── Red_Yellow_Blue_1         ← Preset color ramp (5 stops)
├── Red_Yellow_Blue_2         ← Preset color ramp (5 stops)
└── Red_Yellow_Blue_3         ← Preset color ramp (5 stops)
```

---

## 🔧 Troubleshooting

| Problem | Solution |
|---------|----------|
| Ramps not visible after import | Restart QGIS and check **Style Manager → Color Ramps** |
| "Invalid style file" error | Ensure you're using QGIS 3.x (style version 2 format) |
| Colors look different on screen | Check your monitor calibration and project CRS |
| Ramp not in dropdown | Click **All Color Ramps** in the dropdown, not just Favorites |

---

## 📝 License

Free to use for personal and commercial projects. Attribution appreciated but not required.

---

> **Tip:** To favorite a ramp for quick access, open **Style Manager**, right-click the ramp, and select **Add to Favorites** ⭐
