# a9lh-guide

A simple guide to install A9LH in 2025.

Note that my english isn't that good, I'm sorry if I make mistakes.

Alright, want to install A9LH on your 3DS for whatever reason?
I gotcha.

# IF YOU DO NOT KNOW WHAT YOU'RE DOING, GET THE FUCK OUT
- This guide is only intended for users who know what they are doing, I am not responsible if you brick your 3DS.

# PLEASE, REALLY
- I'm insisting, you should have a bit of knowledge. If you truly want CFW for daily use on your 3DS, just go to https://3ds.hacks.guide to install boot9strap and get out.
Alright, now that it's said, let's start for real.

If you want to show me you succeded, you can send me a mail right here: maylina53uwu@gmail.com or just dm me on discord: maylina53_uwu
(Or if you want help, but it's not likely that I'll answer, especially if you didn't follow the steps correctly.)

# Summary

- [Requirements](#requirements)
- [Preparation](#preparation)
- [Downgrade](#downgrade)

# Prerequisites

- Any console in the 3DS family running boot9strap (yes, it is be useful to have boot9strap installed, we'll just remove it afterwards.)
- A few braincells

# 1. Required files

- The basic stuff that should go with your boot9strap installation (Luma, Godmode9)
- Soundhax audio file (or any other entrypoint) -> http://soundhax.com
- The otherapp.bin -> https://smealum.github.io/3ds/#otherapp
- Your otp.bin, should be on /boot9strap/ if you dumped it, if you do not know how to dump it, get out, you're not supposed to be here
- Luma v6.6 -> https://github.com/LumaTeam/Luma3DS/releases/download/v6.6/Luma3DSv6.6.7z
- SafeA9LH Installer -> https://github.com/AuroraWright/SafeA9LHInstaller/releases/tag/v2.6.7
- Arm9LoaderHax -> https://github.com/AuroraWright/arm9loaderhax/releases
- udsploit -> https://github.com/smealum/udsploit/releases/tag/1.0
- safehax -> https://github.com/TiniVi/safehax/releases/tag/r27
- data_input_v4.zip (I can't provide a link here, please search for it yourself)

# 2. If you're running a recent 3DS firmware versions


You'll need to downgrade your 3DS.
BACKUP EVERYTHING!
Get firmwares files for your 3ds. The region should match and the model too. It should be a updates folder with a bunch of cia files. THIS SHOULD NOT BE A CTRTRANSFER IMAGE
Put the updates folder on the root
Install SysUpdater (please use the cia) https://github.com/profi200/sysUpdater/releases/tag/0.4.3b
Once install, run the app and hit Y to downgrade
Wait a few minutes for the downgrade process to complete.
Now reboot your console, if it boots, then it should have worked.

I personally didn't use that method. If I said something wrong, I'm sorry. Here's what I did instead (

- Go to GodMode9
- Press HOME button Go to More -> System Info
- If the original system version is below 9.0.0 or past 11.3 , you won't be able to use soundhax, and installing A9LH might not be possible. (or try to downgrade to a compatible version anyways, maybe it'll work, I might test by myself when I'll have time)
- If your version is correct, download the firmware files for that exact version. Should be an 'updates' folder Make sure region and the model of your 3DS match.
- Put this updates folder at the root of your SD card.
- Boot into GodMode9
- Go to Title Manager -> NAND / TWL Titles
- Press L+Right to select everything, press A, select Manage Title -> Uninstall -> Uninstall Everthing. Do the key combo and wait. It's better if you dont relock permissions yet, as we still need them.
- Then once done, go to sd/updates, Press L+Right to select everything, go to CIA options -> Install titles. There might be one title that doesn't install in the end, it's okay.
- Reboot and check if it worked.

# 3. Removing Boot9strap

To make sure the A9LH install goes smoothly, we might want to remove boot9strap.

First make sure you don't have a custom keyboard or made a region change. Because removing cfw will brick your console if it's not the case.
Now, let's uninstall b9s!

- Boot Into GodMode9
- Press the HOME Button, go to Scripts -> GM9Megascript -> Hax Options -> Uninstall CFW
- Confirm everything and do the key combo. You should now have cfw uninstalled. Now reboot, you should boot into stock firmware.

# 4. Getting to install A9LH

Now, place the required files on your SD Card this way:

- Put the otherapp file in root (of course renaming it first)
- Put the soundhax file in root
- Put the boot.3dsx file in root
- UDSPloit goes in the 3ds folder
- Safehax goes in the 3ds folder
- From the SafeA9LHInstaller zip, take the arm9loaderhax.bin file and put it in root
- Put the contents of the release.7z file in the a9lh folder
- Put your OTP.bin file in the a9lh folder
- Merge the a9lh folder from data_input_v4.zip with the one on your SD card.

Now, put the SD Card back in your 3DS and boot.
Go to Soundhax (or whatever method you're using)
On the HBL, launch udsploit. Press Start to quit
Then, run safehax, you should get on the SafeA9LHInstaller
Press Select to Install A9LH.
Once finished, click any button to shutdown and put your SD Card back in your computer.

# 5. Installing Luma

From the Luma v6.6 zip, replace the arm9loaderhax.bin on the root of your SD card by the one in the zip file.
Now try to boot with your SD Card, you should get on Luma Config.
You might want to check Autoboot on SysNAND if you don't have an EmuNAND.

Congrats! You now have installed A9LH on your system with Luma!
