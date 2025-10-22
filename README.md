# Duress-Alert-Emergency-Alert-LAN-Messaging
LAN-based duress /emergency alert / messaging system with siren

A lightweight **LAN-based emergency alert system** designed and developed by **Asad Qureshi - asad@itmotivational.com (© 2025)** for hospitals, offices, and organizations needing fast, reliable internal alerts across all VLANs.

---

## Features
- Instant broadcast alerts across **LANs/VLANs** (uses `<broadcast>`)
- Supports **Duress Alerts** and **Custom Messages**
- Built-in **visual + audio alert system**   
  (sound is embedded in the EXE — no separate files required)
- Receiver auto-starts for all users
- Works **offline** — no internet dependency
- Compact, portable, and efficient EXE build (no install needed)
- **Open Source** under MIT License

---

## Installation

1. Copy both executables to a folder, e.g C:\LanAlertBuilder\Output\

2. To make the **receiver** auto-launch for all users at login, open **PowerShell as Administrator** and run:

powershell

$source = "C:\LanAlertBuilder\Output\LanAlert_Receiver.exe"
$startup = "$env:ProgramData\Microsoft\Windows\Start Menu\Programs\Startup"
Copy-Item $source -Destination $startup -Force

**Usage**

**Sender:**

Click "Duress Alert" for an emergency broadcast

Or enter a custom message and click Send Custom Message

**Receiver:**

Displays a full-screen red alert with flashing text

Plays a repeating siren until Acknowledge Alert is clicked

Shows sender name, PC, and timestamp

Works seamlessly across all subnets/VLANs where the receiver is running.

**Tech Details**

Built in Python 3.12

Uses socket for UDP broadcasting and tkinter for UI

Built into standalone .exe using PyInstaller

Fully self-contained — no runtime or dependencies needed

