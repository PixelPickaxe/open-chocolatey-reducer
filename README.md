# open-chocolatey-reducer
Open Chocolatey Reducer is a script that mimics the official [Chocolatey Package Reducer](https://docs.chocolatey.org/en-us/features/package-reducer#mainContent) available in the [Pro and Business versions](https://chocolatey.org/pricing#pricing-faq) of [Chocolatey](https://chocolatey.org).

# How it works
The __official__ Chocolatey Package Reducer scans the "%APPDATA%\chocolatey\" directory recursively for any 7z, zip, rar, gz, tar, sfx, iso, msi, msu, msp, and exe files.
If it locates any, it deletes them. This is an effective way to remove unwanted installation files, but it's unfortunately locked behind a paywall. I highly encourage you to support Chocolatey if you feel so inclined. Additionally, it also reduces the file size of nupkg files, but this is something I was not able to accomplish with my limited knowledge.

Open Chocolatey Reducer mimics the Chocolatey Package Reducer by using Windows batch scripting to manually delete the listed file types at the log-on of any user, achieveing similar results as the Chocolatey Package Reducer.

## Requirements
* Working installation of Windows 7 / 8 / 8.1 / 10
* Working installation of Chocolatey
* Administrator access on your PC

### Installation

1. Extract "OCR_1.0.0.zip" into your Downloads folder. If you extract to a different directory, you'll have to edit the installation .bat file accordingly.

2. Open the "Installer" directory located within the "OCR_1.0.0" folder that you just extracted.

3. Open "(Step 1) Import Task into Task Scheduler"

4. Import the "Open Chocolatey Reducer.xml" into Task Scheduler.

A guide on how to import tasks can be found [here](https://www.windowscentral.com/how-export-and-import-scheduled-tasks-windows-10).

5. Return to the "Installer" directory.

6. Right-click "(Step 2) Installer" and click "Run as administrator" from the context menu.

7. Press any key to continue . . .

## Post-Installation
1. Navigate back to your Downloads folder and delete "OCR_1.0.0" and "OCR_1.0.0.zip"

2. Tell your friends about this script :D Spread the word!

### License
Boost Software License - Version 1.0 - see [LICENSE](https://github.com/PixelPickaxe/open-chocolatey-reducer/blob/main/LICENSE)
