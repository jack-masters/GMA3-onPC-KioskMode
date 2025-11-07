# GMA3-onPC-KioskMode
Turn the grandMA3 onPC Software into a Fullscreen kiosk mode for inbuilt systems (WINDOWS ONLY)

# - How To - 

1) Install Latest [GMA3 onPC software](https://www.malighting.com/downloads/products/grandma3/)

2) Open Powershell as Administrator

3) cd Into the Microsoft.NET Framework64 folder `cd C:\Windows\Microsoft.NET\Framework64\v4.0.30319`
>  **v4.0.30319 is the virsion number and may have to be edited.**

4) Run the installer `.\InstallUtil.exe "C:\Program Files\MALightingTechnology\gma3_**[Your Version]**\bin\ma_shell_launcher_service.exe"`
> PLEASE replace the **[Your Version]** part with the version of grandMA3 you have insalled, you can check in File Explorer (The name of the folder)

5) Once Completed, open the registry editor - Search for **Regedit** in windows search

6) On the side bar navigate to: **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon**

7) Modify the **Shell** value and edit the value data to be: eshell.exe (This is the exe for the MA Shell)
   > Shells default value is: `explorer.exe`

8) In the same **Winlogon** key from Step 7 find the string value named **Userinit**
   > Userinits default value is: `C:\Windows\system32\userinit.exe,`

9) Edit the **Userinit** value to include the same shell launcher path from Step 4
    > The value at the end should look somthing like this: `C:\Windows\system32\userinit.exe,C:\Program Files\MALightingTechnology\gma3_**[Your Version]**\bin\ma_shell_launcher.exe`
  
10) Reboot your system and see it boot into the MA Launcher!

# - Auto Logon To An Account -

1) Download the latest AutoLogon script from Microsoft [here](https://learn.microsoft.com/en-us/sysinternals/downloads/autologon)
   > Select the **Run now from Sysinternals Live** and then you can skip extracting the zip file.

3) Extract the zip file if downloading the zip over Run Now (As stated above).

4) Run `AutoLogon.exe` as an Administrator

5) Enter the Username and Password of the account you want it to autoLogin to and click **Enable**

6) Reboot again and your PC will auto login to the user account you set and boot you into MA!
