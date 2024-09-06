## What's it to do?
- Bring back **"Internet Explorer"** for latest version of Windows 10 and Windows 11. It means you can use the **"Internet Explorer"** as a standalone browser like before, no annoying **"Microsoft Edge"** startup again.
- Restore the castrated **"Internet Options"** in the **"Control Panel"**.
- Provide a registry file to completely remove **"IEToEdge BHO"** *(It actually no needed, but if you want)*.

## How to use it?
- Open the corresponding directory based on the version of Windows you are using *(Win10 or Win11)*.
- Copy the `"ieframe.dll"` and `"inetcpl.cpl"` to the corresponding directory ***(Prefix with "C:\Windows\")*** and replace the original files.
- **Don't forget make a backup** for `"ieframe.dll"` and `"inetcpl.cpl"`, just in case!

#### Something you need to know:
You may encounter permission issues that prevent you from replacing original files, this because system files can only be modified by "TrustedInstaller" account. You need change the owner of the `"ieframe.dll"` and `"inetcpl.cpl"` to lift this restriction.

Reference: [How to take ownership and get full access to files and folders in Windows 10](https://winaero.com/how-to-take-ownership-and-get-full-access-to-files-and-folders-in-windows-10/)

After each Windows Update, these modifications may no longer work, you need to repeat the above steps.

## How it works?
Since the Windows build 10.0.1904x.3570 or even earlier, Microsoft has blocked the previous methods to enable "Internet Explorer", such like edit the registry or create a vbs shortcut.

Not only that, they also hardcoded the logic to jump to "Microsoft Edge" into "ieframe.dll" and deleted many options in "Control Panel".

So I backed up an earlier version of "ieframe.dll" and "inetcpl.cpl" then replace, it works prefectly.
