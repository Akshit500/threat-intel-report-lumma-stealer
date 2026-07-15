## Overview

## Delivery / Initial Access

## Execution / Defense Evasion

## Credential Access

## Sources

## MITRE ATT&CK Technique

|    Technique ID    |     Name    |    Tactic     |
|--------------------|-------------|---------------|
| T1071	.001	| Application Layer Protocol: Web Protocols| Lumma Stealer has used HTTP and HTTP for command and control communication|
|T1119	|Automated Collection	|Lumma Stealer has automated collection of various information including cryptocurrency wallet details.|
|T1547	.001	|Boot or Logon Autostart Execution: Registry Run Keys / Startup Folder	|Lumma Stealer has created registry keys to maintain persistence using HKCU:\SOFTWARE\Microsoft\Windows\CurrentVersion\Run.|
|T1217	|Browser Information Discovery	|Lumma Stealer has identified and gathered information from two-factor authentication extensions for multiple browsers.|
|T1622	|Debugger Evasion	| Lumma Stealer has checked for debugger strings by invoking GetForegroundWindow and looks for strings containing "x32dbg", "x64dbg", "windbg", "ollydbg", "dnspy", "immunity debugger", "hyperdbg", "debug", "debugger", "cheat engine", "cheatengine" and "ida".|
|T1140	|Deobfuscate/Decode Files or Information	|Lumma Stealer has used Base64-encoded content during execution, decoded via PowerShell.|
|T1685	|Disable or Modify Tools	|Lumma Stealer has attempted to bypass Windows Antimalware Scan Interface (AMSI) by removing the string "AmsiScanBuffer" from the "clr.dll" module in memory to prevent it from being called.|
-----
Enterprise	T1573	.002	Encrypted Channel: Asymmetric Cryptography	
Lumma Stealer has used HTTPS for command and control purposes.[4]

Enterprise	T1041	Exfiltration Over C2 Channel	
Lumma Stealer has exfiltrated collected data over existing HTTP and HTTPS C2 channels.[3][4]

Enterprise	T1564	.003	Hide Artifacts: Hidden Window	
Lumma Stealer has utilized the .NET ProcessStartInfo class features to prevent the process from creating a visible window through setting the CreateNoWindow setting to "True," which allows the executed command or script to run without displaying a command prompt window.[4]

Enterprise	T1574	.001	Hijack Execution Flow: DLL	
Lumma Stealer has leveraged legitimate applications to then side-load malicious DLLs during execution.[1]

Enterprise	T1036	.008	Masquerading: Masquerade File Type	
Lumma Stealer has used payloads that resemble benign file extensions such as .mp3, .accdb, and .pub, though the files contained malicious JavaScript content.[2]

Enterprise	T1027	Obfuscated Files or Information	
Lumma Stealer has used SmartAssembly to obfuscate .NET payloads.[4]

.013	Encrypted/Encoded File	
Lumma Stealer has used AES-encrypted payloads contained within PowerShell scripts.[3]

Enterprise	T1566	.001	Phishing: Spearphishing Attachment	
Lumma Stealer has been delivered through phishing emails with malicious attachments.[1]

.002	Phishing: Spearphishing Link	
Lumma Stealer has been delivered through phishing emails containing malicious links.[1]

Enterprise	T1055	.012	Process Injection: Process Hollowing	
Lumma Stealer has used process hollowing leveraging a legitimate program such as "BitLockerToGo.exe" to inject a malicious payload.[3]

Enterprise	T1620	Reflective Code Loading	
Lumma Stealer has used reflective loading techniques to load content into memory during execution.[2][4]

Enterprise	T1113	Screen Capture	
Lumma Stealer has taken screenshots of victim machines.[1]

Enterprise	T1518	.001	Software Discovery: Security Software Discovery	
Lumma Stealer has detected antivirus processes using commands such as "tasklist" and "findstr."[3]

Enterprise	T1176	.001	Software Extensions: Browser Extensions	
Lumma Stealer has installed a malicious browser extension to target Google Chrome, Microsoft Edge, Opera and Brave browsers for the purpose of stealing data.[1]

Enterprise	T1539	Steal Web Session Cookie	
Lumma Stealer has harvested cookies from various browsers.[1][4][5]

Enterprise	T1553	.002	Subvert Trust Controls: Code Signing	
Lumma Stealer has used valid code signing digital certificates from ConsolHQ LTD and Verandah Green Limited to appear legitimate.[5]

Enterprise	T1195	Supply Chain Compromise	
Lumma Stealer has been delivered through cracked software downloads.[1][4][5]

Enterprise	T1218	.005	System Binary Proxy Execution: Mshta	
Lumma Stealer has used mshta.exe to execute additional content.[3][2]

.015	System Binary Proxy Execution: Electron Applications	
Lumma Stealer as leveraged Electron Applications to disable GPU sandboxing to avoid detection by security software.[5]

Enterprise	T1082	System Information Discovery	
Lumma Stealer has gathered various system information from victim machines.[1][4][5]

Enterprise	T1204	User Execution	
Lumma Stealer has been distributed through a fake CAPTCHA that presents instructions to the victim to open Windows Run window ("Windows Button + R") and paste clipboard contents ("CTRL + V") and press "Enter" to execute a Base64-encoded PowerShell.[3][1][2]

.002	Malicious File	
Lumma Stealer has gained initial execution through victims opening malicious executable files embedded in zip archives, and MSI files within RAR files.[1]

Enterprise	T1497	.001	Virtualization/Sandbox Evasion: System Checks	
Lumma Stealer has queried system resources on the victim device to identify if it is executing in a sandbox or virtualized environments, checking usernames, conducting WMI queries for system details, checking for files commonly found in virtualized environments, searching system services, and inspecting process names.[4] Lumma Stealer has checked system GPU configurations for sandbox detection
