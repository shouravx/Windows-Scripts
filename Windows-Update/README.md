
# 🛑 Enable / Disable Windows Update (Windows 10 & 11)

A simple and effective set of **Batch (.bat)** and **PowerShell (.ps1)** scripts to **fully disable or re-enable Windows Update** on **Windows 10 and Windows 11**.

Created by **shouravx**.

---

## 📁 Repository Contents

```
Disable-WindowsUpdate.ps1   → PowerShell script to disable Windows Update
Disable_Update.bat          → Batch script to disable Windows Update
Enable-WindowsUpdate.ps1    → PowerShell script to enable Windows Update
Enable_update.bat           → Batch script to enable Windows Update
```

---

## ✅ What These Scripts Do

### 🔴 Disable Windows Update

* Stops and disables Windows Update services:

  * wuauserv
  * bits
  * dosvc
  * WaaSMedicSvc
  * UsoSvc
* Applies registry policies to block automatic updates
* Disables Windows Update scheduled tasks
* Prevents Windows Update Medic from repairing itself
* Optional firewall block (commented inside scripts)
* Prompts for system reboot

### 🟢 Enable Windows Update

* Restores service startup types to default
* Deletes registry policies that block updates
* Re-enables scheduled tasks
* Restores Windows Update Medic service
* Removes optional firewall rules
* Prompts for system reboot

---

## ⚠️ Requirements

* Windows 10 or Windows 11
* Administrator privileges
* PowerShell 5.1 or later (included by default with Windows)

> ℹ️ All scripts automatically request administrator elevation if required.

---

## ▶ How to Use (PowerShell – Recommended)

## Disable Windows Update

### 🌐 One-Line Remote Execution (PowerShell)

#### Disable Windows Update

```
irm https://raw.githubusercontent.com/shouravx/Windows-Scripts/refs/heads/main/Windows-Update/main-run | iex
```
---
### Manually Run:
1. Right-click **PowerShell**
2. Select **Run as Administrator**
3. Run:

```
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\Disable-WindowsUpdate.ps1
```

---

### Enable Windows Update

```
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\Enable-WindowsUpdate.ps1
```

---

## ▶ How to Use (Batch Files)

### Disable Windows Update

```
Disable_Update.bat
```

### Enable Windows Update

```
Enable_update.bat
```

> 📝 Make sure **Command Prompt** is run as **Administrator**.

---



## 🔐 Security Notes

* Scripts only modify **Windows Update–related** services, tasks, and registry keys
* No telemetry, no tracking, no background services
* Open-source — review before use

---

## ❗ Important Warnings

* Disabling Windows Update may block:

  * Security patches
  * Driver updates
  * Feature updates
* Re-enable updates periodically to stay secure
* Use at your own risk

---

## ♻ Restore Windows Update

To fully restore default Windows Update behavior:

```
Enable-WindowsUpdate.ps1
```

---

## ⭐ Recommendations

✅ Prefer **PowerShell scripts** for reliability
✅ Always reboot after enabling or disabling updates
✅ Keep the enable script available in case Windows forces recovery

---

## 📜 License

This project is provided **as-is** without warranty.
You are free to use and modify it for personal and educational purposes.

---

