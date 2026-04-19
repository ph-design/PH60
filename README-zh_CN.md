[English Version](README.md) | 中文

**[GitHub 仓库](https://github.com/ph-design/PH60) | [Wiki](https://wiki.phdesign.cc/PH60/rev3_multi/) | [Discord](https://discord.gg/8UfQXcefPH) | [淘宝店](https://shop268559013.taobao.com) | [QQ 群](https://qm.qq.com/q/OY0mIxSRs4) | [定制工具](https://custom.phdesign.cc)**

---

# PH60 Rev.3

**PH60 Rev.3** 是一套 60% 三模机械键盘套件，包含 FDM 3D 打印外壳和 PH60 Rev.3 Multi PCB。本版主控换用 NRF52840，支持蓝牙 5.3 和 Nordic 2.4 GHz 私有协议（TBD），固件为 [ZMKs](https://github.com/ph-design/zmks)（基于 ZMK 的自定义分支），外壳围绕**无线**和**多配列兼容**重新设计。


![PH60 Rev.3 渲染](Assets/bloom.png)

![PH60 Rev.3 正面](Assets/front.png)

![PH60 Rev.3 背面](Assets/back.jpg)

![PH60 Rev.3 PCB](Assets/pcb.jpg)


## 特色

### PCB

+ [Nordic NRF52840](https://www.nordicsemi.com/products/nrf52840) 主控，蓝牙 5.3 + 2.4 GHz（TBD）。
+ [ZMKs](https://github.com/ph-design/zmks) 固件，通过 [ZMKs Studio](https://zmks.phdesign.cc/) 实时自定义键位。
+ 多配列支持 — ANSI / ISO / WK / WKL / HHKB，额外支持分裂空格：6.25u → 2.75u + 1u + 2.5u，7u → 3u + 1u + 3u。
+ 电池供电，内置电池连接器。

> **关于 ANSI/ISO 版本的说明：** Rev.3 目前仅发售 **Multi** 配列 PCB。本仓库中的 ANSI PCB 是早期原型，设计方案与 Multi 有根本性不同，没有独立的 ISO 版本。未来我们可能会基于 ZMKs 继续开发独立的 ANSI/ISO 版本。

### 外壳

+ 面向 FDM 3D 打印设计，适用于任意热床 ≥ 256 × 256 mm 的打印机，无需支撑。
+ 磁吸快拆卡扣，免工具拆装。
+ O 型圈 Gasket 定位板，不加填充也有扎实清脆的手感。
+ 模块化电池托板和磁铁抽屉，最大兼容 100 × 50 × 5 mm 锂聚合物电池和 10 × 5 × 5 mm 磁铁。
+ 自锁式无线接收器收纳槽，适用于绝大多数市售 2.4 GHz 接收器外壳。
+ 多种外壳变体：标准、WKL、HHKB（6u/7u）、分裂退格等选项。

### 定位板

+ 已有定位板：ANSI、ISO、WK、HHKB（6u/7u）、LS64、EC60，及各种分裂键配置。
+ 更多配列陆续更新。

## 相比 Rev.2 的变化

| | Rev.2 | Rev.3 |
| --- | --- | --- |
| **主控** | RP2040 | NRF52840 |
| **连接方式** | 仅 USB | USB + 蓝牙 5.3 + 2.4 GHz（TBD） |
| **固件** | QMK + VIA | ZMKs + ZMKs Studio |
| **供电** | USB 供电 | 电池供电 |
| **分裂空格** | 不支持 | 支持 6.25u 和 7u 分裂 |
| **外壳** | 三件式模块化 | 磁吸快拆，O 型圈 Gasket |

## 在线定制

通过 [custom.phdesign.cc](https://custom.phdesign.cc) 在线配置你的 PH60 Rev.3，支持实时 3D 预览。

![PHD 定制工具](Assets/customizer.png)

---

## 项目结构

```
PH60 Rev.3
├── Assets/                         # 预览图片
├── Case_Model_Rev3/                # 外壳 3D 模型文件（STEP）
├── LICENSE
├── PCB_Model_Rev3/                 # PCB 3D 模型文件
├── PCB_Rev3/
│   ├── ANSI/                       # ANSI 版本（早期原型）
│   └── Multi/                      # 多配列版本（主要版本）
├── Plates_Rev3/                    # 定位板文件（STEP）
├── Production/
│   ├── PH60-Rev3-ANSI/             # ANSI 生产文件
│   └── PH60-Rev3-Multi/            # Multi 生产文件
├── README.md
└── README-zh_CN.md
```

## 打印指南

外壳在打印机默认设置下即可获得良好效果。推荐参数：

| 设置项 | 推荐值 | 备注 |
| --- | --- | --- |
| 打印材料 | PLA 或 PETG | 高温材料会增加翘曲风险 |
| 层高 | 0.2 mm | 模型以 0.2 mm 为基准设计 |
| 壁厚 | 2 层 | — |
| 填充图案 | Gyroid | — |
| 填充密度 | 15% | — |
| 墙生成器 | Arachne | 提高打印速度 |
| 精准外墙尺寸 | 启用 | 减少层纹 |
| 支撑 | 关闭 | 设计为无支撑打印 |

打印前确保热床调平、清洁。上盖等细长件建议涂胶棒防翘曲。打印完可打磨以改善表面质感。

## 组装

### 物料清单

| 材料 | 数量 | 备注 |
| --- | --- | --- |
| 3D 打印外壳组件 | 1 套 | 建议 PLA 或 PETG |
| PH60 Rev.3 Multi PCB | 1 块 | 含预装 SMD 元件 |
| MX 兼容轴体 | 61+ | 因配列而异 |
| 键帽 | 1 套 | 兼容 60% 配列 |
| 锂聚合物电池（可选） | 1 个 | 推荐：100 × 50 × 5 mm，Molex 1.25 mm 端子 |
| 磁铁 | 8 个 | 推荐：10 × 5 × 3 mm，N52 |
| 硅胶 O 形圈 | 8 个 | 外径 9 mm，线径 1.5 mm |
| 硅胶防滑贴 | 4 个 | 推荐：20 × 10 × 2 mm |

详细组装步骤请参考 [Wiki](https://wiki.phdesign.cc/PH60/rev3_multi/)。

## 固件

### 获取固件

- **GitHub Actions**：从 [ZMKs 配置仓库](https://github.com/ph-design/ph_lite-zmk-config) 的 Actions 下载构建产物。
- **QQ 群**：加入 [512933670](https://qm.qq.com/q/OY0mIxSRs4)，在群文件中获取。

### 刷写固件

1. **进入 Bootloader**：按下 `FN + B + R`，或拔出空格键帽后用镊子快速轻触 `BOOT` 焊盘两次。
2. **刷入**：键盘变为 USB 存储设备，将 `.uf2` 固件文件复制进去，自动重启。

### 键位自定义

访问 [ZMKs Studio](https://zmks.phdesign.cc/) 进行实时键位编辑。

## 常见问题

**Q：哪些 3D 打印机可以打印 Rev.3 外壳？**
A：任何热床 ≥ 256 × 256 mm、支持 PLA 或 PETG 的 FDM 打印机。

**Q：Rev.3 外壳支持哪些配列？**
A：ANSI、ISO、HHKB、WK、WKL、LS64、EC60（NIZ 静电容）。定位板持续更新中。

**Q：为什么没有独立的 ANSI 或 ISO PCB？**
A：早期 ANSI 原型与 Multi PCB 设计上完全不同，我们选择集中做 Multi，一块板兼容所有配列。未来可能基于 ZMKs 开发独立版本。

**Q：支持哪些电池和磁铁尺寸？**
A：电池最大支持 100 × 50 × 5 mm 锂聚合物电池。磁铁推荐 10 × 5 × 3 mm（N52）。电池托板和磁铁抽屉可修改以适配其他尺寸。

## 获取帮助

- GitHub Issues：[ph-design/PH60](https://github.com/ph-design/PH60/issues)
- Discord：[discord.gg/phdesign](https://discord.gg/8UfQXcefPH)
- QQ 群：[512933670](https://qm.qq.com/q/OY0mIxSRs4)
- Wiki：[wiki.phdesign.cc](https://wiki.phdesign.cc/)