# Samsung_Tablet_Reset

# 🚀 Step-by-Step Guide: Removing Government Restrictions & Resetting a Samsung Tab A9 (Android 15)

*This guide condenses the Hindi video ([YouTube ID: k7afFwA6ePk](https://www.youtube.com/watch?v=k7afFwA6ePk)) into reproducible steps.*  

---

## 📋 Prerequisites

| ✅ | Item |
|----|------|
| 📱 | **Device:** Samsung Galaxy Tab A9 (Android 15/One UI 7) |
| 📦 | **APKs already sideloaded:** Shizuku 🫧 · aShell 🐚 · Canta 🎼 · Hail ❄️ · Alliance Shield X 🛡️ |
| 📶 | Stable Wi-Fi connection |

---

## 🔧 1. Enable Developer Options & Wireless ADB

1. ⚙️ **Settings → About Tablet → Software Information**.  
2. 🖐️ Tap **Build number** *7* times → enter PIN.  
3. ↩️ Back to **Settings** → open **Developer options**.  
4. In **Debugging**:  
   - ☑️ Toggle **USB debugging** ON.  
   - ☑️ Toggle **Wireless debugging** ON → *Allow on this network*.

---

## 🫧 2. Pair Shizuku via Wireless ADB

1. Open **Shizuku** → hit **Pairing** 🔗.  
2. Grant **notification access**.  
3. Developer options → **Wireless debugging → Pair device with pairing code** 🔢.  
4. Enter 6-digit code → **Send**.  
5. ✅ “Pairing successful” toast appears.  
6. Back in Shizuku → **Start** ▶️ → reopen to confirm **Authorized**.

---

## 🐚 3. Authorize aShell & Canta

1. Shizuku → **Authorized apps**.  
2. ☑️ Tick **aShell** & **Canta** → **Allow**.

---

## 🚫 4. Disable First Knox Agent with aShell

1. Launch **aShell** → **Start**.  
2. Paste:

```

pm disable-user --user 0 com.sec.knox.kccagent

```

3. ✅ Toast confirms **disabled**.

---

## 🎼 5. Disable Second Knox Package with Canta

1. Open **Canta** → *Proceed* 👉.  
2. 🔍 Search **knox**.  
3. ☑️ Select **com.sec.enterprise.knox.cloudmdm.smdms**.  
4. 🗑️ Tap **Uninstall** (*or* freeze 🧊 if uninstall fails).

---

## 🏭 6. Factory-Reset the Tablet

1. **Settings → General Management → Reset → Factory data reset** 🔄 → **Delete all**.  
2. 💡 If blocked, use **hardware keys**:  
- Power off ⏻.  
- Hold **Power + Vol Up** while USB-C is tethered.  
- In Recovery: **Wipe data/factory reset → Reboot system now**.

---

## 🛡️ 7. Create Alliance Shield Owner Profile (QR Provisioning)

1. Register at Alliance Shield X 🌐.  
2. On fresh tablet **tap Welcome screen 5-6×** to open QR scanner 📷.  
3. Scan first Alliance QR → connect Wi-Fi.  
4. Choose **Use only the Shield** → sign in → **Finish** ✅.

---

## 📴 8. Disable Remaining Knox Enrollment via Alliance Shield

1. Alliance Shield X → **App Manager** → search **knox**.  
2. Select **Enrollment Service** → **Disable** 🚫.

---

## 🔓 9. Remove Alliance Shield Ownership

1. Alliance **Settings → Device Owner OFF** → **Yes** ✔️.

---

## ❄️ 10. Freeze Enrollment Service with Hail Freezer

1. Re-pair Shizuku if needed.  
2. Hail **Settings → Working mode → "Shizuku disable"**.  
3. **Apps → System apps ON**.  
4. Freeze **com.sec.enterprise.knox.cloudmdm.smdms** 🧊.

---

## 🧹 11. Clean-Up

- 🗑️ Uninstall auxiliary apps (Alliance, Shizuku, aShell, Canta, Hail) if desired.  
- 🔁 Reboot → **Settings → Security & privacy → Device admin apps** should be **empty**.  
- 🎉 Enjoy a fully unrestricted Samsung Tab A9!

---

## ⚠️ Important Notes

- Avoid OTA updates until community confirms Shizuku & Wireless ADB still work.  
- A future factory reset will re-enroll Knox; rerun this guide then 🔁.

<div style="text-align: center">⁂</div>


