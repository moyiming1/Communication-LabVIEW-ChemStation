# Communication-LabVIEW-ChemStation
A DDE protocol for communication between LabVIEW and Agilent ChemStation

## Required packages (tested)
1. LabVIEW
2. Agilent ChemStation Rev. C.01.07[27]
3. Windows 10 OS (DDE is only available in Windows)

## How to use it:
### Some comments about DDE mechanism
#### ChemStation is a DDE server itself, no need to setup anything. It is automatically a server.

Type “print _DDENAME$” in ChemStation command line to obtain the DDE Application Name. This name is different every time after restarting the ChemStation

Typically, the name is "hpcorexxxx"

#### ChemStation will only update the method parameters after reloading the method. 
To reload the method: "LoadMethod "_MethodPath$", "_MethodName$""

Example: "LoadMethod "C:\Chem32(2)\1\Methods\", "YM_AC_AUTOMATION.M""


