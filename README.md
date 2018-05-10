# Win_ZIP_password

## Description:
In Windows 10 Microsoft released new functions for encrypted zip files to make it more user friendly, I suppose. When you open one time encrypted ZIP file, Windows 10 saves the password in the memory. When you will try to open again this ZIP file, Windows 10 will take the path of the file, search in the memory the real path of last open ZIP files, and if he found ZIP-password couple then he will try to open the encrypted ZIP file. 

I saw that if you will try to hook SHUnicodeToAnsi function from ShLwApi.dll in ZIP opening time, then you can know the password of an encrypted ZIP file. 

The passwords stored in explorer.exe memory.

![](https://github.com/vah13/hooker_ZIP_password/blob/master/hook2.gif)
(https://raw.githubusercontent.com/vah13/Win_ZIP_password/master/hook2.gif)

## Windows 10 version
```
OS Name:                   Microsoft Windows 10 Pro
OS Version:                10.0.17134 N/A Build 17134
explorer.exe               10.0.17134.1
```

## TODO

Need to 
1. Get all ZIP files paths from explorer.exe and extract passwords
2. Analyze password storage (**because if you kill explorer.exe process and run it, the method works**)

## Useful for
CTF/Forensic
