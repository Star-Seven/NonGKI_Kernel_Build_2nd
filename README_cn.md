<h2 align="center">Non-GKI 内核自动化编译项目</h2>

<p align="center">
  <a href="README.md">English</a> | 中文说明 | <a href="Supported_list.md">支持列表</a> | <a href="https://github.com/JackA1ltman/NonGKI_Kernel_Build_2nd/wiki">Wiki</a> | <a href="https://t.me/+9XqfxcDtpkM2ZGE1">Telegram 群组</a>
</p>
<p align="center">
  <img alt="GitHub Actions Workflow Status" src="https://img.shields.io/github/actions/workflow/status/Star-Seven/NonGKI_Kernel_Build_2nd/main.yml?branch=mainline&style=for-the-badge">
 <img alt="GitHub License" src="https://img.shields.io/github/license/JackA1ltman/NonGKI_Kernel_Build_2nd?style=for-the-badge">
</p>

> [!NOTE]
> **版本：2.0**  
> **获取示例：[sample](https://github.com/JackA1ltman/NonGKI_Kernel_Build_2nd/tree/sample)**  

### 简介  
本地精简版本仅为三星 **Galaxy S10 / Note10 系列**提供统一的 Non-GKI 内核构建流程。工作流从 [Star-Seven/M62-backport](https://github.com/Star-Seven/M62-backport) 的默认 `bpf111` 分支拉取源码，并沿用该仓库的 `build.sh --model all` 为全部九个受支持设备生成统一刷机包：S10e、S10、S10+、S10 5G、Note10、Note10 5G、Note10+、Note10+ 5G（SM-N976B）和 Note10+ 5G（SM-N976N）。其中 `d2xks` 仅对应 SM-N976N，是全系列中的一个设备代号，并非唯一构建目标。

> [!IMPORTANT]
>我们基于[GPLv3协议](LICENSE)  
>
>我们允许
>    - Fork 并用于自行编译
>    - Star本项目
>    - 参与贡献项目
>    - 基于开源和免费提供意向的小范围编译成果分享
>
>我们不允许
>    - 利用本项目提供付费项目
>    - 未经同意进行商业行为

---

### 特性

- [x] **全系列双变体**：一次手动触发分别构建标准 SuSFS 内核与 Droidspaces SuSFS 内核；每个作业均覆盖全部九个 S10/Note10 设备。
- [x] **源码固定**：始终从 `Star-Seven/M62-backport` 的默认 `bpf111` 分支检出源码与子模块。
- [x] **原生统一打包**：两个作业均通过上游 `build.sh --model all` 使用 Android 16 参数和统一镜像归档生成安装 ZIP。
- [x] **内核功能**：构建时接入 ReSukiSU 14574、SuSFS 2.2 后移植与管理器查询接口；生成的内核实际仅集成 ReSukiSU。Droidspaces 作业额外应用上游 non-GKI 补丁和 `droidspaces.config`。
- [x] **运行环境**：GitHub Actions Ubuntu 24.04，ARM64 内核交叉编译。
    
---

### 鸣谢

- 感谢来自 [版本：1.X](https://github.com/JackA1ltman/NonGKI_Kernel_Build) 系列的贡献者（排名不分前后）:
    - [@adontoo](https://github.com/adontoo)
    - [@PeterTea5822](https://github.com/PeterTea5822)
    - [@pkczc](https://github.com/pkczc)
    - [@yu13140](https://github.com/yu13140)
- 感谢 [KernelSU_Action](https://github.com/xiaoleGun/KernelSU_Action) - @xiaoleGun 为本项目提供了诸多灵感
- 感谢每一名提供**Issue**的用户
- 感谢曾在**酷安**为本项目提供**Issue**或构思的用户

### 版权
- [KernelSU](https://github.com/tiann/KernelSU) - @tiann
    - [rsuntk](https://github.com/rsuntk/KernelSU) - @rsuntk
        - [rsuntk-SuSFS](https://github.com/cyberc3dr/KernelSU) - @cyberc3dr
    - [xxksu](https://github.com/backslashxx/KernelSU) - @backslashxx
    - [SukiSU-Ultra](https://github.com/SukiSU-Ultra/SukiSU-Ultra) - @ShirkNeko
        - [ReSukiSU](https://github.com/ReSukiSU/ReSukiSU) - @ReSukiSU Development
            - [ReSukiSU_CI](https://github.com/cctv18/ReSukiSU_CI) - @cctv18
- [SuSFS](https://gitlab.com/simonpunk/susfs4ksu) - @simonpunk
- [Re:Kernel](https://github.com/Sakion-Team/Re-Kernel) - @Sakion-Team
- [Baseband Guard](https://github.com/vc-teahouse/Baseband-guard) - @秋刀鱼
- [Droidspaces](https://github.com/ravindu644/Droidspaces-OSS) - @ravindu644
- [NoMount](https://github.com/maxsteeel/nomount) - @maxsteeel
- 以及更多的开源内核作者
