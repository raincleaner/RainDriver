# Rain Driver

Back up, understand and recover Windows drivers - without random driver-pack sites.

[**Download the latest release**](https://github.com/raincleaner/RainDriver/releases/latest) · [Website](https://raincleaner.eu/driver) · [Guides](https://raincleaner.eu/guides)

Windows 7 SP1 to 11 · 32-bit and 64-bit · public beta · free version included

## What it does

- **Driver Passport** - saves your working third-party driver packages with a SHA-256 checksum for every file. Restore them after a Windows reinstall, network and storage drivers first.
- **Rescue Bundle** - Passport + drivers + a verified restore script on a USB stick, built for the moment a fresh Windows has no network driver.
- **Problem Doctor** - Device Manager codes (10, 28, 43 ...) explained in plain language, with safe diagnostic actions.
- **Timeline** - what changed on the PC, and when.
- **Protected updates** - restore point and a copy of the current drivers first; the previous package can be restored afterwards.
- **Official sources only** - Windows Update, the Dell / HP / Lenovo catalogs, NVIDIA's own service and the makers' official pages (AMD, Intel, Realtek, ASUS, MSI, Gigabyte, ASRock and others). Never third-party driver-pack sites.

## Why trust it

- No ads and no bundled software.
- It never installs a driver without asking; you confirm every change.
- A single portable `.exe` - not an installer. To remove it, delete the file.
- SHA-256 values are published for every release, here and on https://raincleaner.eu/trust.
- What leaves your PC (version check, licence activation, and Rain AI only if you ask) is listed on the Trust page.

### Public beta, not yet code-signed

The builds are **not code-signed yet** while the organisation's code-signing verification is being completed, so Windows may show an "unknown publisher" warning. Check the hash before you run it:

```powershell
Get-FileHash .\RainDriver-*.exe -Algorithm SHA256
```

## Free and Pro

| Free | Pro |
|---|---|
| Scan every driver, Driver Health report | One-click restore from a Driver Passport |
| Problem Doctor, Timeline | Install all available updates at once |
| Create a Driver Passport and Rescue Bundle | Rain AI included with Lifetime (optional add-on with Monthly / Yearly) |
| Official manufacturer packs and pages | Everything in Free |

Pro: €4.99 / month · €29.99 / year · €49.99 once. Rain Cleaner Pro owners get an automatic loyalty discount.

## No tools needed? The built-in way

You can do the core backup with Windows itself:

```cmd
pnputil /export-driver * D:\Drivers
pnputil /add-driver D:\Drivers\*.inf /subdirs /install
```

Step-by-step: [Back up drivers before reinstalling Windows 11](https://raincleaner.eu/guides/back-up-drivers-before-reinstalling-windows-11). Rain Driver is the same idea with checksums, a restore order and a graphical interface.

## Guides

- [Back up drivers before reinstalling Windows 11](https://raincleaner.eu/guides/back-up-drivers-before-reinstalling-windows-11)
- [Install the network driver after a reinstall, offline](https://raincleaner.eu/guides/install-network-driver-after-windows-reinstall-offline)
- [Unknown device in Device Manager](https://raincleaner.eu/guides/unknown-device-device-manager-find-driver-hardware-id)
- [Device Manager Code 28](https://raincleaner.eu/guides/device-manager-code-28-driver-not-installed)
- [Device Manager Code 43](https://raincleaner.eu/guides/device-manager-code-43-causes-fixes)

## Support and security

Questions: support@raincleaner.eu. Security reports: see [SECURITY.md](SECURITY.md).

Part of the Rain family (Rain Cleaner, Rain Driver, RainServer).
