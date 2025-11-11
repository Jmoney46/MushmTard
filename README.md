# MushTard Installer jargon

Hola, I am retard, and the other day I was using murkmod and some fellow peers of mine were like "Dude, you are so retarded, we gotta make mushm where it is only safe stuff so you don't fuck shit." Then that got me thinking, so when I got home I created "MushTard," which is a retarded version of their "mushm," and now this is for all those peeps that are retarded and you know will screw their shit if not monitored, hence me making MushTard.

> [!WARNING]
> **This will replace your current Mush installation** with the Nonagon-modified-Jmoney-modified version.  
> Back up any important data before continuing.
> Also, if you have a friend who knows how to do this that is smart HAND THE COMPUTER TO THEM!

---

## Installation

Run the following command as **root** to install the de-modified version of mush

```bash
bash <(curl -fsSL https://raw.githubusercontent.com/Jmoney46/MushTard/refs/heads/main/installer.sh)
```
---

## Fixes

### Fix for "Can't Install MushTard" (Read-Only File System)

If you're seeing a "Read-Only" (RO) file system error when trying to install **MushmTard** or any other package on Chrome OS, follow the steps below to fix it.

#### Step 1: Remount Root as Read-Write

1. Open **V2 Shell**.
2. Log in as root.
3. Run the following command to remount the root file system with read-write access:

   ```bash
   sudo mount -o remount,rw /
   ```
3.1 If no reply, reboot and proceed to installation

3.2 If it replies with RO(Read Only) file system Procead to step 4

4. Run the following command to fix the RO error:

```bash
# replace /dev/mmcblk1p5 with the directory from step 3
e2fsck -f /dev/mmcblk1p5
```

5. Reboot and proceed to installation

