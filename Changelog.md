Changelog EFI

======================================================
#### OpenCore v0.9.4
- Fixed kext blocker `Exclude` strategy for prelinked on 32-bit versions of macOS
- Fixed `ForceAquantiaEthernet` quirk on macOS 14 beta 2, thx @Shikumo
- Added `InstanceIdentifier` to OpenCore and option to target `.contentVisibility` to specific instances (thx @dakanji)
- Improved `LapicKernelPanic` quirk on legacy versions of macOS
- Allowed `.contentVisibility` in same boot FS root locations as `.VolumeIcon.icns`, in order to survive macOS updates
- Fixed incorrect core count on Silvermont Atom/Celeron processors
- Fixed PM timer detection on Silvermont Atom/Celeron processors for TSC calculations
- Fixed PM timer detection on non-Intel chipsets when booted through OpenDuet
- Fixed `FadtEnableReset` on NVIDIA nForce chipset platforms
- Added BlockIoDxe alternative OpenDuet variant
- Added support for ATI cards when using `ForceResolution` option

#### AirportItlwm v2.3.0 - 09/08/2023
- Implementado no config.plist

#### AppleALC v1.8.4
- Added ALC262 layout-id 14 for Dell Studio One 19 1909 by Goldfish64
- Headphones Fix ALC255 layout-id 69 by juniorcaesar 
- Added ALC289 layout-id 33 for Asus ROG Zephyrus G14 GA401IV & fix layout-id 93 in xml
- Added Conexant CX20632 layout-id 21 for Axioo MyPC One Pro H5 by Andres ZeroCross
- Added ALC257 layout-id 101 for Lenovo XiaoXin Air14ALC by htmambo
- Added ALC236 layout-id 19 for Lenovo IdeaPad 500-14ISK. Enables Internal Speakers, Internal Mic, Jack Microphone and Jack Headphones by wolf606
- Added ALC289 layout-id 12 for XPS 13 9300 with working headphones and external microphone by wern-apfel
- Added ALC269 layout-id 38 for Fujitsu Esprimo D552 by jayveeballesteros
- Fix no sound after sleep/wake for ALC891 layout 11 by portrayer

#### ECEnabler v1.0.5
- Implementado no config.plist

#### Lilu v1.6.7
- Added Broadwell-EP CPU model
- Added Raptor Lake C0 stepping model

#### NVMeFIX v1.1.1
- Added constants for macOS 14 support
- Fixed macOS 14 compatibility
- Implementado no config.plist

#### WhateverGreen v1.6.6
- Extended the Backlight Registers Alternative Fix (BLT) submodule to support both KBL and CFL platforms. (by @0xFireWolf)
- Revised the Backlight Registers Fix (BLR) submodule to make it compatible with the Backlight Smoother (BLS) on KBL platforms. (by @0xFireWolf)

======================================================
#### OpenCore v0.9.3
- Added `--force-codec` option to AudioDxe, thx @xCuri0
- Downgraded additional warning message in normal operation of emulated NVRAM to info
- Disabled not present DVL0 device in SSDT-SBUS-MCHC by default, thx @stevezhengshiqi
- Added EFI mandated box drawing, block element and arrow characters to `Builtin` renderer console font
- Improved support for overlong menu entries and very narrow console modes in builtin picker
- Made `Builtin` text renderer ignore UI Scale, when required to ensure that text mode reaches minimum UEFI supported size of 80x25
- Added save and restore of text and graphics mode round tools and failed boot entries
- Updated out-of-range cursor handling to work round minor display issue in memtest86
- Added optional `--enable-mouse-click` argument to `CrScreenshotDxe` driver to additionally respond on mouse click
- Added `--use-conn-none` option to `AudioDxe` driver to discover additional usable output channels on some systems
- Added `PciIo` protocol override used to fix Aptio IV compatiblity with Above 4G BARs, thx @xCuri0
- Fixed `AppleXcpmForceBoost` quirk on macOS 14
- Updated builtin firmware versions for SMBIOS and the rest
- Added `ConsoleFont` option to load custom console font for `Builtin` renderer
- Improved `XhciPortLimit` quirk on macOS 11 to 14

#### AppleALC v1.8.3
- Added layout-id 73 for the ALC283/ThinkCentre M73 Tiny by UHDbits
- Added constants for macOS 14 support

#### VIrtualSMC v1.3.2
- Added NCT6799D support by @Lorys89
- Added preliminary macOS 14 support
- Added FAN controls for ITE chips by @xCuri0

#### WhateverGreen v1.6.5
- Added constants for macOS 14 support
- Added a new boot argument -igfxblt to revert the optimizations done by the compiler in backlight related functions, fixing the 3-minute dark screen issue and making Backlight Smoother (BLS) work on mobile Coffee Lake platforms running macOS 13.4 or later. (by @0xFireWolf)

#### FeatureUnlock v1.1.5
- Added constants for macOS 14 support

#### BrcmPatchRAM v2.6.7
- Added constants for macOS 14 support

#### Lilu v1.6.6
- Fixed macOS 13+ installer detection regression in 1.6.5
- Allow loading on macOS 14 without -lilubetaall

======================================================
#### OpenCore v0.9.2
- Added `DisableIoMapperMapping` quirk, thx @CaseySJ
- Fixed disabling single user mode when Apple Secure Boot is enabled
- Improved guard checks for `GopBurstMode` on systems where it's not needed
- Improved compatibility of `GopBurstMode` with some very non-standard GOP implementations
- Fixed possible hang with `GopBurstMode` enabled on DEBUG builds
- Enabled `GopBurstMode` even with natively supported cards, in EnableGop firmware driver
- Fixed inability to patch force-injected kexts
- Fixed `ExternalDiskIcons` quirk on macOS 13.3+, thx @fusion71au
- Fixed various recent reversions and some longer-standing minor bugs in `Builtin` text renderer
- Applied some additional minor optimizations to `Builtin` text renderer
- Implemented `InitialMode` option to allow fine control over text renderer operating mode
- Added support for `ConsoleMode` text resolution setting to `Builtin` renderer
- Fixed regression for ACPI quirks `RebaseRegions` and `SyncTableIds`
- Updated build process to provide stable and bleeding-edge versions of `EnableGop`
- Implemented minor improvements in `PickerMode` `Apple`
- Improved filtering algorithm for `LogModules` and added `?` filter for matching non-standard log lines
- Fixed crash when gathering system report on virtualised CPUs
- Fixed unnecessary warning when first booting with emulated NVRAM
- Enabled `AppleCpuPmCfgLock` quirk on macOS 13

#### Lilu v1.6.5
- Fixed macOS 13+ recovery and installer detection

#### AppleALC v1.8.2
- Added ALC1220 layout-id 18 for Gigabyte Z490 Aorus Master by hgsshaanxi
- Fixed LayoutId 21 for ALC298 on X270 by MKjanek32

======================================================
#### OpenCore v0.9.1
- Fixed long comment printing for ACPI patches, thx @corpnewt
- Added sample config for VS Code source level debugging with `gdb`
- Updated builtin firmware versions for SMBIOS and the rest
- Added GOP memory caching report to `SysReport`
- Implemented `GopBurstMode` quirk for faster GOP operation on older firmware
- Fixed `ThirdPartyDrives` quirk on macOS 13.3 and above

#### VoodooPS2 v2.3.5
- Removed actAsTrackpad and related logic
- Fix Trackpoints connected to Elan Touchpads
- Use VoodooInput Trackpoint logic for Elan Touchpads

#### AppleALC v1.8.1
- Added ALC293 layout-id 31 for Hasee Z7-CT7NA by lgh07711
- Added Alder Lake PCH-P High Definition Audio Controller (0x51C8) by DalianSky
- Added ALC269 layout-id 111 for minisforum NAG6 by DalianSky
- Added ALC623 layout-id 13 for Lenovo ThinkCentre M720e with internal speaker by Pinokyo-H
- Added ALC295 layout-id 11 for ZenBook UX581 by wern-apfel
- Added ALC255 layout-id 37 for Acer Nitro 5 AN515-52-73Y8 by imoize

======================================================
#### OpenCore v0.9.0
- Resolved issues with verbose boot log appearing over picker graphics
- Added version number to EnableGop UI section, so tool builders can track it
- Added ProvideCurrentCpuInfo support for macOS 13.3 DP
- Added AMD support, GOP offset auto-detection and macOS 10.11+ support to EnableGop vBIOS insertion script
- Included precompiled EDK-II EfiRom and GenFfs in Utilities/BaseTools with OpenCore releases