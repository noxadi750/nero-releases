# Nero Releases Repository Guide

This folder contains everything needed to host your NeroCaption v1 updates and AI model on GitHub.

---

### Step 1: Create a GitHub Repository
1. Go to **[github.com/new](https://github.com/new)**.
2. Repository name: `nero-releases` (Public repository).
3. Click **Create repository**.

---

### Step 2: Upload `version.json` to the Main Branch
1. On your repository page, click **Add file** > **Upload files**.
2. Drag and drop `version.json` from this folder into GitHub.
3. Click **Commit changes**.

---

### Step 3: Create a Release and Attach the 3 Assets
1. On the right side of your GitHub repository, click **Releases** > **Create a new release** (or **Draft a new release**).
2. Choose tag: type `v1.0.0` and click **Create new tag**.
3. Release title: `NeroCaption v1.0.0`
4. Under **"Attach binaries by dropping them here"**, drag and drop all 3 files from the `RELEASE_ASSETS` folder:
   - `NeroCaption_v1_Setup.exe` (Installer for users)
   - `nero_update.zip` (Silent background update file)
   - `ggml-base.bin` (AI speech model)
5. Click **Publish release**.

---

### How Auto-Updates Work After This:
- Whenever you make changes in the future, simply update `version.json` (e.g. `"version": "1.0.1"`) and upload a new `nero_update.zip` to a new release.
- Every user with Nero installed will detect it automatically in the background, update silently, and display:
  `⚡ NERO Updated! Please restart AE to apply.`
