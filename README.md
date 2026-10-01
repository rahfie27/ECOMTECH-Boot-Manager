# ECOMTECH Boot Manager

ECOMTECH Boot Manager is a Windows-focused desktop utility for inspecting and managing boot, recovery, power, and startup settings through a PyQt6 graphical interface.

## Highlights

- View current boot mode, firmware type, Hibernate/Fast Startup state, and Safe Mode status
- Configure one-time Safe Mode boots
- Open Advanced Startup and UEFI Firmware Settings when supported
- Manage Windows boot-menu timeout and boot policy
- Restart, shut down, sign out, sleep, and hibernate with confirmation and configurable delays
- Toggle selected startup/system tweaks
- Open Windows Startup Apps settings
- Maintain an application log in the ECOMTECH application-data directory
- Run elevated when administrator privileges are required
- Persistent application settings
- Windows executable packaging with PyInstaller

## Requirements

- Windows 10/11
- Python 3.10+
- PyQt6

Install runtime dependencies:

```powershell
py -m pip install -r requirements.txt
```

Run from source:

```powershell
py -3 main.py
```

Or use:

```text
run.bat
```

## Build a Windows EXE

The repository includes a ready-to-use build script:

```text
build_exe.bat
```

It installs the build dependencies, generates the application icon, and builds:

```text
dist\ECOMTECH_Windows_Boot_Manager.exe
```

The PyInstaller build requests administrator execution and bundles the `assets` directory.

## Project Layout

- `main.py` — application source
- `requirements.txt` — runtime dependencies
- `requirements-build.txt` — runtime + build dependencies
- `build_exe.bat` — Windows PyInstaller build
- `run.bat` — run from source
- `install_and_run.bat` — install and launch helper
- `make_icon.py` — icon generation helper
- `assets/` — bundled application assets
- `legacy_scripts/` — retained legacy scripts, when present
- `VERSION.txt` — release version marker

## Safety Notes

This application can change Windows boot configuration and power/system settings. Review each operation before applying it, keep backups where appropriate, and avoid changing boot configuration on systems where recovery access is unavailable.

Many operations require administrator privileges. The application detects elevation and can request an elevated restart on Windows.

## Version

Current application version: **1.1.1**

## License

MIT License. See `LICENSE`.
