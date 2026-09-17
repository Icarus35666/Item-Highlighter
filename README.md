# Item Highlighter
Version 1.0.2

![icon.jpg


Item Highlighter is a QGIS plugin developed for INSA Rennes.

It allows users to highlight features from one or several layers using configurable drop-down lists based on attribute values.

---

## Features

- Highlight features from up to 10 layers
- Dynamic layer selection
- Dynamic field selection
- Automatic zoom to selected features
- Custom border color
- Custom fill color
- Custom border width
- Save configuration to JSON
- Load configuration from JSON
- Reset configuration
- Support for multiple geometries

---

## How it works

### 1. Configure the plugin

Open the Settings dialog and define:

- Layer
- Attribute field
- Highlight border color
- Highlight fill color
- Highlight border width

Save the configuration to a JSON file.

![ ](https://espaces-verts.insa-rennes.fr/images/ImagesReadMePlugin/ReadMe_Setting.jpg)

---

### 2. Launch Item Highlighter

After loading the configuration, the main dialog displays one combobox for each configured layer.

Example:

```text
Trees
[ Oak ▼ ]

Shrubs
[ Rose ▼ ]

Perennials
[ Lavender ▼ ]
```

![ ](https://espaces-verts.insa-rennes.fr/images/ImagesReadMePlugin/ReadMe_MainWindow.jpg)
---

### 3. Select a value

When a value is selected:

- matching features are searched
- features are highlighted
- the map automatically zooms to the selected features

![ ](https://espaces-verts.insa-rennes.fr/images/ImagesReadMePlugin/ReadMe_List.jpg)

![ ](https://espaces-verts.insa-rennes.fr/images/ImagesReadMePlugin/ReadMe_Canvas.jpg)
---

## Configuration file

Settings are stored in JSON format.

Example:

```json
{
    "item_1": {
        "layer": "Trees",
        "field": "Name",
        "borderColor": "#693400",
        "fillColor": "#ffb1007b",
        "borderWidth": 3
    }
}
```

---

## Requirements

- QGIS 3.x
- QGIS 4.x
- Python 3
- PyQt5

---

## Installation

1. Download or clone the repository.
2. Copy the plugin folder into the QGIS plugins directory.
For QGIS3 :(C:\Users\...\AppData\Roaming\QGIS\QGIS3\profiles\default\python\plugins\item_highlighter)
For QGIS4 :(C:\Users\...\AppData\Roaming\QGIS\QGIS4\profiles\default\python\plugins\item_highlighter)
3. Restart QGIS.
4. Enable the plugin from:

```text
Plugins > Manage and Install Plugins
```

---

## Usage

1. Open the plugin.
2. Configure layers and fields.
3. Save the settings.
4. Select values from the generated comboboxes.
5. View highlighted features directly on the map canvas.

---

## Author

François Thouanel

INSA Rennes

---

## License

This project is released under the GNU General Public License (GPL v2 or later).

---

## Changelog

    Version 1.0 Stable
    - Added JSON save/load support
    - Added reset button
    - Added layer not found warning
    - Added no feature found warning
    - Improved dialog management
    - Improved canvas interaction
    - Prevented multiple plugin instances
    - Improved configuration handling
	Version 1.0.1
	- Added QGIS 4 / Qt6 compatibility
	- Updated metadata
	- Updated changelog
	- Fixed Qt5/Qt6 compatibility issues
	Version 1.0.2
	- Fix Qt6 check issue
