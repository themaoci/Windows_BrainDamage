[Go To Main](https://github.com/themaoci/Windows_BrainDamage/blob/main/README.md)

If you didnt checked the option while installing VSCode the code below will help you enable that option without reinstalling vscode
  
Steps:
So you are able to create your own folder actions at the Windows Registry:
- Press ⊞ Win + R and type regedit.
- Navigate to the path HKEY_CLASSES_ROOT\Directory\shell.
- Right click and create a new Key named vscode.
- At the (Default) REG_SZ, put the desired text, like Open with Code.
- Optionally, create an Icon key pointing to the Code.exe path (most likely "C:\Users\%UserName%\AppData\Local\Programs\Microsoft VS Code\Code.exe").
  
  
.reg file edit
```
Windows Registry Editor Version 5.00

[HKEY_CLASSES_ROOT\Directory\shell\VSCode]
@="Open with Code"
"Icon"="\"%LocalAppData%\\Programs\\Microsoft VS Code\\Code.exe\""

[HKEY_CLASSES_ROOT\Directory\shell\VSCode\command]
@=hex(2):22,00,25,00,4c,00,6f,00,63,00,61,00,6c,00,41,00,70,00,70,00,44,00,61,\
  00,74,00,61,00,25,00,5c,00,50,00,72,00,6f,00,67,00,72,00,61,00,6d,00,73,00,\
  5c,00,4d,00,69,00,63,00,72,00,6f,00,73,00,6f,00,66,00,74,00,20,00,56,00,53,\
  00,20,00,43,00,6f,00,64,00,65,00,5c,00,43,00,6f,00,64,00,65,00,2e,00,65,00,\
  78,00,65,00,22,00,20,00,22,00,25,00,56,00,22,00,00,00
```
