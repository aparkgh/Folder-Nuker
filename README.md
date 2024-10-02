# Folder Nuker
**Folder Nuker** is a simple and fast folder generator, written in Windows Batch, that creates empty folders very quickly.

## Directions of use
* Place `Folder Nuker.bat` in the directory where you want to create folders and run the file.
* Press any key as prompted to begin folder creation.
* Close the Command Prompt window to stop the process once you're done.

**Warning:** This script generates folders very quickly and will continue to do so until the Command Prompt window is manually closed. Be cautious and ensure it's run in the correct directory to avoid unintended folder creation.

## How it works
An infinite loop continuously executes the folder creation command until the program is terminated.

An attempt to create a folder with a specific name in a directory that already contains a folder with that name will fail. To minimize the risk of this happening, multiple instances of %random%[^1] were utilised, increasing the general folder name length and reducing the likelihood of a duplicate folder generation attempt- resultantly exponentially increasing the total number of possible folders that can be generated.

## What is a Windows Batch Executable?
A Windows Batch Executable (`.bat`) is a script that automates tasks by executing commands in sequence through the Windows Command Prompt (`cmd.exe`). In this case, Folder Nuker uses batch commands to rapidly create empty directories.

[^1]: %random% is an environment variable which generates a number between 0 and 2<sup>15</sup>-1, the maximum value for a signed 16-bit integer.
