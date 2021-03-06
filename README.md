# QtStatic
Script that builds Qt in Static version
---------------------------------------
## Prerequisites

**You need _Qt already installed_. <a href="https://www1.qt.io/download-open-source/" target="_blank">Download Qt here</a>**

Then you need :
 - PowerShell script. You can download it here: <a href="https://www.microsoft.com/en-us/download/details.aspx?id=34595" target="_blank">Microsoft PowerShell</a>
 - <a href="http://www.7-zip.org" target="_blank">7Zip</a>.
 - MinGW 5.3.0 (downloaded with <a href="https://www1.qt.io/download-open-source/" target="_blank">Qt online installer</a>)

---------------------------------------
## How to use ?
Open this script with an text editor and change these lines at your convenience:

- At line 79: Choose the Qt source URL (Example: **"https://download.qt.io/official_releases/qt/5.11/5.11.0/single/qt-everywhere-src-5.11.0.zip"**).<br/>
All versions of Qt are available here : **https://download.qt.io/official_releases/qt**.
- At line 80: Set path where Qt will be installed (Example: **"C:\Qt\Static"**).
- At line 81: Set the Qt folder name of the static version (Example: **"5.11.0"**, this is optional).
- At line 82: Set the directory of MinGW, by default path is **"C:\Qt\Tools\mingw530_32"**.
- At line 254 and 256: Set the path of "7z.exe" (Example: **"C:\7-Zip\7z.exe"**).

The archive file will be stored in **"src"** folder into your Qt path (Example: **"C:\Qt\Static\src\qt-everywhere-src-5.11.0.zip"**)

After that, launch the modified script by right-clicking the file and select **"Execute with PowerShell"**. **This process may take _several hours_**.

When Qt Static build is finished, open Qt Creator. Go to options and go to **"Build and run"**. Go to **"Qt Versions"** and click "add" button, go to the Qt Static path (Example: **"C:\Qt\Static\5.11.0\bin"**) and select **"qmake.exe"**.
Go to **"Kits"** section and add Qt Static Build the Qt Version.

Now you can build static apps!

For more informations, please visit <a href="https://wiki.qt.io/Building_a_static_Qt_for_Windows_using_MinGW" target="_blank">Build a Qt static</a>