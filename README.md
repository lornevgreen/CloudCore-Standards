# CloudCore-Standards
Coding standards for CloudCoin software.

### Folder Structure

Here is the list of directories to be used when handling CloudCoin files:

```
|-CloudCoin\
| |--  Accounts\
| | |-[##########]
      Bank\
      Commands\
        Backuper\
        DirectoryMonitor\
        Echoer\
        Eraser\
        Exporter\
        Minder\
        ShowCoins\
        Vaulter\     
      Counterfeit\
      Detected\
      Export\
        Email
        PayForward
        Sent
      Fracked\
      Gallery\
      Import\
        Waiting\
      Imported\
      Logs\
      Lost\
      Suspect\
      Templates\
      Trash\
      config.txt
      status.txt
```

Each folder has a specific use, and should not be used in any other way than instructed here. 
These standards must be upheld to ensure proper file management. Here is the lifecycle of a CloudCoin moving through the CloudCore:
Import: The Import folder is where the CloudCore system will find the new CloudCoins. 
These files will be converted into individual JSON files, and then moved to the Suspect folder and copied to the Imported folder.
Imported: The Imported folder holds copies of the CloudCoins before they are separated or authenticated. The CloudCoins in this folder will not be used.
Suspect: The Suspect folder holds the CloudCoins, which will be authenticated by RAIDA nodes, then be moved to the Detected folder.
Detected: The Detected folder holds the CloudCoins, which will be sorted into new folders based on their authentication results: Bank, Fracked, Counterfeit, or Lost.
Bank: The Bank folder holds the authentic CloudCoins, which are validated with all RAIDA nodes.
Fracked: The Fracked folder holds authentic CloudCoins, which are invalidated with some RAIDA nodes.
The CloudCore will attempt to fix these coins, which would then be moved to the Bank folder.
Counterfeit: The Counterfeit folder holds CloudCoins, which are either fake notes or fracked beyond repair.
Lost: The Lost folder holds CloudCoins, which do not have enough RAIDA responses and cannot be repaired.
Export: The Export folder holds files that contain any amount of CloudCoins in any supported file. These files will be converted into JSON files when imported back into a program.
Templates: The Templates folder holds images that will be used when exporting CloudCoins as jpeg files.
Trash: The Trash folder holds CloudCoins with unsupported file extensions or invalid data. The CloudCoins in this folder will not be used.
Logs: The Logs folder holds text records of all activity in the CloudCore.
### Deprecated Folders

These folders were in use in older programs, namely Founders 1.0:

```
Dangerous\
Partial\
Predetect\
Language\
```
