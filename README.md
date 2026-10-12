<p align="center">
  <img src="https://play-lh.googleusercontent.com/GHFPwUryd9Sk-xKUpjrduaD3cOFzMOJ1ehnI51kGuXD47Lfs5RShCDX5_BuRQN5j0SK_T_eimYU04P6_7QhR" width="96" alt="Cisco Secure Client">
</p>

# Cisco Secure Client — Installers Archive

A personal archive of **Cisco Secure Client 5.x** installers for Windows, macOS and Linux (x86_64 and ARM64).

The repository itself contains only this README. **All files are published as [Releases](https://github.com/NeroDOC/cisco-clients/releases)**, one release per client version, with every file Cisco provides for that version.

> [!IMPORTANT]
> Cisco Secure Client is proprietary software owned by Cisco Systems, Inc. This repository is not affiliated with or endorsed by Cisco. Files are kept here for convenience and internal use only. Use them only if you are covered by a valid Cisco license / support contract. Official downloads: [software.cisco.com](https://software.cisco.com/download/home/286330811/type/282364313/).

---

## 📦 Where to get the files

- **Latest version:** [Releases → Latest](https://github.com/NeroDOC/cisco-clients/releases/latest)
- **All versions:** [Releases](https://github.com/NeroDOC/cisco-clients/releases)

| Item | Format | Example |
|---|---|---|
| Tag | `v<version>` | `v5.1.20.333` |
| Release title | `Cisco Secure Client <version>` | `Cisco Secure Client 5.1.20.333` |

---

## 🗂 Available versions

| Version | Win x64 | Win ARM64 | macOS | Linux x64 | Linux ARM64 | Notes |
|---|:---:|:---:|:---:|:---:|:---:|---|
| [5.1.20.333](https://github.com/NeroDOC/cisco-clients/releases/tag/v5.1.20.333) | ✅ | ✅ | ✅ | ✅ | ✅ | Secure Firewall Posture package (`secure-firewall-posture-…-k9.pkg`) |
| [5.1.19.1862](https://github.com/NeroDOC/cisco-clients/releases/tag/v5.1.19.1862) | ✅ | ✅ | ✅ | ✅ | ✅ |  |
| [5.1.14.145](https://github.com/NeroDOC/cisco-clients/releases/tag/v5.1.14.145) | ✅ | ✅ | ✅ | ✅ | ✅ | macOS: headend `.pkg` only |
| [5.1.9.113](https://github.com/NeroDOC/cisco-clients/releases/tag/v5.1.9.113) | ✅ | ✅ | ✅ | ✅ | — | NVM standalone (Win, Linux); macOS core-vpn webdeploy `.dmg` |
| [5.1.7.80](https://github.com/NeroDOC/cisco-clients/releases/tag/v5.1.7.80) | ✅ | ✅ | ✅ | ✅ | — | macOS core-vpn webdeploy `.dmg` |
| [5.1.6.103](https://github.com/NeroDOC/cisco-clients/releases/tag/v5.1.6.103) | ✅ | ✅ | ✅ | ✅ | — | Linux: generic + RPM installers (no DEB) |
| [5.1.5.65](https://github.com/NeroDOC/cisco-clients/releases/tag/v5.1.5.65) | ✅ | ✅ | ✅ | ✅ | — | NVM standalone (Win, macOS, Linux) |
| [5.1.4.74](https://github.com/NeroDOC/cisco-clients/releases/tag/v5.1.4.74) | ✅ | ✅ | ✅ | ✅ | — | Separate Windows MSIs: core-vpn, DART, posture |
| [5.1.3.62](https://github.com/NeroDOC/cisco-clients/releases/tag/v5.1.3.62) | ✅ | ✅ | ✅ | ✅ | — | Separate Windows MSIs: core-vpn, posture; macOS ISE Compliance module 4.3.3509.6400 |
| [5.1.2.42](https://github.com/NeroDOC/cisco-clients/releases/tag/v5.1.2.42) | ✅ | ✅ | ✅ | ✅ | — | Separate Windows MSIs: core-vpn, posture; macOS core-vpn & posture webdeploy `.dmg` |

| Status | Meaning |
|:---:|---|
| ✅ | Available |
| ⚠️ | Partially available — see Notes |
| — | Not available |

<!-- Add a new row for every new release (newest on top) -->

---

## 📁 What's inside a release

File names below use `<ver>` for the version, e.g. `5.1.20.333`.

> [!NOTE]
> Linux and macOS archives use `.tar.gz` up to 5.1.9.x and `.tgz` from 5.1.14.x. Linux ARM64 packages are available from 5.1.14.x. Older releases may also include extra files (separate Windows MSIs, NVM standalone, posture / ISE Compliance packages); see the Notes column above.

### 1. Headend packages — for ASA / FTD

Uploaded to the VPN headend. Users get the client automatically on first connect via the web portal.

| Platform | File |
|---|---|
| Windows x64 | `cisco-secure-client-win-<ver>-webdeploy-k9.pkg` |
| Windows ARM64 | `cisco-secure-client-win-arm64-<ver>-webdeploy-k9.pkg` |
| macOS | `cisco-secure-client-macos-<ver>-webdeploy-k9.pkg` |
| Linux x64 | `cisco-secure-client-linux64-<ver>-webdeploy-k9.pkg` |
| Linux ARM64 | `cisco-secure-client-linux-arm64-<ver>-webdeploy-k9.pkg` |
| Any | `external-sso-<ver>-webdeploy-k9.pkg` — External Browser SAML package (ASA 9.17.1+, FMC/FTD 7.1+) |

### 2. Pre-deployment packages — for end users

Installed directly on the endpoint, manually or via SCCM / Intune / Jamf / scripts.

| Platform | File | Contents |
|---|---|---|
| Windows x64 | `cisco-secure-client-win-<ver>-predeploy-k9.zip` | All module MSIs + `Setup.exe` |
| Windows ARM64 | `cisco-secure-client-win-arm64-<ver>-predeploy-k9.zip` | All module MSIs + `Setup.exe` |
| macOS | `cisco-secure-client-macos-<ver>-predeploy-k9.dmg` | Full installer (admin rights or managed device required) |
| Linux x64 | `cisco-secure-client-linux64-<ver>-predeploy-k9.tar.gz` | Generic installer script (up to 5.1.14.x) |
| Linux x64 | `cisco-secure-client-linux64-<ver>-predeploy-deb-k9.tgz` | DEB packages (Debian / Ubuntu) |
| Linux x64 | `cisco-secure-client-linux64-<ver>-predeploy-rpm-k9.tgz` | RPM packages (RHEL / Fedora) |
| Linux ARM64 | `cisco-secure-client-linux-arm64-<ver>-predeploy-deb-k9.tgz` | DEB packages |
| Linux ARM64 | `cisco-secure-client-linux-arm64-<ver>-predeploy-rpm-k9.tgz` | RPM packages |

### 3. Admin tools — Windows

| File | Purpose |
|---|---|
| `tools-cisco-secure-client-win-<ver>-profileeditor-k9.msi` | Standalone VPN Profile Editor |
| `tools-cisco-secure-client-win-<ver>-transforms.zip` | MSI transforms for customizing the installer |

### 4. API / SDK

| Platform | File |
|---|---|
| Windows | `cisco-secure-client-win-<ver>-vpnapi.zip` |
| macOS | `cisco-secure-client-macos-<ver>-vpnapi.tgz` |
| Linux x64 | `cisco-secure-client-linux64-<ver>-vpnapi.tgz` |
| Linux ARM64 | `cisco-secure-client-linux-arm64-<ver>-vpnapi.tgz` |

---

## 🔐 Deploying to Cisco ASA

1. Copy the headend packages to ASA flash:
   ```
   copy tftp://<server>/cisco-secure-client-win-<ver>-webdeploy-k9.pkg disk0:/
   ```
2. Register the images (the number sets the order the ASA offers them to clients):
   ```
   configure terminal
   webvpn
    anyconnect image disk0:/cisco-secure-client-win-<ver>-webdeploy-k9.pkg 1
    anyconnect image disk0:/cisco-secure-client-win-arm64-<ver>-webdeploy-k9.pkg 2
    anyconnect image disk0:/cisco-secure-client-macos-<ver>-webdeploy-k9.pkg 3
    anyconnect image disk0:/cisco-secure-client-linux64-<ver>-webdeploy-k9.pkg 4
    anyconnect image disk0:/cisco-secure-client-linux-arm64-<ver>-webdeploy-k9.pkg 5
    anyconnect enable
   ```
3. *(Only for SAML with external browser)* register the External SSO package:
   ```
   webvpn
    anyconnect external-browser-pkg disk0:/external-sso-<ver>-webdeploy-k9.pkg
   ```
4. Check and save:
   ```
   show webvpn anyconnect
   write memory
   ```

Old images: `no anyconnect image disk0:/<old-file>.pkg`, then `delete disk0:/<old-file>.pkg`.

---

## 🛠 Quick install (pre-deployment)

**Windows** — unzip the predeploy archive, then run `Setup.exe` or install the VPN module silently (as Administrator):
```powershell
msiexec /i cisco-secure-client-win-<ver>-core-vpn-predeploy-k9.msi /qn /norestart
```

**macOS** — open the `.dmg` and run the `.pkg`, or:
```bash
sudo installer -pkg "/Volumes/Cisco Secure Client/Cisco Secure Client.pkg" -target /
```

**Linux (DEB)**
```bash
tar xzf cisco-secure-client-linux64-<ver>-predeploy-deb-k9.tgz
sudo apt install ./<package>.deb
```

**Linux (RPM)**
```bash
tar xzf cisco-secure-client-linux64-<ver>-predeploy-rpm-k9.tgz
sudo dnf install ./<package>.rpm
```

---

## ✅ Verifying downloads

Files are uploaded exactly as downloaded from Cisco. To check a file, compute its SHA-512 and compare it with the hash shown on the Cisco download page (hover over the file name there).

```powershell
# Windows (PowerShell)
Get-FileHash .\<file> -Algorithm SHA512
```
```bash
# macOS
shasum -a 512 <file>

# Linux
sha512sum <file>
```

GitHub also shows a SHA-256 digest for every release asset on the release page.

---

## ⬇️ Downloading with GitHub CLI

```bash
# Latest release, all assets
gh release download -R NeroDOC/cisco-clients

# Specific version, Windows headend packages only
gh release download v5.1.20.333 -R NeroDOC/cisco-clients -p "*win*webdeploy*"
```

---

## 📝 Release notes

[Cisco Secure Client 5 Release Notes](https://www.cisco.com/c/en/us/td/docs/security/vpn_client/anyconnect/Cisco-Secure-Client-5/release/notes/release-notes-cisco-secure-client-5-1.html)
