# Google-Hypervisor-Manager

## **Before you read, I don't work for Google. this software isnt affiliated with them in any way, this is simply a manager for the Google Emulator that Android Studio uses.**

A lightweight manager for the **Android x86 emulator** provided by Google, written in **Python**.

* **No admin privileges required**
* Designed to work cleanly with Google’s official emulator + ADB tooling

---

## Installing APKs (ADB)

### 1. Download ADB (Platform Tools)

Download the official Android Platform Tools here:

* [https://dl.google.com/android/repository/platform-tools-latest-windows.zip](https://dl.google.com/android/repository/platform-tools-latest-windows.zip)

Extract the ZIP somewhere convenient.

---

### 2. Open a Terminal in the Platform Tools Folder

You can do this in either of these ways:

* **Right‑click inside the folder** → *Open in Terminal* (PowerShell)
* Or open CMD / PowerShell and `cd` into the folder manually

---

### 3. Install an APK

Run the following command:

```
adb install "FULL_PATH_TO_APK"
```

Example:

```
adb install "C:\Users\Partvision\Downloads\GeometryDash_2.207_b40.apk"
```

---

### Common PowerShell Error (Important)

If you see an error like:

> *The command adb was not found, but does exist in the current location*

That’s **PowerShell being annoying**, not ADB being broken.

Fix it by running:

```
.\adb install "FULL_PATH_TO_APK"
```

Example:

```
.\adb install "C:\Users\Partvision\Downloads\GeometryDash_2.207_b40.apk"
```

This is required because PowerShell does **not** execute local binaries by default.

---

### Notes

* Make sure the emulator is **running** before installing APKs
* `./adb` is for Unix-like shells — **Windows PowerShell uses `.\adb`**
* If ADB can’t see your emulator, run:

```
adb devices
```

---

That’s it. If this breaks, it’s almost always PATH, PowerShell, or the emulator not running — not the APK.

<img width="1096" height="767" alt="image" src="https://github.com/user-attachments/assets/83b5d083-66b0-4d83-904b-be4b24d6f28a" />

<img width="793" height="546" alt="image" src="https://github.com/user-attachments/assets/230e4507-4b83-4116-a082-ec70605f8831" />


