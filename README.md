# Nuance-Research

Nuance-Research beta source and Windows installer repository.

## Download and install on Windows

[Download Nuance-Research for Windows x64](https://github.com/pjeu-oss/nuance-research/releases/download/windows-beta-0.11/Nuance-Research-Windows-x64-Setup.exe) (591 MB). Open the single `.exe` to install. No GitHub account, Python, Docker or GPU is required.

[Release notes and SHA-256 checksum](https://github.com/pjeu-oss/nuance-research/releases/tag/windows-beta-0.11). This unsigned beta may display a Windows publisher/reputation warning. Interactive laptop testing remains.

The complete curated project is in `Nuance-Research-Windows-cloud-build-0.11.zip`. Extract it to inspect or develop the FastAPI engine, web interface, bibliography tools, editor, resource guards, tests and desktop packaging. No private user documents, bibliography databases or access credentials are included.

## Build the Windows installer

Open **Actions → Windows beta installer → Run workflow**. The workflow unpacks the project and builds on a Windows Server 2022 x64 runner, using Python 3.12 and CPU-only PyTorch. Unit tests, frozen-engine search tests, silent installation and installed-engine tests must pass before an artifact is uploaded.

After success, download **Nuance-Research-Windows-x64-Beta** from the run's Artifacts section. It contains the single `Nuance-Research-Windows-x64-Setup.exe`, a SHA-256 checksum and build manifest. Artifacts expire after three days; download your copy promptly.

**Build status:** [Windows build #2 succeeded](https://github.com/pjeu-oss/nuance-research/actions/runs/37955754385) on 2026-10-09. The 591 MB artifact contains the installer, checksum and manifest. All 96 Windows unit tests, frozen-engine checks, silent installation, installed-engine search and uninstallation passed. The workflow includes a Windows startup compatibility correction to the archived source snapshot. Interactive GUI and laptop performance checks remain beta-test work. The generated installer is unsigned.

## Privacy and billing

This repository was made public with the owner's approval to share the installer. Never upload your personal library, `work`, `AppData`, databases or access keys. Check the account's Actions quota, artifact storage and spending settings before dispatch; no paid upgrade or larger runner is needed by the workflow. Use a zero spending limit if no cost is authorized.

Detailed architecture, licenses, installation and limitations are in the source archive's README and `desktop/BUILD-WINDOWS.md`.
