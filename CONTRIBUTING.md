# Contributing

## Development

Create a virtual environment and install the runtime dependencies:

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
py -m pip install -r requirements.txt
```

Run the application:

```powershell
py -3 main.py
```

Before opening a pull request:

- Keep Windows-specific operations guarded by platform checks.
- Avoid destructive defaults.
- Preserve administrator/elevation checks.
- Update `VERSION.txt` and documentation when behavior changes.
- Run a syntax check with `py -m compileall main.py`.

## Pull Requests

Describe the Windows versions tested, the change made, and any boot/system settings affected by the change.
