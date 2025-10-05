# AirShare Updates Repository

This repository contains update manifests for AirShare application.

## Structure

```
{{target}}/{{arch}}/{{current_version}}/
├── latest.json
└── {{version}}.json
```

## Example files:

- `darwin-x86_64/0.1.0/latest.json` - Latest version info for macOS Intel
- `darwin-arm64/0.1.0/latest.json` - Latest version info for macOS Apple Silicon
- `windows-x86_64/0.1.0/latest.json` - Latest version info for Windows 64-bit
- `linux-x86_64/0.1.0/latest.json` - Latest version info for Linux 64-bit

## How to add a new update:

1. Create directory: `{{target}}-{{arch}}/{{current_version}}/`
2. Add `latest.json` with update information
3. Add version-specific `{{version}}.json` file

## Update JSON format:

```json
{
  "version": "0.1.1",
  "notes": "Bug fixes and improvements",
  "pub_date": "2025-01-27T12:00:00Z",
  "platforms": {
    "darwin-x86_64": {
      "signature": "dW50cnVzdGVkIGNvbW1lbnQ6IHNpZ25hdHVyZSBmcm9tIHRhdXJpIHNlY3JldCBrZXk...",
      "url": "https://github.com/jaksatomovic/airshare/releases/download/v0.1.1/airshare_0.1.1_x64.dmg"
    },
    "darwin-arm64": {
      "signature": "dW50cnVzdGVkIGNvbW1lbnQ6IHNpZ25hdHVyZSBmcm9tIHRhdXJpIHNlY3JldCBrZXk...",
      "url": "https://github.com/jaksatomovic/airshare/releases/download/v0.1.1/airshare_0.1.1_aarch64.dmg"
    },
    "windows-x86_64": {
      "signature": "dW50cnVzdGVkIGNvbW1lbnQ6IHNpZ25hdHVyZSBmcm9tIHRhdXJpIHNlY3JldCBrZXk...",
      "url": "https://github.com/jaksatomovic/airshare/releases/download/v0.1.1/airshare_0.1.1_x64_en-US.msi"
    },
    "linux-x86_64": {
      "signature": "dW50cnVzdGVkIGNvbW1lbnQ6IHNpZ25hdHVyZSBmcm9tIHRhdXJpIHNlY3JldCBrZXk...",
      "url": "https://github.com/jaksatomovic/airshare/releases/download/v0.1.1/airshare_0.1.1_amd64.AppImage"
    }
  }
}
```
