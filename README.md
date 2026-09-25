# Alvus

Downloads and the update feed for Alvus, for **Mac** and **Windows**. No source code lives here.

**Download:** every file is on [the newest release](https://github.com/59nn5kmzy8-maker/alvus-releases/releases/latest).

| Your computer | Download |
|---|---|
| Mac (Apple silicon or Intel) | the Terminal command below, or `Alvus-<version>-universal.dmg` |
| Windows PC (most PCs) | `Alvus-<version>-x64.exe` |
| Windows on ARM (Surface Pro X, Snapdragon laptops) | `Alvus-<version>-arm64.exe` |

After installing, sign in with the email and access key you were given.

---

## Mac

### Install (recommended: no security warning)

Open **Terminal** (Spotlight → "Terminal") and paste:

```bash
curl -fsSL https://github.com/59nn5kmzy8-maker/alvus-releases/releases/latest/download/install.sh | bash
```

It downloads the newest Alvus, checks it (checksum and signature), puts it in Applications and opens it.

### Or with the .dmg

Download `Alvus-<version>-universal.dmg` from [the newest release](https://github.com/59nn5kmzy8-maker/alvus-releases/releases/latest), open it and drag Alvus to Applications.

macOS then says it **cannot verify Alvus** (it is not signed with a paid Apple Developer ID). Allow it once:

1. Open Alvus and click **Done** on the message.
2. **System Settings → Privacy & Security**, scroll down to *"Alvus" was blocked* → **Open Anyway** → confirm.

Still blocked, or it says the app is "damaged"? In Terminal: `xattr -dr com.apple.quarantine /Applications/Alvus.app`, then open it again.

---

## Windows (from version 0.1.3)

1. Download from [the newest release](https://github.com/59nn5kmzy8-maker/alvus-releases/releases/latest):
   - `Alvus-<version>-x64.exe` for most PCs,
   - `Alvus-<version>-arm64.exe` for Windows on ARM.

   Not sure which? **Settings → System → About → System type**: "x64-based" or "ARM-based".
2. Open the file. Windows SmartScreen says it *protected your PC* (Alvus is not signed with a paid certificate): click **More info → Run anyway**.
3. It installs for you only, no administrator needed, and opens Alvus.
4. The setup screen helps you install Claude Code and git if you don't have them yet.

**Recommended: secure your agents' terminal.** The setup screen offers one more step, *Secure your agents' terminal*. Windows asks for administrator rights once. Alvus then runs your agents' commands as a hidden Windows user of its own: no access to your files, and no internet unless you allow it. Without this step Alvus still works, but test runners that start other programs (such as `npm test` with `node --test`, jest or vitest) can fail inside the sandbox.

---

## Updates

Alvus updates itself, on Mac and Windows: at launch it installs a newer release before you use it. Every release is signed; the app installs nothing that is not.
