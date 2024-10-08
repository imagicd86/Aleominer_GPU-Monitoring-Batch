
This ![1](https://github.com/user-attachments/assets/6bc5dea4-1587-4c2c-a71e-c6afc5688c61)
release introduces a batch script that creates a virtual AI computation interface while running an Aleo mining program (`Aleominer`) in the background. The script monitors real-time GPU status, including power usage, core temperature, memory temperature, and memory usage, and displays it as part of a simulated AI task interface. Meanwhile, the `Aleominer` runs the actual mining process in the background.

Additionally, the script automatically generates logs to record GPU information during each session, making it easier to track performance and analyze data over time.

#### Key Features:
- Simulates an AI computation task on the front-end while `Aleominer` runs in the background for Aleo mining.
- Real-time monitoring of GPU power usage, core temperature, memory temperature, and memory usage for up to 6 GPUs.
- Displays structured data in a compact format with 2 GPUs displayed per line for ease of reading.
- Logs the GPU status at every update interval (every 3 seconds), with automatic timestamped log file generation.
- Refreshes every 3 seconds to show up-to-date GPU information.
- Customizable for various AI computation environments and use cases.

#### Automatic Log Generation:
- The script automatically creates a log file in the working directory for each session.
- Log filenames are timestamped in the format: `tensorflow_log_YYYY-MM-DD_HH-MM.txt`.
- Each log entry captures the real-time status of all monitored GPUs, including:
  - Power usage (W)
  - Core temperature (°C)
  - Memory temperature (°C)
  - Memory usage (MiB/GiB)
- Logs provide historical data for GPU performance tracking and debugging.

#### How to Use:
1. Clone this repository.
2. Run the batch script on a Windows system with `nvidia-smi` and NVIDIA drivers installed.
3. The Aleo mining program, named `tensorflow` in the script, will run in the background while the AI computation interface is displayed.
4. The script will output the following for each GPU:
   - Power usage (W)
   - Core temperature (°C)
   - Memory temperature (°C)
   - Memory usage (MiB/GiB)
   
5. The interface is updated every 3 seconds with real-time data, and logs are automatically generated in the working directory.

#### Requirements:
- Windows operating system with NVIDIA GPUs.
- Installed NVIDIA drivers and `nvidia-smi` tool.
- `Aleominer` software for Aleo mining.

Feel free to report any issues or contribute to this project!
本版本提供了一个批处理脚本，用于创建一个虚拟的AI计算界面，而实际的Aleo挖矿程序（Aleominer）在后台运行。该脚本能够实时监控显卡的功耗、核心温度、显存温度以及显存使用情况，并以结构化的方式展示在虚拟的AI任务界面中。同时，`Aleominer` 在后台进行Aleo挖矿操作。

此外，脚本会自动生成日志，记录每次监控过程中显卡的状态，便于后续进行性能跟踪与数据分析。

#### 主要功能：
- 前台模拟AI计算任务界面，后台运行 `Aleominer` 进行Aleo挖矿。
- 实时监控多达6张显卡的功耗、核心温度、显存温度和显存使用情况。
- 显示结构化的显卡信息，每行展示两张显卡，格式紧凑，便于阅读。
- 每3秒刷新一次，显示最新的显卡状态。
- 自动生成日志，记录显卡的实时状态，方便后续分析。
- 可根据不同的AI计算环境和需求进行自定义。

#### 日志自动生成：
- 脚本会在每次运行时自动生成日志文件，保存在工作目录中。
- 日志文件名以时间戳命名，格式为：`tensorflow_log_YYYY-MM-DD_HH-MM.txt`。
- 每个日志条目都会记录监控的显卡状态，包括：
   - 功耗（瓦特）
   - 核心温度（摄氏度）
   - 显存温度（摄氏度）
   - 显存使用情况（MiB/GiB）
- 日志可用于跟踪显卡的性能，并便于调试和分析。

#### 使用方法：
1. 克隆此仓库。
2. 在安装有 `nvidia-smi` 工具和NVIDIA驱动的Windows系统上运行批处理脚本。
3. Aleo挖矿程序（脚本中名为 `tensorflow`）将在后台运行，同时虚拟的AI计算界面在前台展示。
4. 脚本会实时显示每张显卡的以下信息：
   - 功耗（瓦特）
   - 核心温度（摄氏度）
   - 显存温度（摄氏度）
   - 显存使用情况（MiB/GiB）

5. 界面每3秒更新一次，并自动生成日志，保存在工作目录中。

#### 环境要求：
- Windows 操作系统，支持 NVIDIA 显卡。
- 已安装NVIDIA驱动和 `nvidia-smi` 工具。
- 用于Aleo挖矿的 `Aleominer` 软件。

欢迎反馈问题或为项目贡献代码！
