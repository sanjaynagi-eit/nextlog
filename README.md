# 🪵 nextlog 

`nflog` is a small CLI and Python library that inspects recent Nextflow runs in a project directory. It reads `.nextflow/history`, `.nextflow.log`, and `work/**/.command.*` files to summarize runs and surface failing tasks quickly.

## Install

Clone the repo and install with pip:

```bash
pip install -e .
```

## CLI usage

- Quick summary: `nflog` (shows status + failures for the most recent run)
- List runs: `nflog runs --limit 5`
- Run status: `nflog status` or `nflog status --run <session-id>`
- Show failing tasks: `nflog failed --show 3` (alias `nflog f`)
- Show a specific failure: `nflog f 3` (prints the error/log content)

Use `--json` on any command for machine-readable output and `--debug` to see which artifacts were used.