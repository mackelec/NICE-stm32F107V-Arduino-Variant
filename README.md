# NICE-stm32F107V-Arduino-Variant
A custom variant for stm32Duino for the `stm32F107VCT` processor, specifically tailored for the 'NICE' (Nissan Inverter Controller par Excellence) PCB.

## Installation
1. Navigate to your stm32Duino variants directory. It should be something like:
```
.../variants/STM32F1xx
```
2. Create a folder named `F107VC(NICE)` within this directory.
3. Download the following files and place them into the `F107VC(NICE)` folder:
    - `boards_entry.txt`
    - `CMakeLists.txt`
    - `generic_clock.c`
    - `ldscript.ld`
    - `PeripheralPins.c`
    - `PinNamesVar.h`
    - `variant_generic.cpp`
    - `variant_generic.h`

4. Before proceeding, it's recommended to backup your original `boards.txt` located at:
```
.../packages/STMicroelectronics/hardware/stm32/2.4.0
```
5. Copy the provided `boards.txt` and overwrite the `boards.txt` in the directory mentioned above. 

## Notes
- This variant is set up for an 8MHz crystal, and the processor runs at 72MHz. This configuration is essentially the same as a BluePill in this regard.
- Currently, compatibility is maintained up to core version `2.4.0`.
