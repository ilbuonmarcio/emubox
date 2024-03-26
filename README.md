# emubox

This project is the direct aftermath of the (allegedly) shitty support provided by RetroArch for configuring CRT displays with custom super resolutions in both Windows, Linux and Lakka: it aims at having a shortcut-based i3wm configuration for playing your emulated games without having to bang your head to the _**fucking**_ table each time something misconfigures or does what you didn't expect, while having pixel-perfect retrostyle gameplay look and feel.

I hope you like it as I do!

Now... ARE YOU READY FOR SOME _**THICC**_ SCANLINES?!?

### How to use

With all the following files properly set up, start i3 and with the following keyboard shortcuts you can, at every time, change the current resolution of your display:

- Max Original resolution: Win+Control+1
- 240p Super resolution: Win+Control+2
- 360p Super resolution: Win+Control+3
- 480p Super resolution: Win+Control+4
- 540p Super resolution: Win+Control+5
- 640p Super resolution: Win+Control+6

As you can see, it's easy to remember because the first number of the resolution matches the number of the shortcut!

### Modes supported

**!! CAUTION !!** These config files may NOT be supported by your CRT monitor, be careful and be sure they will work with your setup, I'm not responsible for damaged hardware and broken hearts, okay? :P

- Regular: 2048x1536 @ 69Hz
- Super: 2560x**240p** @ 150Hz
- Super: 2560x**360p** @ 150Hz
- Super: 2560x**480p** @ 150Hz
- Super: 2560x**540p** @ 150Hz
- Super: 2560x**640p** @ 150Hz

All tested on a pair of LG F900P with the following specs:

- Default resolution: 1600x1200 @ 60Hz
- Max resolution: 2048x1536 @ 69Hz
- Horizontal Sync Range: 30.0kHz - 111.0kHz
- Vertical Refresh Range: 50.0Hz - 160.0Hz

**For your hardware, I'll suggest you to check the hardware specification of your monitor and see if the configs in this project are compatible with it, and otherwise disable or adapt the scripts to your setup with custom `cvt` parameters.**

### Requirements, Hardware Tested & Suggestions

These config files are tested and working with the current prerequisites:

- An Nvidia graphics card with DVI analog hardware support output and a 400MHz integrated DAC
    - Currently available hardware in my office:
        - [x] NVIDIA GTX TITAN X (Maxwell)
        - [x] NVIDIA GTX 980 Ti
        - [x] NVIDIA GTX 980
        - [ ] NVIDIA RTX 4090 (with a dedicated near-400MHz DisplayPort to VGA converter, because no analog output is provided sadly... [this one (StarTech DP2VGAHD20)](https://www.amazon.it/dp/B0849FTBXQ/) provides no latency and is good for the job with newer graphics cards without a native analog output!)
        - [ ] AMD R7 260X, which has a 400MHz DAC too
- Arch Linux installed with:
    - i3 window manager with `ly` login manager
    - NO compositor (comptron/picom is highly **not** recommended as of now)
    - nvidia proprietary drivers (amdgpu driver will be tested with the R7 260X above, if I have time) with custom resolutions setup via xorg.conf file
    - kitty terminal for pretty terminal file editing :nail_care:
    - a controller (PS5 controller via USB was tested and is good)
- Some emulators! The one tested and good with this setup were:
    - **NES**: [fceux](https://github.com/TASEmulators/fceux)
    - **GB/GBC/GBA**: [mgba](https://github.com/mgba-emu/mgba) (with `mgba-qt` package for GUI access if needed)
    - **SEGAMEGADRIVE**: [ares](https://github.com/ares-emulator/ares)

### Things that remains to be tested and/or done

- R7 260X (and in general GPUs with analog output that are supported by the `amdgpu` driver under Linux) 
- 15kHz displays, that are otherwise called CRT TVs :smirk:
    - I currently have a wide Sony Trinitron KV-36FS70 36" to test, I hope it will work with a VGA to RGB cable and the COMP2RGBSCART from RetroTink that I already have!
- Other emulators, of course!
- Maybe creating an already built ISO file to image a disk and be ready to rock as fast as you can? 👀

## License

This software is licensed under the MIT License. See `LICENSE` file for more information.