# 💼 HP EliteBook 840 G3 · OpenCore Hackintosh EFI

**Intel Core i5-6300U · Intel HD 530 · 8GB DDR4 · Skylake · macOS Sonoma/Ventura**

<div align="center">

![CPU](https://img.shields.io/badge/CPU-i5_6300U_6th_Gen-0071C5?style=flat-square)
![GPU](https://img.shields.io/badge/GPU-Intel_HD_530-0071C5?style=flat-square)
![RAM](https://img.shields.io/badge/RAM-8_GB_DDR4-8B5CF6?style=flat-square)
![OpenCore](https://img.shields.io/badge/OpenCore-1.0.4-9cf?style=flat-square)
![Status](https://img.shields.io/badge/Status-Working_✓-brightgreen?style=flat-square)

**[💻 硬件配置](#硬件配置) · [⚙️ BIOS](#bios-设置) · [✅ 驱动](#驱动状态) · [📸 截图](#截图) · [🚀 安装](#安装步骤)**

</div>

---

## 📌 关键信息

| 指标 | 说明 |
|:---:|:-----|
| **笔记本型号** | HP EliteBook 840 G3（商务本） |
| **支持系统** | ✅ macOS Sonoma · Ventura · Monterey |
| **完整度** | ⭐⭐⭐⭐⭐ 99% 功能完整 |
| **推荐用途** | 📱 日常办公 · 📊 轻度生产力 |

---

## 💻 硬件配置

| 组件 | 规格 | 驱动状态 |
|:-----|:-----|:-------:|
| **CPU** | Intel Core i5-6300U | ✅ |
| **GPU** | Intel HD Graphics 530 | ✅ |
| **RAM** | 8 GB DDR4 2133 MHz | ✅ |
| **触控板** | Synaptics SMBus | ✅ |
| **声卡** | Conexant CX20724 | ✅ |
| **Wi-Fi** | Intel Wireless-AC 8260 | ✅ |
| **蓝牙** | Intel BT | ✅ |
| **网卡** | Intel I219-LM | ✅ |

---

## ⚙️ BIOS 设置

| 选项 | 值 | 说明 |
|:-----|:---:|:-----|
| **Intel SGX** | Disabled | 避免兼容性问题 |
| **Fast Boot** | Disabled | 启动稳定性 |
| **Boot Mode** | UEFI | 现代启动方式 |
| **Legacy Boot** | Disabled | UEFI only |
| **Secure Boot** | Disabled | macOS 不支持 |
| **Hyperthreading** | Enabled | 性能优化 |
| **VT-x** | Enabled | 虚拟化支持 |
| **VT-d** | Disabled | 可选 |
| **Video Memory** | 64 MB | 核显显存 |

---

## ✅ 驱动状态

### 🟢 完全工作

| 功能 | 状态 | 功能 | 状态 |
|:-----|:---:|:-----|:---:|
| **音频** | ✅ | **Wi-Fi** | ✅ |
| **有线网** | ✅ | **蓝牙** | ✅ |
| **核显** | ✅ | **USB** | ✅ |
| **触控板** | ✅ | **睡眠** | ✅ |
| **电池** | ✅ | **亮度** | ✅ |

---

## 📸 截图

### 系统信息

![System Info](https://via.placeholder.com/400x300?text=HP+EliteBook+840+G3+System+Info)

### 关于本机

![About Mac](https://via.placeholder.com/400x300?text=About+This+Mac)

---

## 📁 EFI 结构

```
EFI/
├── BOOT/BOOTx64.efi
└── OC/
    ├── ACPI/ (SSDT-EC, SSDT-PLUG, ...)
    ├── Drivers/ (OpenRuntime, HfsPlus)
    ├── Kexts/ (Lilu, VirtualSMC, WhateverGreen, ...)
    └── config.plist
```

---

## 🚀 安装步骤

### 1️⃣ BIOS 配置

1. 重启进入 BIOS（F10 键）
2. 按照上方表格配置所有选项
3. 保存并退出

### 2️⃣ 制作启动盘

```bash
# 创建 macOS 启动盘
gibMacOS.command
# 选择版本 → 创建 USB
```

### 3️⃣ 配置 EFI

1. 使用 OpenCore Configurator 挂载 USB EFI
2. 复制本配置的 EFI 文件夹
3. 生成 SMBIOS 三码（MacBookPro13,3）
4. 编辑 config.plist 替换序列号

### 4️⃣ 启动安装

```
1. 从 USB 启动（F9 选择启动盘）
2. OpenCore 菜单 → Install macOS
3. 完成安装（约 30 分钟，2 次重启）
4. 将 EFI 复制到硬盘 EFI 分区
```

---

## 🔧 关键 Kexts

| Kext | 功能 | 必需 |
|:-----|:-----|:---:|
| **Lilu.kext** | 内核补丁 | ✅ |
| **VirtualSMC.kext** | SMC 模拟 | ✅ |
| **WhateverGreen.kext** | 核显修复 | ✅ |
| **AppleALC.kext** | 声卡驱动 | ✅ |
| **IntelMausi.kext** | 网卡驱动 | ✅ |
| **AirportItlwm.kext** | Wi-Fi 驱动 | ✅ |
| **IntelBluetoothFirmware.kext** | 蓝牙固件 | ✅ |

---

## ⚠️ 注意事项

1. **生成三码**：必须使用 GenSMBIOS 生成唯一序列号
2. **勿复用序列**：本仓库的序列号已注册，请勿直接使用
3. **触控板精调**：可在安装后调整灵敏度
4. **电池优化**：启用 CPUFriend 进一步降低功耗
5. **定期备份**：保留一个工作 USB 作为应急启动盘

---

## 📊 性能表现

- **Geekbench 6** 单核：~850-900
- **续航时间**：8-10 小时（正常使用）
- **CPU 温度**：空闲 35°C · 满载 75°C
- **GPU 性能**：足够日常任务

---

## 🔗 参考资源

- [OpenCore 安装指南](https://dortania.github.io/OpenCore-Install-Guide/)
- [HP EliteBook 驱动支持](https://github.com/acidanthera)
- [Hackintosh 笔记本配置](https://reddit.com/r/hackintosh)

---

## 📄 许可证

MIT License - 仅供学习和研究使用

---

<p align="center">
  <b>为 Hackintosh 社区贡献 ❤️</b><br/>
  <sub>HP EliteBook 840 G3 · OpenCore 1.0.4 · 2026年</sub>
</p>