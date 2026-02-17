# ODrive 3.6 - AEAT9922 Firmware Integration

This repository contains a modified version of the ODrive 3.6 firmware, specifically updated to support the **AEAT9922** magnetic encoder via SPI. This is part of the larger Encoder-Interpolator-Bridge project.

## 🛠 Building the Firmware

This project uses the [ODrive 0.5.4 Documentation](https://docs.odriverobotics.com/v/0.5.4/configuring-vscode.html) standards for building and development.

### Prerequisites
1. **ARM GCC Toolchain:** [Download and install](https://developer.arm.com/tools-and-software/open-source-software-projects/gnu-toolchain/gnu-rm) the ARM embedded toolchain.
2. **Tup:** Ensure `tup` is installed and added to your system PATH.
3. **Environment Variable:** You must have a system environment variable named `ARM_GCC_ROOT` pointing to your toolchain folder.
   * *Example:* `C:\Program Files (x86)\GNU Tools Arm Embedded\7 2018-q2-update`

### Build Instructions (VS Code)
1. **Open Workspace:** You must open the project using the `ODrive_Workspace.code-workspace` file. This ensures VS Code loads the correct path variables for the ODrive build system.
2. **Run Build:** Press `Ctrl + Shift + B` to trigger the default build task (`make -j4`). Alternatively, pull down ...->Terminal->Run Build Task.
3. **Output:** The compiled files (`.bin`, `.hex`, `.elf`) will be located in the `Firmware/build` folder.

### Build Instructions (Manual Terminal)
If your terminal is configured with the correct paths, navigate to the `Firmware` directory and run:
```bash
make -j4