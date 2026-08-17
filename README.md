<h2 align="center">Non-GKI Kernel Build</h2>

<p align="center">
  English | <a href="README_cn.md">中文说明</a> | <a href="Supported_list.md">Supported List</a> | <a href="https://github.com/JackA1ltman/NonGKI_Kernel_Build_2nd/wiki">Wiki</a> | <a href="https://t.me/+9XqfxcDtpkM2ZGE1">Telegram Group</a>
</p>
<p align="center">
  <img alt="GitHub Actions Workflow Status" src="https://img.shields.io/github/actions/workflow/status/JackA1ltman/NonGKI_Kernel_Build_2nd/build-samsung-s10-note10-series.yml?branch=mainline&style=for-the-badge">
 <img alt="GitHub License" src="https://img.shields.io/github/license/JackA1ltman/NonGKI_Kernel_Build_2nd?style=for-the-badge">
</p>

> [!NOTE]
> **Version 2.0**  
> **Get Sample：[sample](https://github.com/JackA1ltman/NonGKI_Kernel_Build_2nd/tree/sample)**  

### Introduction

This local streamlined version provides unified Non-GKI kernel builds for the Samsung **Galaxy S10 / Note10 series** only. The workflow checks out the default `bpf111` branch of [Star-Seven/M62-backport](https://github.com/Star-Seven/M62-backport) and runs its `build.sh --model all` flow for all nine supported devices: S10e, S10, S10+, S10 5G, Note10, Note10 5G, Note10+, Note10+ 5G (SM-N976B), and Note10+ 5G (SM-N976N). `d2xks` is only the SM-N976N device codename; it is not the sole build target.



> [!IMPORTANT]
>We are based on the [GPLv3 License](LICENSE)  
>
>We permit:
>  - Forking and using for personal compilation.
>  - Staring this project.
>  - Contributing to the project.
>  - Small-scale sharing of compilation results based on open-source and free provision.
>
>We do not permit:
>  - Using this project to provide paid services.
>  - Engaging in commercial activities without consent.

---

### Features

- [x] **Two all-series variants:** one manual run builds a standard SuSFS kernel and a Droidspaces SuSFS kernel; each job covers all nine S10/Note10 devices.
- [x] **Source alignment:** source and submodules always come from the default `bpf111` branch of `Star-Seven/M62-backport`.
- [x] **Native unified packaging:** both jobs run the upstream `build.sh --model all` flow with Android 16 parameters and its unified image archive.
- [x] **Kernel features:** the builds set up ReSukiSU, the SuSFS 2.2 backport, and manager query interfaces; ReSukiSU's built-in multi-manager signature compatibility allows Official KernelSU, RKSU, MKSU, and SukiSU-Ultra managers to coexist in one kernel; the Droidspaces variant additionally applies upstream non-GKI patches and `droidspaces.config`.
- [x] **Build environment:** GitHub Actions Ubuntu 24.04 with ARM64 cross-compilation.

---

### Acknowledgements

- Thanks to the contributors of the [Version 1.X series](https://github.com/JackA1ltman/NonGKI_Kernel_Build) (in no particular order):
  - [@adontoo](https://github.com/adontoo)
  - [@PeterTea5822](https://github.com/PeterTea5822)
  - [@pkczc](https://github.com/pkczc)
  - [@yu13140](https://github.com/yu13140)
- Thanks to [KernelSU_Action](https://github.com/xiaoleGun/KernelSU_Action) - @xiaoleGun for providing much of the inspiration for this project.
- Thanks to every user who has provided an **Issue**.
- Thanks to the users who provided **Issues** or ideas for this project on **CoolAPK**.

### Copyright
- [KernelSU](https://github.com/tiann/KernelSU) - @tiann
  - [rsuntk](https://github.com/rsuntk/KernelSU) - @rsuntk
    - [rsuntk-SuSFS](https://github.com/cyberc3dr/KernelSU) - @cyberc3dr
  - [xxksu](https://github.com/backslashxx/KernelSU) - @backslashxx
  - [SukiSU-Ultra](https://github.com/SukiSU-Ultra/SukiSU-Ultra) - @ShirkNeko
    - [ReSukiSU](https://github.com/ReSukiSU/ReSukiSU) - @ReSukiSU Development
      - [ReSukiSU_CI](https://github.com/cctv18/ReSukiSU_CI) - @cctv18
  - [Next](https://github.com/KernelSU-Next/KernelSU-Next) - @rifsxd
- [SuSFS](https://gitlab.com/simonpunk/susfs4ksu) - @simonpunk
- [Re:Kernel](https://github.com/Sakion-Team/Re-Kernel) - @Sakion-Team
- [Baseband Guard](https://github.com/vc-teahouse/Baseband-guard) - @秋刀鱼
- [Droidspaces](https://github.com/ravindu644/Droidspaces-OSS) - @ravindu644
- [NoMount](https://github.com/maxsteeel/nomount) - @maxsteeel
- And to more open-source kernel authors.
