# ec-round2-260431305
#1.开发环境概述
  本项目基于STM32F103C8T6核心板开发，采用STM32CubeMX生成底层代码，结合CMake构建系统与GCC交叉编译工具链进行开发与调试。
##2.硬件环境（MCU&接线）
  * **主控芯片**：STM32F103C8T6(ARM Cortex——M3）
  * **下载调试器**：ST-link v2
  * **接线说明**：
  * ST-Link'SWDIO'->核心板'TMS'
  * ST-Link'SWCLK'->核心板'TCK'
  * ST-Link'GND'->核心板'GND'
  * ST-Link'3.3V'->核心板'3.3V'
##3.软件工具链与构建环境（Debug/Release)
    本项目采用VScode及以下工具链进行编译与调试：
  * **码生成工具**：STM32CubeMX(V6.X)
  * **构建系统**：CMake（v3.x及以上）
  * **交叉编译器**:GNU Arm Embedded Toolchain(GCCarm-none-aebi)
  * **集成开发环境**：Visual Studio Code（配合STM32Cube for VSCode插件）
  * **烧录与调试服务**：STM32CubeProgrammer/ST-LINK GBD Server
###3.1构建说明（如何编译0
  1.确保已安装CMake和GCC工具链，并已加入系统环境变量‘path'.
  2.在VS Code中打开本项目根录。
  3.**Debug模式编译**：
   * 点击底部状态栏的生成按钮，编译生成的elf和hex文件存放于’build/Debug/目录下。
  4.Release模式编译：
   * 在CMake工具扩展中，将构建体改为Release。
   * 重新点击Build，生成优化后的代码，存放于build/Release/目录下。
##3.2烧录与调试（
