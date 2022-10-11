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
