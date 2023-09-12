# PowerShell File Integrity Monitor

## Overview

This PowerShell script is designed to monitor file integrity within a specified folder. The script initially establishes a baseline of the current files and their SHA512 hashes. Subsequently, it continuously monitors changes to files and alerts the user when:

- A new file is created
- An existing file is modified
- An existing file is deleted

## Languages, Utilities, and Environment Used

- **Languages**: PowerShell
- **Utilities**: SHA512 Hashing, File I/O Operations
- **Environment**: Windows with PowerShell 5.1 or later

## Program Walkthrough

### Functions

1. `Calculate-File-Hash($filepath)`: Calculates the SHA512 hash of the specified file.
2. `Erase-Baseline-If-Already-Exists()`: Checks if a baseline file exists and removes it.

### Steps

1. The user is prompted to either collect a new baseline or begin monitoring based on an existing baseline.
2. If the user chooses to collect a new baseline:
    - Any existing baseline file is deleted.
    - A new baseline file is created, consisting of file paths and their corresponding SHA512 hashes.
3. If the user chooses to begin monitoring:
    - The existing baseline is loaded into a dictionary.
    - The script enters into a continuous monitoring phase where changes to the files are checked every second.

## How to Run the Script

1. Clone the repository or download the script to your machine.
2. Open PowerShell as an administrator.
3. Navigate to the script's directory.
4. Run the script using `.\YourScriptName.ps1`.
5. Follow the prompts to either create a new baseline or to begin monitoring.

## Contributions

Feel free to contribute to this project by opening a Pull Request.

