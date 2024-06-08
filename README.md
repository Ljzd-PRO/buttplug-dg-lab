# buttplug-dg-lab

本仓库提供 [buttplug](https://github.com/buttplugio/buttplug), [intiface-central](https://github.com/intiface/intiface-central), [intiface-engine](https://github.com/intiface/intiface-engine) 的 DG-Lab 适配分支

由于 Buttplug 并不适合郊狼这类产品，因此无法并入主分支

## 介绍

适配 郊狼 2.0, 3.0 (DG-Lab-V2, DG-Lab-V3)

郊狼 2.0 支持控制 [官方文档](https://github.com/DG-LAB-OPENSOURCE/DG-LAB-OPENSOURCE/blob/main/coyote/v2/README_V2.md) 中描述的
- 通道强度 `S`
- 脉冲频率 `Frequency`
- 脉冲宽度 `Z`

郊狼 3.0 支持控制 [官方文档](https://github.com/DG-LAB-OPENSOURCE/DG-LAB-OPENSOURCE/blob/main/coyote/v3/README_V3.md) 中描述的
- 通道强度
- 波形频率
- 波形强度

提供编译好的 Intiface Central 客户端。

## 关于 Buttplug

Buttplug 是一个开源的标准和软件项目，用于控制类似郊狼的各类设备。一般通过**蓝牙**连接设备。
> https://buttplug.io/

Intiface® Central 是一个面向用户的实现了 Buttplug 协议的开源跨平台软件，支持 Windows 10+, Linux, macOS, Android 以及 iOS。
> https://intiface.com/central/

借助 Intiface Central，设备（如郊狼）可以连接至应用了 Buttplug 协议的各类软件，比如游戏 Mod、视频播放器等。Intiface Central 将作为服务端，应用了 Buttplug 协议的各类软件通过 WebSocket 控制设备。
> - 一些已知的 Buttplug 项目：https://github.com/buttplugio/awesome-buttplug 
> - 其中一个游戏 Mod（Deppart Prototype）：https://github.com/Ljzd-PRO/DeppartPrototypeHentaiPlayMod

## 下载

- GitHub Actions 自动构建：https://github.com/Ljzd-PRO/intiface-central/actions/workflows/central.yml
- Release 发行版：https://github.com/Ljzd-PRO/buttplug-dg-lab/releases

## 主要代码

- https://github.com/Ljzd-PRO/buttplug/blob/master/buttplug/src/server/device/protocol/dg_lab_v2.rs
- https://github.com/Ljzd-PRO/buttplug/blob/master/buttplug/src/server/device/protocol/dg_lab_v3.rs
- https://github.com/Ljzd-PRO/buttplug/blob/master/buttplug/buttplug-device-config/device-config-v2/buttplug-device-config-schema-v2.json
- https://github.com/Ljzd-PRO/buttplug/blob/master/buttplug/buttplug-device-config/device-config-v2/buttplug-device-config-v2.yml
- https://github.com/Ljzd-PRO/buttplug/blob/master/buttplug/buttplug-device-config/device-config-v3/buttplug-device-config-schema-v3.json
- https://github.com/Ljzd-PRO/buttplug/blob/master/buttplug/buttplug-device-config/device-config-v3/buttplug-device-config-v3.yml

## 计划
- [x] 适配 DG-Lab-V3
- [ ] DG-Lab-V2 缺少实际测试，欢迎测试使用，可以反馈在 Issues 页面
- [ ] Intiface Central 的 GitHub Actions 自动构建 CI 脚本，无法成功构建 macOS App 和 Android APK
  > https://github.com/Ljzd-PRO/intiface-central/blob/main/.github/workflows/central.yml
