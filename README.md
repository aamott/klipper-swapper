# klipper-swapper
Toolchanger macros for Klipper. Specifically for the kind of toolchanger that uses a servomotor to lock into place. Stepper motor locks will be added shortly. 


# Getting Started
## Setup
1. Install or clone this repo into your klipper config folder.
2. Add the following to your config file:
```
[include klipper-swapper/toolchange.cfg]
```
3. Edit `toolchange.cfg` to fit your printer's configuration.

# Usage
1. Clone the repo into your klipper config folder.
2. Include `toolchange.cfg` by adding `[include klipper-swapper/toolchange.cfg]` in your config file.
3. Edit `toolchange.cfg` to fit your printer's configuration.

# Limitations
- Tools must be created in order, from 0. Numbers cannot be skipped. (i.e. "0, 1, 2...", not "0, 2, 4...")

# TODO
- [ ] Explore how to add pickup position and offsets to each extruder under the `[extruder]` section.
- [x] Fix z offet
- [ ] Simplify setting z offset
    - [ ] Change and save x/y/z offsets live, without changing the config file.
- [x] Load offsets on startup
- [ ] Automatic x/y/z offset calibration (with a load cell?)
- [x] First successful print using tool 2
- [x] First successful print using 2 tools
- [x] Ensure tools lift at least a certain distance above the bed. (ex. 1mm z raise raises 5mm on the first layer, but 1mm after 4mm)
- [ ] Slope lift z while docking tool, but no more than Xmm (ex. slope z lift for 30mm, then only x,y move for the rest of the tool return)
- [ ] Customizable lock function (stepper motors, servo, magnetic, no lock)
- [ ] Optional separate return position (for Prusa XL style toolchagers that move x axis to lock)
- [ ] Separate fan control for each tool