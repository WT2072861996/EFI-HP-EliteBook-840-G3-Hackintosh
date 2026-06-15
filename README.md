<p align="center">
  <img src="https://github.com/WT2072861996/WT-IMG/blob/0e97c9bdf78649c0ceb31fb8013598ce2cf3d105/20250413195928456.png" alt="HP EliteBook 840 G3" width="300" />
</p>

# 💻 HP EliteBook 840 G3 · OpenCore Hackintosh

<p align="center">
  <img src="https://img.shields.io/badge/CPU-Intel_Core_i5_6300U-0071C5?logo=intel&logoColor=white" alt="CPU" />
  <img src="https://img.shields.io/badge/GPU-Intel_UHD_530-0071C5" alt="GPU" />
  <img src="https://img.shields.io/badge/RAM-8GB_DDR4_2133MHz-8B5CF6" alt="RAM" />
  <img src="https://img.shields.io/badge/OpenCore-1.0.4-9cf?logo=opencollective&logoColor=white" alt="OpenCore" />
  <img src="https://img.shields.io/badge/Status-Working-success" alt="Status" />
</p>

<div align="center">
  <i>HP EliteBook 840 G3 黑苹果 OpenCore EFI 配置方案。</i>
  <br>
  <b>Intel Core i5-6300U · HD 530 · OpenCore 1.0.4</b>
</div>

---

## 💻 硬件规格

| 项目 | 规格 |
|------|------|
| **CPU** | Intel Core i5-6300U |
| **GPU** | Intel UHD Graphics 530 |
| **内存** | 8 GB DDR4 2133MHz |
| **触控板** | Synaptics SMBus |
| **声卡** | Conexant CX20724 |
| **Wi-Fi / 蓝牙** | Intel Wireless-AC 8260 |
| **有线网卡** | Intel I219-LM |
| **OpenCore** | 1.0.4（持续更新） |

---

## ⚙️ BIOS 设置

| 选项 | 设置 |
|------|:----:|
| Intel SGX | 🔴 关闭 |
| Fast Boot | 🔴 取消勾选 |
| UEFI Boot Order | 🟢 勾选 |
| Legacy Boot | 🔴 取消勾选 |
| Configure Legacy Support | 🔴 关闭 |
| Secure Boot | 🔴 关闭 |
| Hyperthreading | 🟢 开启 |
| VT-x | 🟢 开启 |
| VT-d | 🔴 关闭 |
| Video Memory Size | 64MB 或更高 |

---

## 📸 截图预览

| 机型外观 | |
|:--------:|:--------:|
| <img src="https://github.com/WT2072861996/EFI-HP-EliteBook-840-G3-Hackintosh/blob/31dd2db566519738586f4b34485a8bbed05ec0bc/Model/1.png" width="200"> | <img src="https://github.com/WT2072861996/EFI-HP-EliteBook-840-G3-Hackintosh/blob/31dd2db566519738586f4b34485a8bbed05ec0bc/Model/2.png" width="200"> |

| 关于本机 | 硬件信息 | 触控板 | 显卡 |
|:--------:|:--------:|:------:|:----:|
| <img src="https://github.com/WT2072861996/EFI-HP-EliteBook-840-G3-Hackintosh/blob/1e1262dc4ca7b685a06feaaaf50b58c831b1561b/After%20installation/1.png" width="200"> | <img src="https://github.com/WT2072861996/EFI-HP-EliteBook-840-G3-Hackintosh/blob/1e1262dc4ca7b685a06feaaaf50b58c831b1561b/After%20installation/2.png" width="200"> | <img src="https://github.com/WT2072861996/EFI-HP-EliteBook-840-G3-Hackintosh/blob/1e1262dc4ca7b685a06feaaaf50b58c831b1561b/After%20installation/3.png" width="200"> | <img src="https://github.com/WT2072861996/EFI-HP-EliteBook-840-G3-Hackintosh/blob/1e1262dc4ca7b685a06feaaaf50b58c831b1561b/After%20installation/4.png" width="200"> |

---

## 📦 使用说明

1. **BIOS 设置**：按上表调整 BIOS
2. **替换 EFI**：用 OpenCore Configurator 挂载 U 盘 EFI 分区，将本项目 EFI 完整复制进去
3. **首次启动**：选择 U 盘启动 → OpenCore 菜单 → Install macOS
4. **安装完成后**：将 EFI 复制到系统盘 EFI 分区，即可脱离 U 盘启动

> ⚠️ 本配置适用于 HP EliteBook 840 G3，不同配置可能存在差异。

---

<div align="center">
  <img src="https://img.shields.io/badge/Built_with_❤️_for_the_Hackintosh_Community-FF6B6B" alt="Built with love">
</div>
