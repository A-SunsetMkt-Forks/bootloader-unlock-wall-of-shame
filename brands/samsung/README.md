# Samsung

- Verdict: **🍅 Terrible!**
* [**🔓️ Unlock Guide (supported devices)**](../../misc/samsung-unlock.md)

If you have a North American device and were lucky enough not to update for a while, you can check out [this paid service][Paid North American Unlock] at your own risk. Exynos devices, regardless of region, can be unlocked assuming you're on One UI 7 or earlier. 

Until recently, international Samsung devices (e.g. ones sold in Europe or Asia) were unlockable, however, starting with One UI 8, Samsung has [completely nuked][One UI 8 Unlock] the ability to unlock their devices, regardless of model or region. If you are still on One UI 7 or earlier, **DO NOT UPDATE.** Once you update to One UI 8, bootloader unlocking is gone forever, there is no way to rollback to One UI 7.

Snapdragon phones prior to the S7/Note7 (2016) can be unlocked regardless of region, as long as it's not locked to a carrier like AT&T or Verizon. The Canadian S7 can also be unlocked as it uses an Exynos SoC, despite Canada normally being a Snapdragon region.

Be aware that unlocking a Samsung device will permanently trip Knox. As a result, many Knox-based features will be broken. This includes, but not limited to: Samsung Pay, Pass, Flow, Health, Secure Folder, Secure Wi-Fi, Smart View. Furthermore, tripping Knox may serve as grounds for voiding your warranty.

In the past, there have been hardware issues caused by unlocking the boatloader, but these have been fixed for some regions. See [here][1] and [here][2]. As of late 2023, Kroean Galaxy Fold3 running OneUI 5 still got camera disabled after unlocking, while EU/CN variants had fixed the issue.

## SoC level exploits
One of the first things Samsung bootloaders do on phone bootup is check if the bootloader is unlocked, and if it is, and a bootloader unlock has not been authorized, the bootloader will automatically relock. This means SoC level exploits such as mtkclient or EDLUnlock will not work on Samsung devices, unless you reverse engineer, modify and re-flash Samsung's bootloader to stop the bootloader from re-locking. 

## KnoxPatch

Some of Knox-based features can be fixed with this LSPosed module [KnoxPatch] and its companion Magisk/KernelSU module [KnoxPatch#knoxpatch-enhancer].

## VoLTE on Custom ROMs

Samsung's IMS service is not compatible with AOSP's, so VoLTE will not work on GSI ROMs.

There is an [open source VoLTE service] developed by phh, but it's incomplete and not stable.

***
Additional info provided by [aries-ts-indo](https://github.com/aries-ts-indo) and [Ivy / Lost-Entrepreneur439](https://github.com/Lost-Entrepreneur439).<br/>
Authored by [melontini](https://github.com/melontini).

[1]:https://www.xda-developers.com/bootloader-unlocking-no-longer-kills-galaxy-z-fold-3-cameras/
[2]:https://www.xda-developers.com/samsung-galaxy-s22-bootloader-unlock-camera-working/

[open source VoLTE service]:https://github.com/phhusson/ims
[Paid North American Unlock]:https://xdaforums.com/t/android-unsamlock-bootloader-unlock-for-samsung-us-canada-devices.4215101/
[KnoxPatch]:https://github.com/BlackMesa123/KnoxPatch
[KnoxPatch#knoxpatch-enhancer]:https://github.com/BlackMesa123/KnoxPatch#knoxpatch-enhancer
[One UI 8 Unlock]:https://xdaforums.com/t/bootloader-unlocking-option-removed-from-one-ui-8-0.4751904/
