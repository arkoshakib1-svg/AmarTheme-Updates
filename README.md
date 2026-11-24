# AmarTheme Updates — আমার থিম

Official public update feed for the **AmarTheme** Windows 11 app.

- **Repository:** https://github.com/arkoshakib1-svg/AmarTheme-Updates
- **Update feed:** https://raw.githubusercontent.com/arkoshakib1-svg/AmarTheme-Updates/main/latest.json
- **Installer release page:** https://github.com/arkoshakib1-svg/AmarTheme-Updates/releases
- **Latest prepared app build:** v2.3.1 (Premium Glass Pro, stability fixes).

## Current status

The feed is intentionally **disabled** until a genuine Windows installer has been published as a GitHub Release asset. Do not replace this with a download URL that returns 404.

## Publish v2.3.1

1. Go to **Releases → Draft a new release**.
2. Create tag **`v2.3.1`**, title **`Amar Theme v2.3.1`**.
3. Upload the genuine **`AmarTheme_v2.3.1_Stability_Fixed_Setup.exe`** build to the Release's **Assets**. The local build supplied in the ChatGPT conversation has:
   - **SHA-256:** `2b5eee0bf389823dc9544138c7114b8e274254922b68923f8218c01556a4188d`
   - **File size:** `17,167,360 bytes`
4. **Publish release** (not a draft or prerelease).

The **Publish AmarTheme update feed** GitHub Actions workflow automatically downloads the genuine released installer, computes its SHA-256, and publishes a compatible `latest.json`. Check the **Actions** tab for success.

The app currently reads `version`, `url`, `sha256`, and `notes`. The published JSON also includes `enabled`, `download_url`, and `release_notes` for forwards/backwards compatibility. The app downloads the installer over HTTPS, checks SHA-256, and asks the user before installation. A checksum is an integrity check, **not a publisher identity guarantee**.

## Configure the installed app

Save this in `%APPDATA%\AmarTheme\updates.json`:

```json
{
  "manifest_url": "https://raw.githubusercontent.com/arkoshakib1-svg/AmarTheme-Updates/main/latest.json"
}
```

Check **আপডেট → আপডেট পরীক্ষা করুন** in the app. If the current app version is already v2.3.1, a v2.3.1 feed does not offer an upgrade. Future versions require publishing a new genuine installer via a newer stable Release tag.

**Important:** The app is an unsigned Windows build and has not been runtime-tested on Windows 11; use antivirus scanning and only install a verified build you trust. Do not disable Windows security to install it. Repository access or push permission does not automatically grant the GitHub connector the ability to upload a binary Release asset.
