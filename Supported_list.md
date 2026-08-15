# 支持的机型

本仓库从 [Star-Seven/M62-backport](https://github.com/Star-Seven/M62-backport) 的默认 `bpf111` 分支拉取源码，并复用其 `build.sh --model all` 为下表**全部九个**三星 Galaxy S10 与 Galaxy Note10 系列设备生成统一安装包。工作流分别构建标准 SuSFS 内核与 Droidspaces SuSFS 内核；每个安装包均包含全部设备所需的 boot、DTB 与 DTBO 映像。`d2xks` 仅是 SM-N976N 的设备代号，并非单独或唯一的构建目标。[1]

| 系列 | 设备代号 | 对应型号 | SoC 平台 | 统一包覆盖 |
|---|---|---|---|---|
| Galaxy S10e | `beyond0lte` | SM-G970F | Exynos 9820 | 是 |
| Galaxy S10 | `beyond1lte` | SM-G973F | Exynos 9820 | 是 |
| Galaxy S10+ | `beyond2lte` | SM-G975F | Exynos 9820 | 是 |
| Galaxy S10 5G | `beyondx` | SM-G977B | Exynos 9820 | 是 |
| Galaxy Note10 | `d1` | SM-N970F | Exynos 9825 | 是 |
| Galaxy Note10 5G | `d1xks` | SM-N971N | Exynos 9825 | 是 |
| Galaxy Note10+ | `d2s` | SM-N975F | Exynos 9825 | 是 |
| Galaxy Note10+ 5G | `d2x` | SM-N976B | Exynos 9825 | 是 |
| Galaxy Note10+ 5G | `d2xks` | SM-N976N | Exynos 9825 | 是 |

> **注意：** 请在刷入前确认设备型号、区域版本与当前系统兼容性。该工作流生成的是统一安装包，不再为其它品牌或机型构建内核。

## 构建方式

在 GitHub Actions 中手动运行 **Build Samsung S10 / Note10 Series Kernels**。该工作流提供两个全系列作业：标准 SuSFS 内核和 Droidspaces SuSFS 内核。两者均拉取 M62-backport 默认 `bpf111` 分支、初始化子模块、接入 ReSukiSU/SuSFS，并执行 `./build.sh --model all --ksu y --recovery n`。构建完成后，可分别下载两个作业生成的全系列 ZIP 文件。

## 参考资料

[1]: https://github.com/Star-Seven/M62-backport/blob/bpf111/build.sh "Star-Seven/M62-backport 的统一构建与打包脚本"
