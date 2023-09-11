# dolphin-quick-view

A simple program to have a quick preview of the files in a folder (similar to Apple's Quick Look)

![Screenshot-10-09-2023-CEST](https://github.com/Nyre221/dolphin-quick-view/assets/104171042/38bfe4e8-80da-4634-98d9-00a0f2a8c1ad)

Supported files: mp3,mp4,jpg,webp,svg,svgz,doc,docx,odt,xls,xlsx,csv,ods,md,pdf

## Installation:
### Dependencies

kubuntu 20
``` 
sudo apt install python3-pip python3-qpageview python3-pyqt5.qtsvg  python3-pyqt5.qtmultimedia antiword python3-poppler-qt5 gstreamer1.0-libav && pip install pyexcel pyexcel-xls pyexcel-xlsx textract
 ```

kubuntu 22
```
sudo apt install antiword python3-pyqt5.qtmultimedia gstreamer1.0-libav python3-poppler-qt5 python3-pip python3-qpageview && pip install pyexcel pyexcel-xls pyexcel-xlsx textract
```

kubuntu 23
```
sudo apt install python3-pyqt5.qtmultimedia python3-poppler-qt5 python3-pip python3-qpageview antiword gstreamer1.0-libav && pip install pyexcel pyexcel-xls pyexcel-xlsx textract --break-system-packages
```

fedora 37
```
sudo dnf install python3-qt5 python3-poppler-qt5 antiword gstreamer1-plugin-libav gstreamer1-plugin-openh264 python3-qpageview && pip install pyexcel pyexcel-xls pyexcel-xlsx textract
```

fedora 38
```
sudo dnf install python3-qt5 python3-pip antiword python3-poppler-qt5 python3-qpageview gstreamer1-plugin-libav gstreamer1-plugin-openh264 & pip install pyexcel pyexcel-xls pyexcel-xlsx & pip install textract
```

Arch/Manjaro:
```
sudo pacman -S python-pyqt5 python-poppler-qt5  python-pip  python-qpageview antiword && yay -S python-pyexcel python-pyexcel-xls python-pyexcel-xlsx python-textract
```


### Install:
Download the latest Release
```
cd ~/Downloads && curl -O https://github.com/Nyre221/dolphin-quick-view/releases/latest/download/dolphin_quick_view.tar.gz
```

Extract the code and enter the directory
```
tar -xf dolphin_quick_view.tar.gz && cd dolphin_quick_view
```

Make the install file executable
```
chmod +x INSTALL.sh
```

## Usage
### Application Keyboard Shortcuts:

| Key  | Function |
| ------------- | ------------- |
| `A` or `LEFT`| Previous File  |
| `B` or `RIGHT`  | Next File  |
| `spacebar` or `Q` or `ESC` | Quit |
| `W` or `UP`  | open with default app  |


### Create a System Keyboard Shortcut
`plasma settings` -> `Shortcuts` -> `Shortcuts` -> `Add a Command` 

```
~/.config/quick_view/dolphin_quick_view_shortcut.sh 
```

### Dolphin Dialog Menu
Right-click an item and select `Quick view`


## Debug:
If quick view doesn't open via Dolphin's dropdown menu:
Open a terminal and type 
```
dolphin
``` 
Error messages will appear in the terminal window (possible missing dependencies)

If dolphin_quick_view_shortcut.sh doesn't work, run: 
```
sleep 5 ; ~/.config/quick_view/dolphin_quick_view_shortcut.sh
```
And reactivate a dolphin window (you have 5 seconds).
The errors should appear there.

If PDFs are not visible, it is because you have not installed python3-qpageview or python3-poppler-qt5 (names may differ a bit)

If some mp4 files don't play, it's probably because you're missing some gstreamer library

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.paypal.com/donate/?hosted_button_id=J7QU55MMUP4G4)
