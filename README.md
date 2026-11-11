
# sing-box rules – ad, tracker & adult-content blocker

A ready-to-use configuration for the **sing-box** app that blocks ads, trackers,
telemetry and adult websites on your iPhone, iPad, Mac, Windows PC or Android device.
Block lists are updated automatically every night.

---

> ## ⚠️ **Important: pause sing-box before system updates**
>
> **Before you install a new iOS, iPadOS or macOS version (or any big system update),
> stop sing-box in the app. Start it again after the update has finished.**
>
> **sing-box filters all network traffic, which can slow down or interrupt large
> update downloads.**

---

## What does it do?

sing-box runs as a **local VPN** directly on your device. Unlike a normal VPN, your
traffic does **not** go through any external server. It stays on your own internet
connection, and sing-box filters it before it leaves your device.

- 🚫 **Blocks ads and trackers** in apps and browsers (HaGeZi Pro + ad lists)
- 🔞 **Blocks adult websites** (SagerNet adult category list)
- 🔒 **Encrypted DNS** through [Quad9](https://quad9.net) (DNS-over-HTTPS), so your
  internet provider can't see or change your lookups
- 🧲 **Blocks BitTorrent** traffic
- 🔄 **Updates itself**: block lists are refreshed every night at 04:00, and devices
  download them automatically

Note: it does **not** hide your IP address or location. It's a filter, not an
anonymity VPN.

---

## 1. Install the sing-box app

| Device | Download |
|---|---|
| **iPhone / iPad / Apple TV** | [App Store – sing-box MT](https://apps.apple.com/app/sing-box-mt/id6785326793) (iOS 15+) |
| **Mac** | [GitHub Releases](https://github.com/SagerNet/sing-box/releases) (standalone "SFM" app, macOS 13+) or Homebrew: `brew install sfm` |
| **Windows** | [GitHub Releases](https://github.com/SagerNet/sing-box/releases) – sing-box for Desktop (Windows 10+) |
| **Android** | [Google Play](https://play.google.com/store/apps/details?id=io.nekohasekai.sfa) · [F-Droid](https://f-droid.org/packages/io.nekohasekai.sfa/) · [GitHub Releases](https://github.com/SagerNet/sing-box/releases) |

Official client overview: [sing-box.sagernet.org/clients](https://sing-box.sagernet.org/clients/)

> The old App Store app **"sing-box VT"** is no longer updated. Please install
> **"sing-box MT"** instead.
>
> Please always use the **latest app version**. These configs need sing-box 1.14 or newer.

---

## 2. Choose your config

Both versions block ads, trackers and adult websites. The only difference:

| Version | pornhub.com | Link |
|---|---|---|
| **Standard (v18)** | not blocked | [sing-box-v18.json](https://raw.githubusercontent.com/alienthrone/sing-box-rules/main/config/sing-box-v18.json) |
| **Strict (v18 strict)** | blocked | [sing-box-v18-strict.json](https://raw.githubusercontent.com/alienthrone/sing-box-rules/main/config/sing-box-v18-strict.json) |

👉 **Recommended for children's devices: Strict.**

---

## 3. Set it up

1. Right-click (or long-press) the link of your chosen version → **Copy Link**.
2. Open the sing-box app → **Profiles** → **New Profile**
   - **Type:** Remote
   - **URL:** paste the link
   - **Auto Update:** on
3. Save, select the new profile and tap **Start**.
4. Allow the VPN permission when your device asks.

The profile updates itself automatically.
**Please don't edit its content in the app**: changes are overwritten at the next
update. To switch between Standard and Strict, create a new profile with the other link.

---

## Rule sets (used automatically by the configs)

You don't need to download these yourself. They're listed here for reference.

| File | Content | Updated |
|---|---|---|
| [ads.srs](https://raw.githubusercontent.com/alienthrone/sing-box-rules/main/rules/ads.srs) | Ad domains (SagerNet geosite) | nightly |
| [hagezi.srs](https://raw.githubusercontent.com/alienthrone/sing-box-rules/main/rules/hagezi.srs) | Ads, trackers, telemetry (HaGeZi Pro) | nightly |
| [adult.srs](https://raw.githubusercontent.com/alienthrone/sing-box-rules/main/rules/adult.srs) | Adult websites (SagerNet geosite) | nightly |
| [alien-block.srs](https://raw.githubusercontent.com/alienthrone/sing-box-rules/main/rules/alien-block.srs) | Custom block list | on every change |

---

## Troubleshooting

- **A website or app doesn't work properly?** Stop sing-box, try again, and tell me
  which site it was, so it can be checked.
- **Internet very slow or not working at all?** Stop and restart sing-box. If that
  doesn't help, restart the device.
- **During system updates:** see the warning at the top. Pause sing-box first.
