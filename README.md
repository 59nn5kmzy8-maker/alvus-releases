# Alvus for Mac

Downloads and the update feed for Alvus. No source code lives here.

## Install (recommended: no security warning)

Open **Terminal** (Spotlight → "Terminal") and paste:

```bash
curl -fsSL https://github.com/59nn5kmzy8-maker/alvus-releases/releases/latest/download/install.sh | bash
```

It downloads the newest Alvus, checks it (checksum and signature), puts it in Applications and opens it. Then sign in with the email and access key you were given.

## Or with the .dmg

Download `Alvus-<version>-universal.dmg` from [the newest release](https://github.com/59nn5kmzy8-maker/alvus-releases/releases/latest), open it and drag Alvus to Applications.

macOS then says it **cannot verify Alvus** (it is not signed with a paid Apple Developer ID). Allow it once:

1. Open Alvus and click **Done** on the message.
2. **System Settings → Privacy & Security**, scroll down to *"Alvus" was blocked* → **Open Anyway** → confirm.

Still blocked, or it says the app is "damaged"? In Terminal: `xattr -dr com.apple.quarantine /Applications/Alvus.app`, then open it again.

## Updates

Alvus updates itself: at launch it installs a newer release before you use it. Every release is signed; the app installs nothing that is not.
