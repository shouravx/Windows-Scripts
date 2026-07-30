# 🚀 Windows Optimization Script (WinOpt)

**Version:** 7.0.b
**Author:** shouravx
**GitHub:** [https://github.com/shouravx](https://github.com/shouravx)

A **single-file, aggressive PowerShell Windows optimization framework** focused on **performance, visibility, and operator control**.

This is **not** a placebo tweaker, “FPS booster,” or beginner-safe tool.
It performs **real system changes**: services, policies, registry, scheduled tasks, and built-in applications.

---

## ⚠️ DISCLAIMER (READ FIRST)

This script **modifies core Windows behavior**.

* Intended for **advanced users only**
* Not suitable for managed, enterprise, or production systems
* Some actions are **partially irreversible** without OS reinstall
* You are responsible for every change applied

If you do not understand what Windows services, AppX provisioning, or system restore points are — **do not run Eternal Mode**.

---

## 🎯 DESIGN PRINCIPLES

* **No silent execution** — every action is printed
* **No fake optimizations** — only real system changes
* **No marketing lies** — limitations are disclosed
* **Control over safety theater**

This tool assumes competence, not consent dialogs.

---

## ✨ CORE FEATURES

### 🔐 Administrator Enforcement

* Script **refuses to run** without admin privileges
* Clear error message (no silent exit, no crash)
* No auto-elevation tricks

---

### 📜 Full Transparency & Logging

* Every operation is printed to console
* Color-coded output:

  * INFO / ACTION
  * WARNING
  * ERROR
* Full PowerShell transcript saved to `%TEMP%`

No background execution. No hidden failures.

---

### 💾 Real System Restore Support (Non-Placebo)

* Creates **actual Windows System Restore points**
* Uses:

  * `Win32_RestorePoint`
  * `Win32_SystemRestore`
* Rollback invokes **native Windows restore**
* May trigger reboot (by design)

Additionally:

* Services are backed up to CSV
* Scheduled tasks are exported as XML

> Restore is **best-effort**. Some removed components cannot be fully reconstructed.

---

### 📊 Built-In Benchmarking (Real Metrics)

* Uses `winsat formal`
* Displays:

  * CPU score
  * Memory score
  * Graphics score
  * D3D score
  * Disk score
* Results saved to timestamped logs

Designed for **before / after comparison**, not synthetic hype.

---

## ⚙️ OPTIMIZATION PROFILES

### 🎮 Gaming Performance

* Disables SysMain (Superfetch)
* Enables Hardware GPU Scheduling
* Reduces background memory pressure

**Risk:** Medium

---

### 🖥 Low-End System Optimization

* Disables Search indexing
* Minimizes telemetry via policy
* Stops low-priority background services

**Risk:** Medium
**Target:** HDD systems, low RAM machines

---

### 🧠 Developer / Workstation

* Disables UI animations
* Prioritizes responsiveness over visuals

**Risk:** Low

---

### 🧹 Debloated Minimal OS

* Removes most built-in AppX applications
* Disables Cortana and web search integration

**Risk:** High
Microsoft Store **may** be impacted.

---

### ☢️ Custom Aggressive (All Tweaks)

* Defender disabled
* Windows Update disabled
* Search disabled
* AppX removal
* SysMain disabled

Requires **explicit confirmation**.

**Risk:** Very High

---

### 🧨 Eternal Mode (Bare-Minimum Windows)

Extreme configuration intended for:

* Dedicated gaming installs
* Lab systems
* Virtual machines
* Disposable or purpose-built OS installs

Actions include:

* Disabling Defender, Update, Search, Telemetry
* Removing AppX packages
* Disabling diagnostics, print, biometrics, Xbox, maps
* Disabling UI effects
* Aggressive service reduction

⚠ **This mode can require OS reinstall to fully undo.**

---

## 🧪 WHAT THIS SCRIPT DOES NOT DO

* ❌ No fake FPS counters
* ❌ No registry “cleaning”
* ❌ No telemetry collection
* ❌ No internet communication
* ❌ No background persistence

Everything happens **locally**, **visibly**, and **on demand**.

---

## ▶️ HOW TO RUN
### Windows Performance Tuner.
[Can Run Any Time.]
### Local Execution
```
Set-ExcutionPolicy Bypass -Scope Process
.\wp-Tuner.ps1
```
Run **Powershell As Administrator**.
---
### Remote Execution

```
iex (irm https://raw.githubusercontent.com/shouravx/Windows-Scripts/refs/heads/main/Windows-Optimizer/wp-Tuner.ps1)
```

### Windows-Optimizer
[Run Only After windows inallation and Installing Driver.  This Might Revmove Microsoft Apps.]

### Local Execution (Recommended)
 
```powershell
Set-ExecutionPolicy Bypass -Scope Process
.\WinOpt.ps1
```

Run **PowerShell as Administrator**.

---

### Remote Execution (Only if you trust the source)

```powershell
irm https://raw.githubusercontent.com/shouravx/Windows-Scripts/refs/heads/main/Windows-Optimizer/Windows-Optimizer.ps1 | iex
```

You are expected to **read the code first**.

---

## 📁 FILES & LOGS

Stored in `%TEMP%`:

* `WinOpt_YYYYMMDD_HHMMSS.log` – Full transcript
* `ServicesBackup_*.csv` – Service state snapshot
* `TasksBackup_*` – Scheduled task XML backups
* `WinOpt_Benchmark_*.log` – Benchmark results

---

## 🔁 ROLLBACK PROCEDURE

1. Select **Rollback to Restore Point**
2. Confirm with `YES`
3. Windows System Restore takes over
4. Reboot may occur automatically

If Eternal Mode was used, rollback **may be incomplete**.

---

## 🛣 ROADMAP (REALISTIC)

* Best-effort service/task restore engine
* Hardware-aware suggestion engine
* Dry-run (`WhatIf`) mode
* Windows build detection
* Optional module packaging

No GUI planned. No beginner mode planned.

---

## 👤 AUTHOR

**shouravx**
Cyber Security Engineer
GitHub: [https://github.com/shouravx](https://github.com/shouravx)

---

## 🧨 FINAL WARNING

This script **does exactly what it says**.

* Read the code
* Understand the consequences
* Check the logs
* Accept the risk

If that mindset is uncomfortable — **do not use this tool**.
