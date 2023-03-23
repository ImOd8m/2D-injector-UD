2D-injector
2D Injector: An AetherVisor-based DLL injector.

In the proof of concept code, I use NPT to stealthily map an unsigned payload DLL in the same address space as OWClient.dll (Overwolf's overlay DLL). Not only does the 2D injector bypass memory permission scans and DLL certificate checks, but it also renders the payload DLL invisible and unreadable.

This was tested and is undetected on Fortnite and EFT, but the major caveat was injector caused FPS drops with cheats.

I can see this being used for things other than cheating, such as debugging heavily protected apps or hiding from EDR.


image



Acknowledgements:
To red0x0002 https://www.github.com/red0x0002 : Thank you to for helping me test the injector and giving me tips.

USAGE:
Compile AetherVisor.sys: https://github.com/MellowNight/AetherVisor
Compile Injector-driver
Compile Injector-client with three parameters in injection_info.h : HOST_DLL_PATH, HOST_DLL_NAME, and ENTRYPOINT_NAME
kdmapper.exe AetherVisor.sys
kdmapper.exe injector-driver.sys
Run Injector-client as administrator
Follow the prompt, provide the target PID and path to your own cheat DLL
