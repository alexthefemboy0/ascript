# Rocket
A simple, lightweight interpreted programming language.<br>
# Requirements<br>
NOTE (for Windows users only): Rocket is not officially supported on Windows. Any Windows-specific guides like installing Lua for Windows or modifying your environment PATH variable will not be listed here, as they can be found with a quick online search. If something on Rocket does not work with Windows but works on Unix-like OSes, (MacOS, Linux, etc.) **Do not make an issue about it.** The only Windows-specific guide that will be provided here is the basic install guide.<br><br>
Lua - You need to have Lua installed on your system as the interpreter is written in Lua.<br>
Make - Make is a build system. All Unix-like OSes should have this installed by default.<br><br>
# Installing Rocket<br>
To install Rocket, first download the source code from the releases page,<br>
Once it's downloaded, extract the compressed folder.<br>
Navigate to the extracted folder and run `make` in the terminal to install it. (Requires sudo permissions) **NOTE: On MacOS, make sure you change `/usr/bin` to `/usr/local/bin` in the Makefile.**<br>
Run `rocket` or `rocket <file>` to enter the Rocket command line or open a Rocket file.<br><br>
# Running a file<br>
The preferred file extension for Rocket files is .rocket, however any extension you fancy will work.<br>
To open a Rocket file, type `rocket <rocket file>`<br>
To open the Rocket command line, type `rocket`<br><br>
# Manual Compilation for Windows Users<br>
If you do not want to install MSYS2 or another tool to get Make onto your system but still want to use Rocket, follow the steps below.<br><br>

1. Extract the compressed folder where the Rocket source code is located.<br>
2. Create a directory in `%localappdata%` named `rocket`<br>
3. Open the command line and navigate to the folder where Rocket is located<br>
4. Run the following command in Command Prompt as administrator: `luac -o %localappdata%\rocket rocket.lua` If you get an error that `luac` cannot be found, add it <br>
5. Create a new file in `%localappdata\rocket` titled `rocket.bat`<br>
6. Put the following contents into the file:<br>
```batch
@echo off
lua rocket.out
```
7. Save and close the file.<br>
8. Add the `%localappdata%\rocket` folder to your environment PATH variable.<br>
9. Run `rocket.bat` or `rocket.bat <file>` to enter the Rocket command line or open a Rocket file.