# pcm-converter-win10
pcm-converter exe for windows 10

# NOTE
Created this with PyInstaller

# INSTALL
## Download
- URL: https://github.com/ninksink/pcm-converter-win10/archive/refs/tags/PCMConverter-1.0.0.zip

## Open zip file
- Copy this file "eli_pcm_converter_gui3.exe" to whatever location you desire.
    - Desktop is fine.

# SCAN FOR VIRUS
This is just a good habit.  You can skip to the next step if you wish.
- Find the file in your Windows File Explorer
    - Right click and choose "Scan with Windows Defender"
    - You should see something like this
```
No current threats.
Last scan: m/d/yyyy h:mm (custom scan)
0 threats found.
Scan lasted 1 seconds
1 files scanned.
```
- If there is an issue that WindowsDefender finds then immediately quarantine the file and contact the author
via eellis@ninkware.com

# USAGE
## Run the "eli_pcm_converter_gui3.exe"
- YOU MIGHT run into "Windows protected your PC"
    - why?  Cuz I am not a licensed MS dev YET but relax, man.
        - and I am not in a mood to go through the mess of it until after my vacation.
    - You will see something like this:
```
Windows protected your PC
Microsoft Defender SmartScreen prevented an unrecognized app from starting. Running this app might put your PC at risk.
More info
```
    - Click the "More Info"
        - A new button will appear saying: "Run anyway"
            - Click that and tada...
                - A window will appear saying "Running from Command Line"
                - ANOTHER window with the User Interface (UI) will appear a short time later
                    - THIS IS the window you want to work in.

## WorkFlow
This is a gist of how you will use this SW.

### Special Notes for v1.0.0
- It is very fast with conversions.  Later versions will have a "progress bar"
- PCM files that are converted are placed in a sub-folder "converted_to_wav" of the PCM file's original location.

### The Workflow is this
NOTE: the original PCM files are ONLY READ, they are NEVER WRITTEN TO.
#### Converting selected files
- Click: "Select File(s)" button.
    - You can select multiple files if you desire using the *SHIFT-CLICK* method
        - Click the "Open" button in the file selector Dialog
        - There will be a pop up in the UI stating "You can click Convert button now."
            - click "Ok" to get past that.
            - THEN, click "Convert"
                - the screen will tell you everything that happened.
                - The output in the large white text area will state something like.
```
________________________________________________________________________________________________________________________
Conversion BEGIN: 2022-08-28 19:00:42.348871
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Count of Files Converted: 1
Converted Files are located: C:/Users/ninks/temp/eli-pcm-test-files/converted_to_wav
Converted Files report: C:/Users/ninks/temp/eli-pcm-test-files/converted_to_wav/convert_pcm_report.rpt
------------------------------------------------------------------------------------------------------------------------
Conversion DONE: 2022-08-28 19:00:42.398112
```
                - Notice the "Converted Files are located: " part.
                    - That is telling you where the newly created WAV files exist.
- Repeat above steps as wanted.

#### Converting a DIRECTORY of files
You will probably find this the most useful
- Click: "Select Directory" button.
    - A File/Dir selection window will popup
    - Click a folder name
        - Then click "Select Folder" button
            - There will be a pop up in the UI stating "You can click Convert button now."
                - click "Ok" to get past that.
                - THEN, click "Convert"
                    - the screen will tell you everything that happened.
                - The output in the large white text area will state something like.
```
________________________________________________________________________________________________________________________
Conversion BEGIN: 2022-08-28 19:05:24.060927
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Count of Files Converted: 1
Converted Files are located: C:/Users/ninks/temp/eli-pcm-test-files/dir-test/converted_to_wav
Converted Files report: C:/Users/ninks/temp/eli-pcm-test-files/dir-test/converted_to_wav/convert_pcm_report.rpt
------------------------------------------------------------------------------------------------------------------------
Conversion DONE: 2022-08-28 19:05:24.063923
```
                - All PCM files found in that dir will be used to generate WAV files in the `converted_to_wav` sub-folder
                    of the Folder you chose.
- Repeat above steps as wanted.

