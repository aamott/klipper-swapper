# klipper-swapper
Toolchanger macros for Klipper. Specifically for the kind of toolchanger that uses a servomotor to lock into place. Stepper motor locks will be added shortly. 

# Usage
1. Clone the repo into your klipper config folder.
2. Include `toolchange.cfg` by adding `[include klipper-swapper/toolchange.cfg]` in your config file.
3. Edit `toolchange.cfg` to fit your printer's configuration.

# TODO
- [ ] Explore how to add pickup position and offsets to each extruder under the `[extruder]` section.
- [x] Fix z offet
- [ ] Simplify setting z offset
    - [ ] Change and save x/y/z offsets live, without changing the config file.
- [ ] Automatic x/y/z offset calibration (with a load cell?)
- [x] First successful print using tool 2
- [x] First successful print using 2 tools
- [ ] Ensure tools lift at least a certain distance above the bed. (ex. 1mm z raise raises 5mm on the first layer, but 1mm after 4mm)
- [ ] Customizable lock function (stepper motors, servo, magnetic, no lock)
- [ ] Optional separate return position (for Prusa XL style toolchagers that move x axis to lock)