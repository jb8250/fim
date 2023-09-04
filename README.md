<h1>File Integrity Monitor</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
This PowerShell script is designed to provide basic file monitoring and integrity checking capabilities. It offers the following functionalities:

Calculate File Hash: It defines a function Calculate-File-Hash($filepath) to calculate the SHA-512 hash of a given file path.

Erase Baseline If Already Exists: Another function, Erase-Baseline-If-Already-Exists(), checks for the existence of a file named "baseline.txt" and deletes it if it's present, ensuring a fresh baseline can be created.

User Interaction:

The script prompts the user to choose between two options:

'A': To collect a new baseline for monitoring.

'B': To begin monitoring files using a previously saved baseline.

Option A - Collect New Baseline:

If the user selects 'A':
The script checks if "baseline.txt" exists and deletes it if found.
It calculates the SHA-512 hash for each file in a folder named "Files."
The calculated file hashes, along with their file paths, are stored in "baseline.txt" as a baseline for future comparisons.

Option B - Begin Monitoring Files with Saved Baseline:

If the user selects 'B':
The script loads file paths and corresponding hashes from "baseline.txt" into a dictionary.
It enters a continuous loop to monitor files.
For each file in the "Files" folder:
It calculates the current hash.
It compares the current hash with the stored baseline hash.
If a new file is detected, it notifies the user that a new file has been created.
If a file's hash differs from the baseline, it notifies the user that the file has been changed (potentially indicating tampering).
It checks if any files from the baseline have been deleted and notifies the user if a baseline file is missing.

In summary, this script serves as a basic file monitoring and integrity verification tool. Users can either establish a new baseline of file hashes or monitor files based on an existing baseline. It continuously checks for changes in files and provides notifications when discrepancies or unauthorized changes are detected, making it useful for basic file integrity and security monitoring purposes.
<br />




<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
