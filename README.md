# CloudCore-Standards
Coding standards for CloudCoin software.

### Folder Structure

Here is the list of directories to be used when handling CloudCoin files:

- Bank
- Counterfeit
- Export
- Fracked
- Import
- Imported
- Logs
- Suspect
- Templates
- Trash

Each folder has a specific use, and should not be used in any other way than instructed here. These standards must be upheld to ensure proper file management. Here is the lifecycle of a CloudCoin moving through the CloudCore:

**Import**: The Import folder is where the CloudCore system will find new CloudCoins. These files will be read by CloudCore, separated into individual files, and then moved to the *Suspect* folder and copied to the *Imported* folder.

**Imported**: The Imported folder holds copies of CloudCoins before they are separated or authenticated. The CloudCoins in this folder will not be used.

**Suspect**: The Suspect folder holds CloudCoins which will be authenticated by RAIDA nodes, then be moved to the *Detected* folder.

**Detected**: The Detected folder holds CloudCoins which will be sorted into new folders based on their authentication results: *Bank*, *Fracked*, *Counterfeit*, or *Lost*.

**Bank**: The Bank folder holds authentic CloudCoins which are validated with all RAIDA nodes.

**Fracked**: The Fracked folder holds authentic CloudCoins which are invalidated with some RAIDA nodes. The CloudCore can attempt to fix these coins, which would then be moved to the *Bank* folder.

**Counterfeit**: The Counterfeit folder holds CloudCoins which are either fake notes, or fracked beyond repair.

**Lost**: The Lost folder holds CloudCoins which do not have enough RAIDA responses and cannot be repaired.

**Templates**: The Templates folder holds images that will be used when exporting CloudCoins as jpeg files.

**Trash**: The Trash folder holds CloudCoins with unsupported file extensions or invalid data. The CloudCoins in this folder will not be used.

**Logs**: The Logs folder holds text records of all activity in the CloudCore.
