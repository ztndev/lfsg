# lfsg

A Git LFS-backed file store with automated download and deletion workflows.

## Structure

```
├── .github/workflows/
│   ├── download-lfs.yml     # Downloads files and stores via LFS
│   └── delete-files.yml     # Deletes files removed from tracked-files.json
├── files/
│   ├── video/
│   ├── audio/
│   ├── images/
│   ├── documents/
│   ├── archives/
│   ├── data/
│   ├── binaries/
│   ├── fonts/
│   └── misc/
├── download-list.txt        # Add URLs here to trigger downloads
└── tracked-files.json       # Master file registry (auto-managed)
```

## Usage

### Download files
Add URLs to `download-list.txt` and push — the workflow triggers automatically.

### Delete files
Remove entries from `tracked-files.json` and push — the delete workflow triggers automatically.

### Manual trigger
Go to **Actions** → select a workflow → **Run workflow**.
