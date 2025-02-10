# Contourlet Transform Toolbox for MATLAB

This repository provides a working version of the Contourlet Transform Toolbox for MATLAB. It includes solutions and fixes to common issues encountered during setup and usage. The provided steps aim to help anyone smoothly use the toolbox without spending hours troubleshooting.

## Quick Start Guide

### Step 1: Clone the Repository
Download or clone the repository to your local machine:
- **Clone:**
  ```bash
  git clone https://github.com/aliibraheemshash/Contourlet-transform.git
  ```
- **Download:** Click the green "Code" button and select "Download ZIP." Extract the files if needed.

### Step 2: Add Toolbox to MATLAB Path
1. Open MATLAB.
2. Add the toolbox folder to the MATLAB path using this command:
   ```matlab
   addpath(genpath('path-to-your-folder\contourlet-transform-master'));
   ```
   Replace `path-to-your-folder` with the actual path where you downloaded or extracted the files.

### Step 3: Save the Path
Run the following command to permanently save the path:
```matlab
savepath;
```

### Step 4: Set MATLAB Active Directory
Move the active directory to the toolbox folder:
1. Create a new `.m` script in the toolbox folder using MATLAB.
2. Run any simple command in the script.
3. When MATLAB asks whether to change the active folder, click **Accept.**

> **Tip:** This "trick" helps MATLAB correctly find all functions and files within the toolbox.

### Step 5: Check for C Compiler
Ensure you have a compatible C compiler installed. Run the following command:
```matlab
mex -setup C
```
If no compiler is installed, MATLAB will prompt you to download and configure one. Visual Studio is a recommended option for Windows users.

### Step 6: Compile the Required C File
The toolbox uses C functions for key operations. Compile `resampc.c` using the following command:
```matlab
mex resampc.c
```
This is a crucial step to ensure the toolbox runs correctly.

### Step 7: Enjoy!
Congratulations, you have successfully set up the Contourlet Transform Toolbox. You can now use it for image processing tasks.

## Troubleshooting Tips
- If MATLAB throws errors during compilation, ensure all files are present and correct.
- Verify that `resampc.mexw64` (Windows) or `resampc.mexa64` (Linux) is generated successfully after running the `mex` command.

## Final Notes
This repository was created to help others avoid the time-consuming setup process for the Contourlet Transform Toolbox. If you encounter any issues, feel free to raise them in the repository or contribute with your solutions.

Enjoy, and happy coding!

