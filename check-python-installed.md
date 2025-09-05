# Check if Python is installed

This document explains simple commands to verify whether Python is installed on your system and how to install it if needed.

## 1) Open a terminal / command prompt
- Windows: Command Prompt or PowerShell
- macOS: Terminal
- Linux: Terminal

## 2) Common commands to check Python
- Windows (Command Prompt or PowerShell):
  - python --version
  - py --version
  - python -V
  - where python   (shows path if on PATH)
  - PowerShell: Get-Command python

- macOS / Linux:
  - python3 --version
  - python --version  (may show Python 2 on older systems)
  - which python3
  - which python

## 3) Interpreting results
- Output like `Python 3.11.4` — Python is installed and the version is shown.
- `python: command not found` or `'python' is not recognized` — Python is not installed or not on your PATH.
- `where` / `which` prints a path (e.g., `/usr/bin/python3` or `C:\Users\You\AppData\Local\Programs\Python\Python311\python.exe`) — location of the executable.

## 4) Extra checks
- Check pip (Python package installer):
  - python -m pip --version
  - pip3 --version
- Print full Python version details:
  - python -c "import sys; print(sys.version)"
- If multiple Python versions are present, prefer `python3` for Python 3.x.

## 5) Quick install commands
- Windows: Download from https://python.org or use winget / Chocolatey:
  - winget install Python.Python.3
  - choco install python
  - Make sure to check "Add Python to PATH" during the installer step.

- macOS (Homebrew):
  - brew install python

- Ubuntu / Debian:
  - sudo apt update && sudo apt install python3 python3-pip

- Fedora:
  - sudo dnf install python3

- Arch Linux:
  - sudo pacman -S python

## 6) Troubleshooting / notes
- On Windows, the `py` launcher can be used to select versions: `py -3.10`.
- If a command is not found but Python is installed, you may need to add the Python install directory to your PATH environment variable.
- To verify a specific interpreter path: run the full path, e.g. `C:\path\to\python.exe --version` or `/usr/bin/python3 --version`.