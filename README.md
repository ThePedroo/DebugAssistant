# Meow's Debug Assistant

The simplest and most flexible logcat capturer for Android as a Magisk module.

## Features

- Captures logs across 3 boots
- Logs can be retrieved via ADB/root easily
- Meow's Debug Assistant's Secure Censor for censoring sensitive information

## Installation

### 1. Download the zip

The latest release can be found on the [Releases page](https://github.com/ThePedroo/DebugAssistant/releases). Download the latest `DebugAssistant-vX.X.X.zip` file.

### 2. Flash the zip

Using your preferred root manager app, such as Magisk, KernelSU or APatch, flash the downloaded zip file.

### 3. Reboot

Reboot your device to start capturing logs.

## Usage

After installation, the module will start capturing logs automatically. The logs will be saved in `/data/local/tmp/` directory with the following files:
- `DebugAssistant.log` - The oldest log file.
- `DebugAssistant-Boot1.log` - The second newest log file.
- `DebugAssistant-Boot2.log` - The newest log file.

They will be created after each reboot, and all logs will be kept for 3 boots. After the third boot, all logs will be deleted and new logs will be captured, in a cyclic manner.

You can retrieve the **redacted log** via the action button in the root manager app. When you click the button, it will redact the most recent log file available, and save it as `DebugAssistant-Redacted.log` in the same directory (`/data/local/tmp/`). You can then pull the redacted log file using ADB or access it with root permissions.

## Contribution

It is mandatory to follow the PerformanC's [contribution guidelines](https://github.com/PerformanC/contributing) to contribute to Debug Assistant. Following its Security Policy, Code of Conduct and syntax standard.

## License

Meow's Debug Assistant is licensed under [BSD 3-Clause License](LICENSE). You can read more about it on [Open Source Initiative](https://opensource.org/licenses/BSD-3-Clause).

* This project is considered as: [leading standard](https://github.com/PerformanC/contributing?tab=readme-ov-file#project-information).
