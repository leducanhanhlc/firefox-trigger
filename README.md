# Firefox Trigger Service

This is a **public trigger repository** for the Firefox automation service.

## Purpose
- Serves as a public endpoint to trigger the private Firefox core service
- Contains no sensitive data or secrets
- Automatically restarts the Firefox service every ~6 hours

## Usage
**Do not manually run this workflow unless needed.**

The private service will automatically trigger this workflow for continuous operation.

## Architecture
```
Public Repo (firefox-trigger) 
    ↓ triggers
Private Repo (firefox-core)
    ↓ auto-restarts by calling back
Public Repo (loop continues)
```

## Security
- All secrets and Firefox profile data are stored in the private repository
- This repository only contains the trigger workflow
