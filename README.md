## Eas Notes
If the orignal repo dissapear, the `https://massgrave.dev/get` content is the following:

```
# Enable TLSv1.2 for compatibility with older clients
[System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor [System.Net.SecurityProtocolType]::Tls12

$DownloadURL = 'https://raw.githubusercontent.com/massgravel/Microsoft-Activation-Scripts/master/MAS/All-In-One-Version/MAS_AIO.cmd'

$FilePath = "$env:TEMP\MAS.cmd"

try {
    Invoke-WebRequest -Uri $DownloadURL -UseBasicParsing -OutFile $FilePath
} catch {
    Write-Error $_
	Return
}

if (Test-Path $FilePath) {
    Start-Process $FilePath -Wait
    $item = Get-Item -LiteralPath $FilePath
    $item.Delete()
}
```
Entering manually to that url, it turns to `https://massgrave.dev/get.ps1`
I think that I should change the URL to another URL that point to the `.cmd` file or use the Method 2 - Traditional


## Microsoft Activation Scripts (MAS):

A Windows and Office activator using HWID / KMS38 / Online KMS activation methods, with a focus on open-source code and fewer antivirus detections.

## Download / How to use it?

### Method 1 - PowerShell

-   On Windows 10/11, right-click on the windows start menu and select PowerShell or Terminal.
-   Copy-paste the below code and press enter\
    `irm https://massgrave.dev/get | iex`
-   You will see the activation options, and follow onscreen instructions.
-   That's all.

### Method 2 - Traditional

-   Download the file named `MAS_1.6_Password_1234.7z` from [here](https://github.com/massgravel/Microsoft-Activation-Scripts/releases)
-   Extract this file with a 3rd party archive manager, such as [7zip](https://www.7-zip.org/download.html)
-   Password is `1234`
-   In the extracted folder, find the folder named `All-In-One-Version`
-   Run the file named `MAS_AIO.cmd`
-   You will see the activation options, and follow onscreen instructions.
-   That's all.


```
Latest Version: 1.6
Release date: 25-July-2022
```

### For more details, check Homepage:  https://massgrave.dev/

### [Download Original Windows & Office](https://massgrave.dev/genuine-installation-media.html)

   <a href="https://discord.gg/gjJEfq7ux8">
  <img src="https://discordapp.com/api/guilds/746721520931569757/widget.png?style=banner3" />
</a>


---

Made with Love ❤️


