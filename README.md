# Communication-LabVIEW-ChemStation
A DDE protocol for communication between LabVIEW and Agilent ChemStation

This is based on "Macro Programming Guide". Please refer to the original document for detailed explanations. 

## Required packages (tested)
1. LabVIEW
2. Agilent ChemStation Rev. C.01.07[27]
3. Windows 10 OS (DDE is only available in Windows)

## How to use it:
### ChemStation is a DDE server itself, no need to setup anything. It is automatically a server.

Type “print _DDENAME$” in ChemStation command line to obtain the DDE Application Name. This name is different every time after restarting the ChemStation

Typically, the name is "hpcorexxxx"

### ChemStation will only update the method parameters after reloading the method. 
To reload the method: "LoadMethod "_MethodPath$", "_MethodName$""

Example: 
The ChemStation method folder is: 
C:\Chem32\1\Methods\AUTOMATION.M

Then, the command for ChemStation is:
```LoadMethod "C:\Chem32\1\Methods\", "AUTOMATION.M"```

### Use "DDE send command.vi" in the repo as the driver
Refer to the "Macro Programming Guide" for additional commands.


