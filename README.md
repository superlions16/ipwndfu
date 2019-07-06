![](repo/ipwndfu.png)
# Open-source jailbreaking tool for older iOS devices


**Read [disclaimer](#disclaimer) before using this software.*


## Features

* Jailbreak and downgrade iPhone 3GS (new bootrom) with alloc8 untethered bootrom exploit. :-)

* Pwned DFU Mode with steaks4uce exploit for S5L8720 devices.

* Pwned DFU Mode with limera1n exploit for S5L8920/S5L8922 devices.

* Pwned DFU Mode with SHAtter exploit for S5L8930 devices.

* Dump SecureROM on S5L8920/S5L8922/S5L8930 devices.

* Dump NOR on S5L8920 devices.

* Flash NOR on S5L8920 devices.

* Encrypt or decrypt hex data on a connected device in pwned DFU Mode using its GID or UID key.


## Dependencies

* libusb, `If you are using Linux: install libusb using your package manager.`
* A computer that runs macOS or Linux. This won't work on Windows or a VM with macOS or Linux.
* An old iDevice that is supported by this program. (e.g. New bootrom iPhone 3GS)


## Tutorial

This tool can be used to downgrade or jailbreak iPhone 3GS (new bootrom) without SHSH blobs, as documented in [JAILBREAK-GUIDE](https://github.com/axi0mX/ipwndfu/blob/master/JAILBREAK-GUIDE.md).


## Exploit write-up

Write-up for alloc8 exploit can be found here:

https://github.com/axi0mX/alloc8



## Coming soon! (on axi0mX's repo mainly)

* Reorganize and refactor code.

* Dump SecureROM on S5L8720 devices.

* Install custom boot logos on devices jailbroken with 24Kpwn and alloc8.

* Enable verbose boot on devices jailbroken with 24Kpwn and alloc8.

## Disclaimer

**This is BETA software.**

Backup your data.

This tool is currently in beta and could potentially brick your device. It will attempt to save a copy of data in NOR to nor-backups folder before flashing new data to NOR, and it will attempt to not overwrite critical data in NOR which your device requires to function. If something goes wrong, hopefully you will be able to restore to latest IPSW in iTunes and bring your device back to life, or use nor-backups to restore NOR to the original state, but I cannot provide any guarantees.

**There is NO warranty provided.**

THERE IS NO WARRANTY FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW. THE ENTIRE RISK AS TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU. SHOULD THE PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING, REPAIR OR CORRECTION.

## Toolchain

You will not need to use `make` or compile anything to use ipwndfu. However, if you wish to make changes to assembly code in `src/*`, you will need to use an ARM toolchain and assemble the source files by running `make`.

If you are using macOS with Homebrew, you can use gcc-arm-embedded. You can install it with this command:

```
brew cask install gcc-arm-embedded
```

## Credit

geohot for limera1n exploit

posixninja and pod2g for SHAtter exploit

iPhone Dev Team for 24Kpwn exploit

pod2g for steaks4uce exploit

walac for pyusb
