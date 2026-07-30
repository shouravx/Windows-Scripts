# Windows 10 → Windows 11 Automated Upgrade Script

A **fully automated PowerShell script** to perform an **in-place upgrade from Windows 10 to Windows 11**, including support for **unsupported hardware** using Microsoft-documented registry bypass methods.

Designed for advanced users, lab systems, and controlled environments.

---

## 🚀 Features

- Administrator privilege enforcement
- Runs **only on Windows 10**
- Verifies minimum **30GB free disk space**
- ISO source selection:
  - Automatic Windows 11 ISO download
  - Manual selection of an existing local ISO
- Downloaded ISO is always renamed to:
```

Win11_Auto.iso

````
- ISO validation:
- File existence
- `setup.exe` presence after mount
- Windows 11 hardware requirement bypass:
- TPM
- Secure Boot
- CPU
- RAM
- Silent in-place upgrade
- Preserves files, applications, and settings
- Optional reboot prompt
- Automatic cleanup:
- ISO dismount
- Downloaded ISO removal

---

## 🧰 Requirements

- Windows 10 (any supported edition)
- PowerShell 5.1
- Administrator privileges
- Minimum 30GB free disk space
- Internet connection (only if downloading ISO)

---

## ▶️ Usage

### Run directly from GitHub

```powershell
iex (irm https://raw.githubusercontent.com/shouravx/Windows-Scripts/main/TO-Win11-Auto-Upgrade/Win11-AutoUpgrade.ps1)
````

### Run locally

```powershell
powershell -ExecutionPolicy Bypass -File Win11-AutoUpgrade.ps1
```

---

## 📀 ISO Selection

During execution, choose one option:

### Option 1 — Automatic ISO Download

* Downloads Windows 11 ISO from Microsoft
* Renames it to `Win11_Auto.iso`
* Deletes the ISO after upgrade completes

### Option 2 — Manual ISO Location

* Prompts for full ISO file path
  Example:

  ```
  D:\ISO\Win11_23H2_English_x64.iso
  ```
* Script verifies:

  * ISO exists
  * `setup.exe` is present
* ISO is **not deleted**

---

## ⚠️ Warnings & Disclaimer

* This script **bypasses Microsoft hardware enforcement**
* Windows 11 on unsupported hardware:

  * Is **not officially supported**
  * May receive limited or no updates
* Do **not** use blindly in enterprise or production environments
* Always back up critical data before running

Use at your own risk.

---

## 📝 Notes

* Windows Setup may reboot automatically regardless of user choice
* BitLocker should be suspended manually if enabled
* OS corruption or pending updates can cause upgrade failure

---

## 👤 Author

**Shourav**
Cyber Security Engineer
GitHub: [https://github.com/shouravx](https://github.com/shouravx)

