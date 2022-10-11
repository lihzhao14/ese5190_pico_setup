# PICO SETUP GUIDE FOR WINDOWS #
University of Pennsylvania, ESE 5190: Intro to Embedded Systems, Lab 2  

    Lihong Zhao  
        LinkedIn: www.linkedin.com/in/lihong-zhao-a24789224  
    Tested on: Lenovo Legion 5 Pro 16" Laptop, Windows11 

## Installing the Toolchain ##

* [Arm GNU Toolchain](#Installing_Arm_GNU_Toolchain)
* [CMake](#Installing_CMake)
* [Build Tools for Visual Studio 2022](#Installing_Build_Tools_for_Visual_Studio_2022)
* [Python 3.10](#Installing_Python_3.10)
* [Git](#Installing_Git)
 

#### [Installing_Arm_GNU_Toolchain](https://developer.arm.com/downloads/-/arm-gnu-toolchain-downloads) ####
* Finding the filename ending with -arm-none-eabi.exe to download
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/1.%20Arm%20GNU%20Toolchain/1.jpg" width="500">  
</div>

* During installation, tick the box (Add path to environment variable) to register the path to the Arm compiler as an environment variable in the Windows shell when prompted to do so.
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/1.%20Arm%20GNU%20Toolchain/2.jpg" width="450">  
</div>

#### [Installing_CMake](https://cmake.org/download/)  ####
* During the installation, add CMake to the system PATH for all users when prompted by the installer.
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/2.%20CMake/1.jpg" width="450">  
</div>

#### [Installing_Build_Tools_for_Visual_Studio_2022](https://visualstudio.microsoft.com/zh-hans/downloads/) ####
* When prompted by the Build Tools for Visual Studio installer, install the C++ build tools only.
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/3.%20Visual%20Studio%202022/1.jpg" width="450">  
</div>

#### [Installing_Python_3.10](https://www.python.org/downloads/release/python-3107/)  ####
* For windows system, install "Windows Installer".
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/4.%20Python%203.10/1.jpg" width="450">  
</div>

* During the installation, ensure that,
    * It’s installed 'for all users';
    * Add Python 3.10 to the system PATH when prompted by the installer. 
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/4.%20Python%203.10/2.jpg" width="450">  
</div>

* Additionally, disable the MAX_PATH length limit when prompted at the end of the Python installation. 
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/4.%20Python%203.10/3.jpg" width="450">  
</div>

* Then, python is successfully installed.
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/4.%20Python%203.10/4.jpg" width="450">  
</div>

#### [Installing_Git](https://git-scm.com/download/win)  ####
* When installing Git you should ensure that you change the default editor away from vim to Notepad as Git's default editor
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/5.%20Git/1.jpg" width="450">  
</div>

* Check the box "Checkout as is, commit as-is"
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/5.%20Git/2.jpg" width="450">  
</div>

* Select "Use Windows' default console window"
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/5.%20Git/3.jpg" width="450">  
</div>

* Select "Enable experimental support for pseudo consoles"
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/5.%20Git/4.jpg" width="450">  
</div>

## Getting the SDK and examples ##
* Open VS Code Terminal
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/6.%20Getting%20the%20SDK%20and%20examples/1.jpg" width="450">  
</div>

* Turn to initial address
```
    cd to "C:\Users\zlhgl\ese5190_lab2\pico\Downloads"
```
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/6.%20Getting%20the%20SDK%20and%20examples/2.jpg" width="550">  
</div>

 
```
C:\Users\zlhgl\ese5190_lab2\pico\Downloads> git clone -b master https://github.com/raspberrypi/pico-sdk.git
C:\Users\zlhgl\ese5190_lab2\pico\Downloads> cd pico-sdk
C:\Users\zlhgl\ese5190_lab2\pico\Downloads\pico-sdk> git submodule update --init
C:\Users\zlhgl\ese5190_lab2\pico\Downloads\pico-sdk> cd ..
C:\Users\zlhgl\ese5190_lab2\pico\Downloads> git clone -b master https://github.com/raspberrypi/pico-examples.git
```

## Building "Hello World" from Visual Studio Code ##
* Download and install [Visual Studio Code](https://code.visualstudio.com/) for Windows
* After installation open a Developer Command Prompt window in Visual Studio 2022
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/7.%20Building%20Hello%20World%20from%20VS%20Code/1.jpg" width="500">  
</div>

* Open VS Code from Developer Command Prompt and type,
```
code
```
VS Code will be popped up.

* Install the **CMake Tools** extension
    * Click on the Extensions icon in the left-hand toolbar (or type Ctrl + Shift + X), and search for **"CMake Tools"** and click on the entry in the list, and then click on the install button.
        * When installing, select "Trust Workspace & Install"

* Then select "Settings". In the Settings pane click on **"Extensions"** and then **"CMake Tools"**. Then scroll down to **"Cmake: Configure Environment"**. Click on **"Add Item"** and set the **PICO_SDK_PATH** to be **..\..\pico-sdk**
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/7.%20Building%20Hello%20World%20from%20VS%20Code/2.jpg" width="450">  
</div>

* Additionally scroll down to **"Cmake: Generator"** and enter **"NMake Makefiles"** into the box.
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/7.%20Building%20Hello%20World%20from%20VS%20Code/3.jpg" width="450">  
</div>

* Close the Settings page and go to the File menu and click on **"Open Folder"** and navigate to pico-examples repo and click **"Select Folder"**. 
* Select "GCC for arm-none-eabi" as the compiler
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/7.%20Building%20Hello%20World%20from%20VS%20Code/4.jpg" width="450">  
</div>

## Connect the RP2040 to the Laptop ##
* Reset the RP2040
    * Hold down the BOOT/BOOTSEL button (highlighted in red) and plug into the USB-port. 
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/8.%20RP2040/1.jpg" width="450">  
</div>

* Drag and drop **"hello_usb.uf2"** into the drive. (The path of "hello_usb.uf2" is "C:\Users\zlhgl\ese5190_lab2\pico\Downloads\pico-examples\build\hello_world\usb")
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/8.%20RP2040/2.png" width="450">  
</div>

## Result ##
<div align=center>
<img src="https://github.com/lihzhao14/ese5190_pico_setup_guide/blob/main/Image/Results/1.jpg" width="550">  
</div>


