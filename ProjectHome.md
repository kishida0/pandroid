# THIS PROJECT IS NO LONGER BEING ACTIVELY DEVELOPED #
## AOSP & Linaro's LEB now have support for PandaBoard see http://omappedia.org/wiki/Android_on_PandaBoard ##





# Project Goal #
Pandroid is full featured port of Android on [PandaBoard](http://pandaboard.org).

# Getting started #
  * Lean more about [PandaBoard](http://omappedia.org/wiki/PandaBoard)
  * Current status listed below
  * Review the latest release notes at: http://www.omappedia.org/wiki/PandaBoard_L27.12.1-P2_Release_Notes

# Supported Platforms #
  * [PandaBoard](http://pandaboard.org) Rev A1 - ES2.1
  * [PandaBoard](http://pandaboard.org) Rev EA1 (Early Board Adopters)
  * [PandaBoard](http://pandaboard.org) ES2.0 Prototypes -- not tested on GB release

# Features #

### Gingerbread ###
  * DRAFT release is available see Getting Started above
    * Limited support at this time
    * See Updates below for current status

### Froyo 2.2 ###
  * External monitor via HDMI/DVI
  * USB Keyboard
  * USB Mouse with mouse cursor
  * Wifi/802.11n
  * Bluetooth
  * Ethernet

# Source Trees #
  * Kernel: git clone git://git.omapzoom.org/kernel/omap.git kernel/android-2.6.35
    * branch: p-android-omap-2.6.35

### TI bootloader release ###
  * u-boot: git clone git://git.omapzoom.org/repo/u-boot.git u-boot
    * branch: omap4\_dev

  * x-loader: git clone git://git.omapzoom.org/repo/x-loader.git x-loader
    * branch: omap4\_dev

### Android Gingerbread Release ###
  * gingerbread: $repo init -u git://git.omapzoom.org/platform/omapmanifest.git -b gingerbread


# Submitting Patches #
Refer to: http://www.omappedia.com/wiki/Gerrit

Add the following reviewers: Omar Barron and Vikram Pandita




&lt;hr&gt;



# Update #
  * 6/16/11
    * It's been brought to our attention that the music.apk and other apps are still crashing on latest release. We have a solution for this issue but it seems it was not included in the binary release. We will upload another release next week which should have this included. Patch is located in binary folder. Sorry for the inconvenience.
  * 6/13/11
    * New Gingerbread release updated -- DRAFT rls\_v2
    * WLAN/GFX included
    * Hotspot functional
    * Audio playback functional
    * Music.apk should be stable -- report any trouble on issues page
    * HDMI to DVI tested and functional
    * HDMI tested and functional
    * ADB functional through OTG
    * Ethernet not tested -- members report this working
    * Mic not tested
    * video playback -- webm playback seems to be working
    * NOTE: Create a 3rd partition on SD card and load media content to this partition.
  * 6/09/
    * We have fix for music.apk
    * New release expected on 6/10/11
  * 6/08/11
    * WLAN is functional
    * pushing out new binary later this week
  * 6/06/11
    * Audio patch is under review in Gerrit.
    * Patch Link: http://review.omapzoom.org/#change,13276 -- Patch Set 5
    * Known issue: Android music.apk is crashing when selected.
    * Work around: Install Meridian.apk for audio playback
  * 6/03/11
    * Audio is working to some degree.
    * Current Android Music Player is crashing but if we use Meridian we am able to play back audio files.
    * Update patches will be posted when a more stable solution is found.
  * 5/25/11 -- Uploaded a "DRAFT release"
    * Draft does not have wlan and AV playback
    * Tested on HDMI
    * Tested on SD boot
    * ADB working with USB OTG w/power supply connected
    * Fastboot enabled but not part of Draft release
    * Includes patches required to build current environment
  * 5/17/11 -- Gingerbread pushed into Gerrit for review. Fastboot tested and enabled by default.
  * 5/12/11 -- Gingerbread "DRAFT" release notes are now available at: http://www.omappedia.org/wiki/PandaBoard_L27.12.1-P2_Release_Notes
    * TODO's: Audio fix for android, Ducati binaries required for AV playback, Clean up PandaBoard device directory in Gerrit, Test OTG, Test Fastboot, Add and test WLAN/BT
    * Support is limited at this time..
    * Looking for volunteers to test fastboot setup...
  * 4/21/11 -- New audio patches were submitted for testing. Works on Minimal-FS validation environment but still need to test within Android rootfs.
    * "http://review.omapzoom.org/#change,13001"
    * "http://review.omapzoom.org/#change,13002"
  * 3/28/11 -- L27.10.2-P1 Froyo Release for Pandroid is available.
    * Release Notes: http://www.omappedia.com/wiki/PandaBoard_L27.10.2-P1_Release_Notes
    * Connectivity (WLAN/BT) was validated - Firmware and patch subset are available at: https://gforge.ti.com/gf/download/frsrelease/514/4465/Froyo_L27.10.2-P1_Connectivity_127x-1.0-Linux-x86-Install-1.0
    * GFX acceleration install is available at: https://gforge.ti.com/gf/download/frsrelease/493/4368/Froyo_L27.10.2-P1_Graphics-1.0-Linux-x86-Install

## Release Notes ##
Information is available at: http://www.omappedia.com/wiki/Release_Notes
-- latest stable release:  http://www.omappedia.com/wiki/PandaBoard_L27.10.2-P1_Release_Notes

## Notes ##
We no longer use gitorious.org/pandroid for this project. Android's Kernel and filesystem is now part of www.omapzoom.org.



&lt;hr&gt;



# What we are working for Gingerbread #
  * Verify ARM based AV playback
  * Accelerated 1080p AV Playback

# ToDo List #
  * USB Camera support
  * USB Mass storage support
  * [External USB Touchscreen](http://www.thinkgeek.com/computing/usb-gadgets/bfa3/#tabs)
  * [LEDs for heartbeat & MMC](http://gitorious.org/pandaboard/kernel-omap4/commit/6167d351752ad23d8a46dfa65383f39187727dc1)
  * [Touchscreen support on LCD Expansion](https://specialcomp.com/beagleboard/LB043WQ1-TD01(070330).pdf1)
  * External Display on PandaBoard's DVI-D port
  * Enable built-in GPIO Button

# How to contribute #
  * You can submit fixes for [known issues](http://code.google.com/p/pandroid/issues/list)
  * Take up issues that are on the todo list
  * You can email your patches to [pandaboard@googlegroups.com](http://groups.google.com/groups/pandaboard)
    * Add "PANDROID-PATCH" in subject.
    * Review & follow the patch guidelines at [here](http://omappedia.org/wiki/Releasing_to_Linux_kernel_using_patches_and_emails).
  * Review Gerrit process at: http://www.omappedia.com/wiki/Gerrit
  * Add the following reviewers to your patches: Omar Barron and Vikram Pandita

# Support & Community #
  * IRC: [#pandaboard](http://pandaboard.org/irc) on irc.freenode.net
  * Mailing List: [pandaboard@googlegroups.com ](http://groups.google.com/group/pandaboard)
