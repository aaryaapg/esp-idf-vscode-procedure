# esp-idf-vscode-procedure
Procedure and resources for getting started with ESP-IDF on VSCode.
## Procedure
### Step 1: Install ESP-IDF
https://www.youtube.com/watch?v=K58Y2dFsQ2A -> Follow the same procedure
### Step 2: Install VSCode
https://www.youtube.com/watch?v=aQi8qiW9fmg&list=PLfcVdODhZSagC8s_13x22eAf0X9TP4zqy&index=9 -> 00:00 to 01:52
1. Set Environment Variables
2. Enable C/C++ Extension on VSCode
3. Enable Native Debug exension on VSCode
### Step 3: Check versions of OpenOCD and Python
https://www.youtube.com/watch?v=KRyvly_SYS8 -> 05:33 to 06:12 
PS: I did not do all the extra stuff he was doing for python packages. Also, I had the latest version of python installed and not 2 versions like he had later in the video. 
### Step 4: Open example project and resolve errors
https://www.youtube.com/watch?v=KRyvly_SYS8 -> 10:18 to 14:34

Errors are:
1. Include Errors
2. portTICK_PERIOD_MS underline 

**How to resolve them?**

Press F1, then select C/C++ Edit configurations (UI). 

_Include Path_ :

`${workspaceFolder}/**`

`${env:IDF_PATH}/components/**`

`build/config`

[https://github.com/espressif/vscode-esp-idf-extension/issues/26]

_Compiler path_

`C:\esp\.espressif\tools\xtensa-esp32-elf\esp-2020r3-8.4.0\xtensa-esp32-elf\bin\xtensa-esp32-elf-gcc.exe`
[https://github.com/espressif/vscode-esp-idf-extension/issues/27]

_IntelliSense mode_ : Choose `gcc-x64(legacy)`

## On ESP-IDF 4.2 CMD (Example) 
`C:\esp>cd C:\esp\hello_world`

`C:\esp\hello_world>idf.py set-target esp32`

`C:\esp\hello_world>idf.py menuconfig`

`C:\esp\hello_world>idf.py build`

`C:\esp\hello_world>idf.py -p COM3 flash`

`C:\esp\hello_world>idf.py monitor`


