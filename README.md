2D-injector
2D Injector: An AetherVisor-based DLL injector.

In the proof of concept code, I use NPT to stealthily map an unsigned payload DLL in the same address space as OWClient.dll (Overwolf's overlay DLL). Not only does the 2D injector bypass memory permission scans and DLL certificate checks, but it also renders the payload DLL invisible and unreadable.

This was tested and is undetected on Fortnite and EFT, but the major caveat was injector caused FPS drops with cheats.

I can see this being used for things other than cheating, such as debugging heavily protected apps or hiding from EDR.



![226236958-1166af80-bb8b-4c60-a148-7227ec157775](https://user-images.githubusercontent.com/101047931/227345207-192ef8d4-734d-4e14-9042-c76347cf1a4d.png)


Acknowledgements:
To red0x0002 https://www.github.com/red0x0002 : Thank you to for helping me test the injector and giving me tips.
