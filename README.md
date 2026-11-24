# AmarTheme Updates

Public update feed for AmarTheme for Windows.

Feed: https://raw.githubusercontent.com/arkoshakib1-svg/AmarTheme-Updates/main/latest.json

The feed starts disabled until a real installer is available. To publish, create a stable GitHub Release with tag `vX.Y.Z` and attach the genuine installer named `AmarTheme-Setup.exe` before publishing. The update workflow (if enabled) generates the feed from the latest stable release, including its SHA-256 digest.

Client requirements: fetch the feed over HTTPS, require enabled=true, compare numeric versions, verify SHA-256 and trusted Authenticode publisher before executing an installer, and ask the user before installing. Never embed GitHub credentials in the client. Public reads require no token; publishing requires authorized repository access.

If the workflow is unavailable, update latest.json manually only after verifying the published installer and its checksum. No client updater or installer is included in this repository yet.
