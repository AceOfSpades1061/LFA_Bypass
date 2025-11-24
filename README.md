# SCPS_Bypass | Written by AceOfSpades1601

> [!IMPORTANT]
> THIS REPO IS FOR EDUCATIONAL PURPOSES AND TO EDUCATE ON CHROMEOS'S BAD SECURITY!!!

**Disclaimer**: _I did not make/find **ANY** of these exploits; all of these exploits belong to their respective owners._

**Another Disclaimer**: _I also do **NOT** condone using this to cheat on school tests or assignments. **Please do your work with honesty**._

**Final Disclaimer**: _I am not responsible if you get into trouble with your local sysadmin for doing this on a **enterprise-owned device**, and not your own._

## Table of Contents
- [Sh1ttyOOBE + BadSh1mmer - Unblock Dev mode and Unenrollment for Versions 135-137](https://github.com/AceOfSpades1061/SCPS_Bypass?tab=readme-ov-file#sh1ttyoobe--badsh1mmer---unenrollment-for-kv5--found-by-crosbreaker)
- [Kernel Version](https://github.com/AceOfSpades1061/SCPS_Bypass?tab=readme-ov-file#kernel-version)
- [Checking Version](https://github.com/AceOfSpades1061/SCPS_Bypass?tab=readme-ov-file#checking-version)
- [Avoiding Accidental Re-enrollment](https://github.com/AceOfSpades1061/SCPS_Bypass?tab=readme-ov-file#avoiding-accidental-re-enrollment)

## Sh1ttyOOBE + BadSh1mmer - Unenrollment for KV5 | Found by [Crosbreaker](https://github.com/crosbreaker)
Prerequisites:
- Chromebook with a Version from 135-137
- A USB (Recommended to have 8 GB or more)
- Reading capabilities of a 5th grader

> [!TIP]
> If you only need unenrollment that can be simply undone and re-enrolled, and don't want full control over your Chromebook, you can just stick with Sh1ttyOOBE.

### SH1TTYOOBE
1. Powerwash Your Chromebook (Ctrl+Shift+Alt+R on Login screen, NOT lock screen)
2. On the "Welcome to Your Chromebook" screen, wait until you see the Set up with Android button (DO NOT PRESS GET STARTED IF IT DOESN'T SHOW IMMEDIATELY), then press the button. (This should be inferred; apparently, some people are too stupid for this 🐳)
3. Press Ctrl+Shift+Alt+R and click Cancel
4. Click "Enter your Google account email and password", and it should say to connect to a network
5. Open quick settings from the bottom right and connect to a network
After signing in, you can sign out, and you will be back on the welcome screen. Progress through Oobe as normal by clicking get started, and next, you will be greeted with three options to sign in. Sign in with the same email, and when you sign in, it will hang on the please wait screen. Simply restart or Alt+VolumeUp + X, and you will be placed on the lockscreen. After that, you are done and can sign out, and it will be persistent until the next powerwash.

> [!CAUTION]
> If it starts downloading an update and you already signed in but signed out back to Oobe, DO AN EC RESET IMMEDIATELY! (Refresh+Power)


### BADSH1MMER (Use after doing SH1ttyOOBE)
1. On the Chromebook you did Sh1ttyOOBE on or another computer, get the [Chromebook Recovery Utility](https://chromewebstore.google.com/detail/chromebook-recovery-utili/pocpnlppkickgojjlmhdmidojbmbodfm) from the web store.
2. Then, get a BadSh1mmer prebuilt from [this link](https://nightly.link/crosbreaker/badsh1mmer/actions/runs/17752578576).
3. Extract the Zip file and go to the Recovery Utility, click the three dots in the top corner, and select Use a Local image.
4. Select the BadSh1mmer bin file you extracted and let it write the bin to the USB.
5. Once it's done, go to your Chromebook and enable Developer Mode by pressing Esc+Refresh+Power and then pressing Ctrl+D and enter once you're on the Recovery Screen.
6. Due to Dev Mode being blocked in FWMP, it will make a _LOUD_ beep and complain that Dev Mode is blocked.
7. Ignore it (since it's not blocked in VPD) and go into recovery again (Esc+Refresh+Power)
8. Insert the USB you put BadSh1mmer on, and select BadBr0ker. Follow the instructions on the screen to fully unenroll and get Dev Mode unblocked.

With Dev Mode on, you can ALWAYS be unenrolled, no matter what version.

However, you must do these commands to avoid accidental re-enrollment. (Go to Avoiding Accidental Re-enrollment)

## Kernel Version
The anti-downgrader Google implemented to stop you from downgrading to vulnerable ChromeOS Versions.
### Versions you can downgrade to with your Kernver:
- Kernver 0: Any
- Kernver 1: Any
- Kernver 2: v111
- Kernver 3: v120
- Kernver 4: v125
- Kernver 5: v132
- Kernver 6: v138
- Kernner 7: v143 (I'm pretty sure this is the version that locks you on KV7, make a Pull req if this is wrong.)

## Checking Version:
Press Ctrl+Shift+Esc and look at the top for your codename, and it should display your major version to the right of your codename (example: yavilla, version 140.16371.0). <img src="https://raw.githubusercontent.com/AceOfSpades1061/SCPS_Bypass/refs/heads/main/images/slightlystupid.png" alt="people who still ask me how to check their version" width="100">

## Avoiding Accidental Re-enrollment
You MUST have Access to the VT-2 Terminal with Dev Mode enabled to execute these commands.
