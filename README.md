# qmk-keymap-keyball46
Keyball46 Custom Firmware


Disclaimer:
The original firmware was developed by https://github.com/Yowkees/keyball, this is a variation and modifications for my own need.


## setup 
```
# setup qmk sub-modules
git submodule update --init
cd qmk_firmware && make git-submodule && python3 -m pip install --user qmk && qmk setup

# linking keyboard files
ln -s $(pwd)/keyball $(pwd)/qmk_firmware/keyboards/keyball


# build qmk hex files keyball_keyball46_j1n6.hex
# a single file can be flashed to both left and right side
qmk compile -j 4 -kb keyball/keyball46 -km j1n6
```
