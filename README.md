# AirShare Updates Repository

This repository contains update manifests for AirShare application.

## Structure

```
{{version}}/latest.json
```

## Example:

- `0.1.0/latest.json` - Version 0.1.0 update manifest
- `0.1.1/latest.json` - Version 0.1.1 update manifest

## Update JSON format:

```json
{
  "version": "0.1.1",
  "notes": "Bug fixes and improvements",
  "pub_date": "2025-01-28T12:00:00Z",
  "platforms": {
    "darwin-arm64": {
      "signature": "base64-signature",
      "url": "https://github.com/airsharehq/airshare/releases/download/v0.1.1/airshare_0.1.1_arm64.dmg"
    },
    "darwin-x86_64": {
      "signature": "base64-signature", 
      "url": "https://github.com/airsharehq/airshare/releases/download/v0.1.1/airshare_0.1.1_x64.dmg"
    },
    "windows-x86_64": {
      "signature": "base64-signature",
      "url": "https://github.com/airsharehq/airshare/releases/download/v0.1.1/airshare_0.1.1_x64_en-US.msi"
    },
    "linux-x86_64": {
      "signature": "base64-signature",
      "url": "https://github.com/airsharehq/airshare/releases/download/v0.1.1/airshare_0.1.1_amd64.AppImage"
    }
  }
}
```

## How it works:

1. Tauri app requests: `https://raw.githubusercontent.com/airsharehq/airshare-updates/main/0.1.0/latest.json`
2. JSON contains all platform-specific download URLs and signatures
3. App downloads and installs the correct version for current platform
