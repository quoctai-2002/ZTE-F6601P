# ZTE F6601P TOOLBOX

⚡ **All-in-One Unlock & Configuration Tool for ZTE F6601P Modem**

Created by **Nguyễn Đình Quốc Tài**  
📧 nguyendinhquoctai@gmail.com  
🔗 [fb.com/NguyenDinhQuocTai](https://www.facebook.com/NguyenDinhQuocTai)

---

## ✨ Features

### 🔓 UNLOCK TELNET
- Auto MAC spoofing (required for exploit)
- One-click Telnet unlock using zteOnu
- Auto credential extraction
- Auto-connect to Telnet after unlock

### ⚙️ CONFIGURATION (setmac)
- **Load From Modem**: Automatically read current config via `setmac show2`
- **Generate Commands**: Create setmac commands for:
  - Identity (SN, Vendor, GPON SN/Password, OUI, REG_ID)
  - MAC addresses (256-263, auto +1)
  - WiFi 2.4GHz & 5GHz (SSID & Password)
  - Admin passwords
  - Region (Viettel, VNPT, FPT, Cambodia)

### 🛠️ TOOLS
- **Fix Reboot**: Disable OMCI Watchdog, TR-069, Auto-Upgrade
- **Bridge Mode**: Enable pass-through mode
- **Memory Check**: Run `free` command
- **NVRAM Info**: Run `setmac show2`

### 💻 BUILT-IN TERMINAL
- Telnet terminal with command input
- Paste Config: Auto-send all generated commands
- Real-time output display

---

## 📋 Requirements

- Windows 10/11
- Administrator privileges (for MAC spoofing)
- Ethernet connection to modem (not WiFi)

---

## 🚀 Usage

### Step 1: Connect Hardware
- Connect PC to modem via **LAN cable** (not WiFi)
- Disconnect fiber optic cable (optional but recommended)

### Step 2: Unlock Telnet
1. Select correct Network Adapter (Ethernet/LAN)
2. Enter Modem IP (usually `192.168.1.1`)
3. Enter GPON SN (from modem label, e.g., `ZTEGXXXXXXXX`)
4. Click **AUTO UNLOCK**
5. Wait ~25 seconds (MAC spoof → exploit → restore)

### Step 3: Configure
1. Click **Load** to read current config from modem
2. Modify values as needed
3. Click **GENERATE COMMANDS**
4. Click **Paste Config** to send commands to modem

### Step 4: Fix Reboot Issues (Important!)
If modem keeps restarting after config changes:
1. Click **Fix Reboot** in Tools section
2. Click **Paste Config** to send fix commands
3. Wait for reboot

---

## ⚠️ Important Notes

1. **Run as Administrator** - Required for MAC spoofing
2. **Use LAN connection** - WiFi will NOT work
3. **Run FIX REBOOT first** - Before changing identity to prevent restart loops
4. **Backup original config** - Use `setmac show2` before making changes
5. **Don't change SN without matching MAC/OUI** - Will cause issues

---

## 🔧 Troubleshooting

### "Connection refused" during unlock
- Check modem IP is correct
- Ensure LAN cable is connected
- Try port 80 (default) or 8080

### "Network unreachable" during Telnet
- Select correct adapter (not WiFi)
- Wait for network to stabilize after MAC restore

### Modem keeps restarting
1. Connect via Telnet quickly after boot
2. Run FIX REBOOT commands immediately
3. Wait for save and reboot

---

## 📁 Files

- `ZTE_AIO_v27.exe` - Main tool
- `zteOnu_new.exe` - Exploit tool (bundled)
- `README.md` - This file

---

## 📜 License

This tool is provided for educational purposes only.  
Use at your own risk. The author is not responsible for any damage.

---

**Version**: v27  
**Last Updated**: January 2026
