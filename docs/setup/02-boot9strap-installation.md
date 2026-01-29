# Step 02 - MSET9 Installation

## Goal
Use the MSET9 script, used to trigger MSET9. While the script is in progress, user data will temporarily be disabled and will return by the end of the directions on this page.
If you get an error on the script, check /docs/troubleshooting

---

## What I used
- SD Card: FAT32 (prepped in step 01)
- Console Model: 3DS XL (Smash Bros. Edition)
- Console version 11.17.0
- Python
- boot9strap (MSET9) https://github.com/hacks-guide/MSET9/releases/tag/v2.1

---

## Section I - Instructions
# Prepare MSET9 exploit bv temporarily creating a new HOME Menu profile with almost no user data, then setting that profile up with only the minimum requirements to trigger MSET9. Existing data will dissapear but will come back after completion.

1. Insert SD Card to computer
2. Unzip everything from the MSET9 .zip, to the root of the SD card - if any files exist, overwrite them.
3. Run the MSET9 script (open MSET9-macOS.command)
4. **DIFFERS PER CONSOLE MODEL AND VERSION** Enter "1" for 3DS XL (11.17.0) (Super Smash Bros. Edition)
5. Once the window changes, enter "1", to create a MSET ID1, view disclaimer, enter "1" again (if you get an error, check /docs/troubleshooting
6. If you see the message, "Created hacked ID1", Enter or enter "0" to exit.
8. Re-Insert the SD card into the device (most data will be removed, thats normal for now)
9. Open Mii Maker, wait for console to reach "Welcome Mii Maker" screen, then exit and return to Home Menu
10. Launch System Settings, navigate to Data Management > Nintendo 3DS > Software > Reset (this will not wipe your data)
11. Power off device, insert SD back into computer
12. Run the MSET9 script
13. Type the number corresponding to your model/version, for me "1"
14. Next display should show Current MSET9 state: Ready, if Not Ready then, check the MSET9 status for more details
15. Enter 0 to close the script, eject the SD, and insert back into console

## Section II - MSET9
# In this next section, you will trigger MSET9 to launch SafeB9SInstaller (the custom firmware installer)
# These instructions must be followed **EXACTLY** so double check everything and avoid errors and a bricked device

1. Power your console back on, ensuring the first app selected is System Settings. If you turn on your device and you are hovering over another application, move to System Settings, then turn your device off and back on.
2. Press (A) to launch System Settings
3. Navigate to Data Management > Nintendo 3DS > Extra Data
4. DO NOT PRESS ANY BUTTONS OR TOUCH THE SCREEN
5. With the console STILL ON, and WITHOUT PRESSING ANY BUTTONS OR TOUCHING THE SCREEN, remove your SD card from the console.
6. The menu should refresh and state that there is no SD card inserted
7. Insert SD to computer
8. Run the MSET9 script
9. Type the number corresponding to model/version, for me "1"
10. Type and enter "3", to inject MSET9, you should see "MSET9 successfully injected"
11. Press enter to close the MSET9 script
12. Reinsert SD card into console WITHOUT PRESSING ANY BUTTONS OR TOUCHING THE SCREEN.
13. If the exploit was succesful you will have booted into the SafeB9Installer, if you get a red screen or loading for more than 10 seconds, check this troubleshooting guide: https://3ds.hacks.guide/troubleshooting-mset9.html

## Section III - Boot9strap
# In this section you will install custom firmware onto your console

1. When prompted input the key combo given on the top screen to install boot9strap
- If you are not prompted, or a step is in colored-red-text, check the troubleshooting guide
- If the top screen is blank and you see "Crypto Status - All checks passed" on the bottom screen - you will have to enter this key combo blindly
- D-Pad Left, D-Pad Down, D-Pad Right, D-Pad Up, A
2. Once complete, all seven steps are in green-colored-text, hit A to reboot the console.
3. The console should boot back up into the Luma3DS configuration menu
  - Luma3DS configuration menu are settings for the Luma3DS custom firmware - many of these settings may be used for customization or debugging.
  - For the purporse of the guide, leave these default for now
  - If the console displays a white notification LED and shuts down, ensure Luma3DS boot.firm is on the root SD card
4. Press Start to Save and reboot

## Section IV - Removing MSET9
# In this section, you will remove MSET9 to prevent further issues and to restore your user data (games, themes, etc.)
# ** DO NOT SKIP THIS, applications may crash and you may experience more errors later in the process

1. Power off console, insert SD back into computer
2. Run the MSET9 script
3. Type the number corresponding to your model/version
- Current state should display "Injected"
- If you did not inject, or have already removed it, the status will read "Ready"
4. Type and enter "4" to remove the trigger file
- You should see "Removed trigger file"
5. Type and enter "5" to remove MSET9
- You should see "Successfully removed MSET9"
6. Press Enter to close the script
7. Upon insertind SD back to console, you should boot to Luma3DS by default
- It looks no different from the original 3DS Menu

# Next, we install homebrew applications
