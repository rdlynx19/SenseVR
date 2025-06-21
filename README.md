# SenseVR  

SenseVR is a SteamVR-compatible VR system built on top of [HadesVR](https://github.com/HadesVR/HadesVR). I’ve redesigned the headset and am currently developing custom controllers. Future updates will also include improvements to the software stack.

*Hades* : The setup includes DIY controllers that are capable of emulating HTC vive wands. It also includes tracking electronics for a Headset, including an integrated wireless receiver to receive the controllers' data.

My current focus is prototyping the controllers, followed by learning PCB design to create custom controller boards. After that, I plan to 3D print the controller shells and update the software stack accordingly.

*Hades* : The SteamVR driver used to be based off of [TrueOpenVR](https://github.com/TrueOpenVR) but it's modified so heavily I'm making it it's own thing.
This driver also uses [PSMoveServiceEX](https://github.com/Timocop/PSMoveServiceEx) (for now at least) for the positional tracking of HMD and controllers, using ping pong balls and different colours of LED's.

For more information on *everything*, check out the [docs](docs/DocsIndex.md)!

![1](docs/img/Headset.png)

# How does it work and what can it do?
*Hades* :

The headset connects to the PC and receives rotation and button data from both controllers through RF, while the tracking is done outside-in (base stations) using Playstation Move Cameras and [PSMoveService](https://github.com/psmoveservice/PSMoveService).

You can use the setup in: 
* Headset and controllers mode: The headset receives data from the controllers and mixed with the PSMoveService position tracking you get full 6dof tracking.
* Headset only mode: where you only have your HadesVR headset and the 6dof tracking (or 3dof if you don't use PSMoveService)
* Controller only mode: where if you already have a headset, you can use only the controllers part of the setup (you'll need to build an [RF receiver](docs/RFReceiver.md) to replace the HadesVR headset's built in one).

## What it can and cannot do:
* This driver can emulate Wand and Index controllers.
* This setup cannot do Inside out tracking.
* This driver cannot do Full body tracking ~~**yet**~~.
* Yes this thing plays beatsaber though I'm not sure how viable it is for expert+ diff since I suck at it.

# Demos
*Hades* :

I've recorded a few demos of my HadesVR setup working in different games, these are all available in this [Youtube Playlist](https://www.youtube.com/playlist?list=PLPNX9YMrhQR2g2nwp1AN23K4V-8d-4bBV)

