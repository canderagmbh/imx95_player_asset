# Digital Twin of 3D SUV Demo with Candera CGI Studio

This is a high-fidelity Digital Twin demonstration of a 3D SUV for Automotive In-Vehicle Information Display (IVI) systems. This demo runs on the **Toradex i.MX 95 Verdin Evaluation Kit** with an FHD display supporting touch control, developed using **Candera CGI Studio** and based on the **NXP BSP**.

![Demo Preview](docs/images/demo-preview.png)
*Screenshot of the 3D SUV Digital Twin Demo*

---

## Table of Contents

- [Software](#software-requirements)
- [Hardware](#hardware-requirements)
- [Setup](#setup)
- [License](#license)
- [FAQs](#faqs)
- [Support](#support)
- [Release Notes](#release-notes)
- [Create Your Own HMI Project with CGI Studio](#create-your-own-hmi-project-with-cgi-studio)

---

## Software Requirements

- **NXP BSP** for i.MX 95

## Hardware Requirements

- **Toradex Verdin i.MX 95 Evaluation Kit** [https://www.toradex.com/computer-on-modules/verdin-arm-family/nxp-imx95-evaluation-kit](https://www.toradex.com/computer-on-modules/verdin-arm-family/nxp-imx95-evaluation-kit)
- **FHD Display (1920x1080)** with touch support
- Power adapter (as per board specification)
- USB keyboard/mouse (for setup/debug)
- Ethernet cable 

## Setup

In this sectiion we will setup the CGI Studio Player for the i.MX95 target and show you how to run the HMI application (Asset). 

### 1. Flash the i.MX95 Board

1. Download the latest NXP BSP:
   [IMXPRERELEASES](https://www.nxp.com/pages/alpha-beta-bsps-for-microprocessors:IMXPRERELEASES)

2. Flash the board using the standard NXP procedure.

3. Boot the device and ensure Linux starts correctly and **Weston** is running.

### 2. Connect via SSH

```bash
ssh root@<device-ip>
```

### 3. Upload Player and Asset Files

Upload `Player` and `Asset.bin` to the device (e.g. via **WinSCP** or `scp`).

### 4. Set Execute Permissions

On the device, navigate to the directory where you uploaded the files and make the Player binary executable:

```bash
chmod +x Player
```

### 5. Run the Player

Start the application with:

```bash
./Player Asset.bin
```

### 6. Optional: Disable Weston Side Panel

If you don't like the side panel (launcher bar) in Weston, you can disable it by editing the Weston configuration file:
```
/etc/xdg/weston/weston.ini
```

## License

The software provided by CANDERA under this agreement or otherwise (the “Demo Software”) is supplied solely for evaluation and demonstration purposes. The Demo Software consists of (i) a precompiled player executable (the “Player”) and (ii) associated binary assets containing HMI/GUI content (the “Assets”).

The Demo Software is provided exclusively in object code form and solely for execution on the specific hardware platform(s) designated by CANDERA. Licensee is granted a limited, non-exclusive, non-transferable, revocable right to use the Demo Software strictly for internal evaluation and demonstration purposes on such designated hardware platform(s).

Licensee shall not, and shall not permit any third party to:
- use the Demo Software on any hardware platform other than the designated platform(s);
- use the Player to execute any assets other than the Assets provided by CANDERA;
- use the Demo Software for production, commercial, or product development purposes;
- modify, adapt, reverse engineer, decompile, or otherwise attempt to derive the source code of the Demo Software, except to the extent permitted by mandatory law.
All rights, title, and interest in and to the Demo Software, including all intellectual property rights, remain exclusively with CANDERA GmbH. No rights are granted to Licensee other than those expressly set forth herein.

THE DEMO SOFTWARE IS PROVIDED “AS IS” AND “AS AVAILABLE”, WITHOUT WARRANTIES OF ANY KIND, WHETHER EXPRESS, IMPLIED, OR STATUTORY, INCLUDING BUT NOT LIMITED TO WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, NON-INFRINGEMENT, OR ERROR-FREE OPERATION. CANDERA SHALL HAVE NO LIABILITY WHATSOEVER ARISING OUT OF OR IN CONNECTION WITH THE USE OF THE DEMO SOFTWARE.

---

## FAQs

Common questions

<details>
<summary><strong>Q1: Which display resolutions are supported?</strong></summary>

Primarily validated on **1920x1080 (FHD)**. 

</details>

<details>
<summary><strong>Q2: Does the demo support multitouch gestures?</strong></summary>

Yes. Supported gestures: tap, swipe, pinch

</details>

<details>
<summary><strong>Q3: Why is my touch input not recognized?</strong></summary>

Please ensure that the cable for touch input (USB) is properly connected to the board.

</details>

---

## Support

If you have further questions, please reach out to us via the following channels or file an issue as bug report in our github repository.

### Contact Channels

- **Candera Support:** [Webform](https://www.candera.eu/contact/)
- **Email:** office@candera.eu

### Bug Report Template
[Candera Github Repository](https://github.com/canderagmbh/imx95_player_asset/)

```markdown
**Environment**
- Board: Verdin i.MX 95
- BSP Version:
- Display Model:

**Issue Description**
<what happened?>

**Steps to Reproduce**
1. ...
2. ...
3. ...

**Expected Behavior**
<what should happen?>

**Logs/Screenshots**
<attach here>
```

---

## Release Notes

Notable updates per version.

### `v0.1.0`

- Initial Digital Twin 3D SUV demo integration
- FHD touch display validation on Toradex i.MX 95 Verdin EVK

---

## Create Your Own HMI Project with CGI Studio

Would you like to experience CGI Studio firsthand?
We offer a free 30-day trial to potential professional CGI Studio users. Complete the form to request a trial.
[Request your trial version now](https://cgistudio.at/trial)

---



