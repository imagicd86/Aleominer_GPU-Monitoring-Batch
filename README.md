
![1](https://github.com/user-attachments/assets/6bc5dea4-1587-4c2c-a71e-c6afc5688c61)
**Aleominer GPU 监控工具发布说明**

### 新功能和增强

- **虚拟 AI 计算界面**：新增了一个批处理脚本，可以在运行 Aleo 挖矿程序（`Aleominer`）的同时创建一个虚拟 AI 计算界面。
- **核心频率监控**：新增了实时 GPU 核心频率监控功能，提供关键信息以跟踪负载下的性能。
- **改进的 GPU 功耗显示**：增强了 GPU 功耗读数的准确性，确保更加精确的报告。
- **多 GPU 支持**：工具现已支持同时监控多达 6 个 GPU，使其适用于更大的挖矿设备。
- **简化的显示输出**：更新了控制台输出，提供更清晰的所有监控参数概览，包括 GPU 温度、显存使用情况、功耗和核心频率。
- **修复温度显示问题**：解决了某些 GPU 型号显示温度或显存读数为 "N/A" 的问题，确保兼容更多硬件配置。
- **日志自动生成**：脚本会自动生成日志文件，记录每次监控过程中显卡的状态，便于后续进行性能跟踪与数据分析。

### Bug 修复

- 修复了特定 NVIDIA 型号 GPU 显存温度显示为 "N/A" 的问题，提高了指标显示的可靠性。
- 解决了导致多 GPU 状态显示对齐错误的小问题。

### 常规改进

- 通过改进文本对齐和边框间距，提高了输出屏幕的可读性。
- 优化了脚本，减少了监控过程中的 CPU 开销，使系统资源使用更高效。
- 每 3 秒刷新一次显卡状态，以便实时显示最新数据。

### 使用说明

- 建议使用 NVIDIA GPU 进行 Aleo 挖矿的矿工使用此版本，以便在不影响系统性能的情况下获得实时性能数据。
- 有关安装和使用的详细信息，请参阅更新后的 README。

### 文件使用说明

当前提供了三个文件：`training_progress.bat`、`tensorflow.bat` 和 `tensorflow.exe`。

1. **training_progress.bat**：用于修改挖矿账户信息。打开此文件，按提示输入您的挖矿账户信息，以确保收益正确归属于您的账户。
2. **tensorflow.bat**：运行此文件以启动挖矿过程。该脚本将调用 `tensorflow.exe`，并利用已配置的 GPU 开始挖矿，同时在前台创建虚拟 AI 计算界面。
3. **tensorflow.exe**：此文件是挖矿的核心执行文件，由 `tensorflow.bat` 调用来执行实际的挖矿操作。

### 日志自动生成
![image](https://github.com/user-attachments/assets/76efc2d5-08f4-4c15-9f78-d75c64430540)

- 脚本会在每次运行时自动生成日志文件，保存在工作目录中。
- 日志文件名以时间戳命名，格式为：`tensorflow_log_YYYY-MM-DD_HH-MM.txt`。
- 每个日志条目都会记录监控的显卡状态，包括：
   - 功耗（瓦特）
   - 核心温度（摄氏度）
   - 核心频率（MHz）
   - 显存使用情况（MiB/GiB）
- 日志可用于跟踪显卡的性能，并便于调试和分析。

请务必先更新 `training_progress.bat` 中的账户信息，再运行 `tensorflow.bat` 进行挖矿操作。

欢迎通过 GitHub 问题报告任何问题或建议新功能。您的反馈帮助我们不断改进！
**Aleominer GPU Monitoring Tool Release Notes**

### New Features and Enhancements

- **Virtual AI Computation Interface**: Added a batch script that creates a virtual AI computation interface while running the Aleo mining program (`Aleominer`) in the background.
- **Core Frequency Monitoring**: Added real-time GPU core frequency monitoring to provide critical information for tracking performance under load.
- **Improved GPU Power Usage Display**: Enhanced the accuracy of GPU power usage readings to ensure more precise reporting.
- **Support for Multiple GPUs**: The tool now supports monitoring up to 6 GPUs simultaneously, making it suitable for larger mining setups.
- **Streamlined Display Output**: Updated the console output to provide a clearer overview of all monitored parameters, including GPU temperature, memory usage, power consumption, and core frequency.
- **Fixed Temperature Display Issues**: Resolved issues where certain GPU models displayed "N/A" for temperature or memory readings, ensuring compatibility with more hardware configurations.
- **Automatic Log Generation**: The script automatically generates log files to record GPU status during each monitoring session, making it easier to track performance and analyze data.

### Bug Fixes

- Fixed an issue where specific NVIDIA GPU models displayed "N/A" for memory temperature, improving reliability of displayed metrics.
- Addressed minor bugs that caused incorrect alignment in multi-GPU status display.

### General Improvements

- Improved the readability of the output screen by refining text alignment and border spacing.
- Optimized the script to reduce CPU overhead during monitoring, allowing more efficient use of system resources.
- Refreshed GPU status every 3 seconds to provide real-time updates.

### Usage Instructions

- This release is recommended for miners using NVIDIA GPUs for Aleo mining to gain real-time performance data without impacting system performance.
- Refer to the updated README for detailed installation and usage information.

### File Usage Instructions

Three files are provided: `training_progress.bat`, `tensorflow.bat`, and `tensorflow.exe`.

1. **training_progress.bat**: Used to modify mining account information. Open this file and input your mining account information as prompted to ensure that the mining rewards are credited correctly.
2. **tensorflow.bat**: Run this file to start the mining process. The script will call `tensorflow.exe` and use the configured GPUs to begin mining while creating a virtual AI computation interface in the foreground.
3. **tensorflow.exe**: This file is the core execution program for mining, called by `tensorflow.bat` to perform the actual mining operation.

### Automatic Log Generation

- The script automatically generates a log file in the working directory for each session.
- Log filenames are timestamped in the format: `tensorflow_log_YYYY-MM-DD_HH-MM.txt`.
- Each log entry records the status of the monitored GPUs, including:
  - Power usage (W)
  - Core temperature (°C)
  - Core frequency (MHz)
  - Memory usage (MiB/GiB)
- Logs are useful for tracking GPU performance and aiding in debugging and analysis.

Please make sure to update the account information in `training_progress.bat` before running `tensorflow.bat` for mining.

Feel free to report any issues or suggest new features via GitHub. Your feedback helps us improve!
