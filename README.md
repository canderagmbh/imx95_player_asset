# i.MX95 Player Setup Guide

### 1. Flash the i.MX95 Board

1. Download the latest NXP BSP:
   [https://www.nxp.com/pages/alpha-beta-bsps-for-microprocessors:IMXPRERELEASES](https://www.nxp.com/pages/alpha-beta-bsps-for-microprocessors:IMXPRERELEASES)

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
