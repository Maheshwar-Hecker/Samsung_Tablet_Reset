# Samsung_Tablet_Reset

# Step-by-Step Guide: Removing Government Restrictions \& Resetting a Samsung Tab A9 (Android 15)

*This markdown file distills the full Hindi video (YouTube ID: k7afFwA6ePk) into concise, reproducible instructions. All apps mentioned below should already be sideloaded on the tablet unless noted otherwise.*

***

## Prerequisites

1. **Device**: Samsung Galaxy Tab A9 running Android 15 (One UI 7) with government management (Knox/UPDESCO profile).
2. **Apps you must have installed (APKs already copied via USB/SD-card):**
    - Shizuku
    - aShell (aka “ASL”)
    - Canta (aka “CTA”)
    - Hail (aka “Hail Freezer”)
    - Alliance Shield X
3. Stable Wi-Fi network.

***

## 1. Enable Developer Options \& Wireless ADB

1. Go to Settings → About Tablet → Software Information.
2. Tap **Build number** 7 times, enter your lock-screen PIN if asked.
3. Back out to Settings; open **Developer options** (now visible).
4. Scroll to Debugging section:
    - Turn **USB debugging** ON.
    - Turn **Wireless debugging** ON → confirm “Allow on this network”.

***

## 2. Pair Shizuku via Wireless ADB

1. Launch **Shizuku** → tap **Pairing**.
2. Grant the “notification access” permission when prompted, then return.
3. Back in Developer options → Wireless debugging → **Pair device with pairing code**.
4. A 6-digit code appears in a system notification (“Pairing service found”).
5. Tap the notification, enter the pairing code, press **Send**.
6. “Pairing successful” toast should appear.
7. Re-open Shizuku → press **Start** → wait 2-3 s until the app auto-closes.
8. Open Shizuku again; confirm status shows **Authorized** with 0 apps.

***

## 3. Authorize aShell \& Canta inside Shizuku

1. In Shizuku home screen tap **Authorized apps (0)**.
2. Check both **aShell** and **Canta**, then hit **Allow**.

***

## 4. Disable First Knox Agent with aShell

1. Open **aShell** and press **Start** to get an ADB shell prompt.
2. Paste the command below and hit the **GO** (paper-plane) button:
```
pm disable-user --user 0 com.sec.knox.kccagent
```

3. Toast “Package com.sec.knox.kccagent new state: disabled” should appear.

***

## 5. Disable Second Knox Package with Canta

1. Open **Canta**. Dismiss the warning → *Don’t show again* → **Proceed**.
2. Tap the search icon and type **knox**.
3. From the list tick **com.sec.enterprise.knox.cloudmdm.smdms** (Knox Enrollment Service).
4. Tap the trash icon → **OK** to uninstall the package.
*If uninstall fails, choose the freeze/disable toggle instead.*

***

## 6. Factory-Reset the Tablet

1. Go to Settings → General Management → Reset.
2. **Factory data reset** option is now unlocked; tap it → **Delete all**.
*If Samsung Account blocks the reset, follow the hardware-key method:*
    - Power the tablet **off**.
    - Plug USB-C cable into another Samsung device or PC (leave tablet end connected).
    - Hold **Power + Volume Up**. Release **Power** on first Samsung logo, keep holding **Volume Up** until Recovery.
    - In Recovery navigate with volume keys: **Wipe data/factory reset** → **Factory data reset** → **Reboot system now**.

The tablet reboots clean but still carries a “work profile” placeholder.

***

## 7. Create Alliance Shield Owner Profile (QR Provisioning)

*Perform on a second phone/PC while the fresh-reset tablet sits at the “Welcome” screen.*

1. Register an Alliance Shield X account at `alliancex.org/ucp.php?mode=register`.
2. Confirm email; keep username \& password handy.
3. Open the Alliance QR setup page (first QR code).
4. On the tablet’s Welcome screen tap anywhere **5-6 times** → hidden QR scanner opens.
5. Scan the first QR. When prompted, connect to Wi-Fi.
6. Device downloads work-profile files; wait.
7. When asked “Use only Shield?”, pick **Use only the Shield** → **Continue**.
8. Sign in with Alliance credentials → **Next** → **Finish**. Alliance Shield X owner mode is now active.

***

## 8. Disable Remaining Knox Enrollment via Alliance Shield

1. Inside Alliance Shield tap **App Manager** → search “knox”.
2. Select **com.sec.enterprise.knox.cloudmdm.smdms** (Enrollment Service).
3. Tap **Disable**. Message “Enrollment Service was disabled” confirms success.

***

## 9. Remove Alliance Shield Ownership Safely

Still inside Alliance:

1. Tap **Settings** → toggle **Device Owner** OFF → confirm **Yes**.

Alliance can now be uninstalled, but first freeze its Knox fallback.

***

## 10. Freeze Enrollment Service with Hail Freezer

1. Re-enable Shizuku pairing if the factory reset cleared it (repeat Section 2).
2. Open **Hail** → **Settings** → **Working mode** → choose “Shizuku disable”.
3. Grant permission → back.
4. Tap **Apps** → overflow button → enable **System apps** → **Continue**.
5. Search **knox** → tick **com.sec.enterprise.knox.cloudmdm.smdms**.
6. Return to home, locate the package entry, press **Freeze**.
Grey icon indicates the agent can no longer auto-reactivate.

***

## 11. Clean-Up

1. Uninstall **Alliance Shield X**, **Shizuku**, **aShell**, **Canta**, **Hail** (optional).
2. Reboot once more to verify no Device-Admin or Owner apps remain:
Settings → Security \& privacy → Device admin apps → list should be **empty**.
3. Enjoy a fully unrestricted Samsung Tab A9. Avoid future factory resets unless you plan to run the whole procedure again.

***

## Important Notes

- **Do not** update system firmware if Samsung later patches Shizuku or disables wireless debugging without USB; confirm community feedback first.
- If you accidentally reset the device later, the Knox profile will re-enroll; re-run this guide from scratch.
- Keep original APKs and this markdown safely stored (GitHub, local PC) for reuse.

<div style="text-align: center">⁂</div>

[^1]: https://www.youtube.com/watch?v=k7afFwA6ePk

