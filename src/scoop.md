### Scoop安装软件指南

Scoop 是一个 Windows 下的命令行包管理器，可以轻松地安装、更新和管理软件。以下是安装和使用 Scoop 的步骤。

#### 安装步骤

1. **设置环境变量**：
   打开 PowerShell，以管理员身份运行以下命令：
   ```powershell
   $env:SCOOP='c:\Applications\Scoop'
   $env:SCOOP_GLOBAL='c:\GlobalScoopApps'
   [Environment]::SetEnvironmentVariable('SCOOP_GLOBAL', $env:SCOOP_GLOBAL, 'Machine')
   ```

2. **安装 Scoop**：
   继续在 PowerShell 中运行以下命令来安装 Scoop：
   ```powershell
   irm get.scoop.sh | iex
   ```

#### 常用功能

- **搜索软件**：
  ```powershell
  scoop search <软件名>
  ```
  
- **安装软件**：
  ```powershell
  scoop install <软件名>
  ```

- **更新软件**：
  ```powershell
  scoop update <软件名>
  ```

- **列出已安装的软件**：
  ```powershell
  scoop list
  ```

- **卸载软件**：
  ```powershell
  scoop uninstall <软件名>
  ```

- **查看软件信息**：
  ```powershell
  scoop info <软件名>
  ```

#### 常用软件推荐

- **开发工具（C/C++相关）**：
  - `gcc`: GNU C/C++ 编译器。
  - `clang`: 高性能的 C/C++ 编译器。
  - `make`: 构建自动化工具。
  - `cmake`: 跨平台的构建系统。
  - `gdb`: GNU 调试器。
  - `visual-studio`: Microsoft 的集成开发环境（IDE）。
  - `rustup`: Rust 编程语言的工具链安装程序。
  - `jetbrains-toolbox`: JetBrains IDE 管理工具，可以轻松安装和更新 JetBrains 的 IDE。

- **实用工具**：
  - `googlechrome`: 谷歌浏览器，快速且功能强大的网页浏览器。
  - `7zip`: 文件压缩工具。
  - `notepad++`: 文本编辑器。
  - `wget`: 命令行下载工具。
  - `curl`: 用于请求数据的工具。

#### 常用仓库

- **主要仓库**：
  - `scoop/shims`: 用于处理软件的快捷方式。
  - `scoop/main`: 默认仓库，包含大多数常用软件。
  - `scoop/versions`: 旧版本软件仓库，可以安装软件的历史版本。
  - `scoop/extras`: 包含更多软件包，通常是常用的桌面应用程序。

#### 添加仓库和安装软件

1. **添加 `extras` 仓库**：
   ```powershell
   scoop bucket add extras
   ```

2. **安装软件示例**：
   ```powershell
   scoop install googlechrome
   scoop install rustup
   scoop install jetbrains-toolbox
   ```
