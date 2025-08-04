# powershell
# Install Chocolatey via PowerShell

This script installs [Chocolatey](https://chocolatey.org/), a package manager for Windows. It sets the execution policy temporarily, enables TLS 1.2, and runs the official installation script from Chocolatey's website.

## ⚠️ Prerequisites

- Run the following script in an **elevated PowerShell window** (Run as Administrator).
- Requires PowerShell version 3 or higher.

## 🚀 Installation Command

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; `
[System.Net.ServicePointManager]::SecurityProtocol = `
[System.Net.ServicePointManager]::SecurityProtocol -bor 3072; `
iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
