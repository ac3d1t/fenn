# fenn — installation guide

## macOS

### step 1 — download

go to the [releases page](https://github.com/ac3d1t/fenn/releases) and download the `.dmg` file for your version.

**which version should i download?**
obviously the newest release you silly goof
- **v1.0.2** is the wesion where you can just download it from the website. easy peasy
- **v1.0.3** has extra features (keyboard shortcuts, persistent settings) but you cant get it off the website for some ridiculous reason. download it from the repo if you want it that bad.

### step 2 — open the dmg

once the download finishes, open the `.dmg` file from your downloads folder. a window will pop up showing the fenn icon and an arrow pointing to your applications folder.

drag the fenn icon onto the applications folder.

### step 3 — first launch

open your applications folder and double-click fenn.

**if you see "fenn cannot be opened because it is from an unidentified developer":**

this happens because fenn isn't signed with an apple developer certificate. to get around it:

1. go to **system preferences** (or system settings on macOS 13+)
2. click **privacy & security**
3. scroll down until you see a message that says `"fenn" was blocked from use because it is not from an identified developer`
4. click **open anyway**
5. a popup will appear asking if you're sure — click **open**

you only have to do this once. after that fenn opens normally.

**alternative method:**
right-click (or control-click) the fenn app in your applications folder and select **open** from the menu. this bypasses the security warning directly.

### step 4 — you're in

fenn opens with a sidebar on the left and the browser on the right. type in the search bar to search or navigate to a URL.

---

## iOS (sideloading)

sideloading means installing an app without going through the app store. apple allows this with a free apple ID, but free accounts need to re-sign the app every 7 days. tools like AltStore automate this for you.

you'll need:
- an iPhone or iPad running iOS 14.0 or later
- a computer (mac or windows) for the initial setup
- a free apple ID

### option 1 — AltStore (recommended)

AltStore is the easiest way to sideload. it runs in the background on your computer and automatically re-signs fenn before it expires.

**on your computer:**

1. go to [altstore.io](https://altstore.io) and download AltServer for your OS (mac or windows)
2. install and open AltServer — it'll sit in your menu bar or system tray
3. connect your iPhone to your computer via USB
4. click the AltServer icon → **install AltStore** → select your iPhone
5. enter your apple ID and password when prompted (this is only used locally to sign apps, apple does not receive it)
6. AltStore will install on your iPhone

**on your iPhone:**

7. go to **settings** → **general** → **VPN & device management**
8. find your apple ID under "developer app" and tap it
9. tap **trust** and confirm — this lets apps signed with your apple ID run on your device
10. open AltStore on your iPhone
11. download the fenn IPA from [fenn-ios releases](https://github.com/ac3d1t/fenn-ios/releases/download/v1.0.3-ios/fenn.ipa)
12. once downloaded, tap the share button → scroll through the share sheet and tap **open in AltStore**
13. AltStore will install fenn

**keeping fenn alive:**
AltStore re-signs apps automatically as long as your iPhone and computer are on the same wifi network and AltServer is running. you don't have to do anything.

---

### option 2 — Sideloadly

Sideloadly is simpler to set up but requires you to manually re-sign every 7 days.

1. download [Sideloadly](https://sideloadly.io) for your computer
2. install and open it
3. connect your iPhone to your computer via USB
4. trust the computer on your iPhone if prompted
5. download the fenn IPA from [fenn-ios releases](https://github.com/ac3d1t/fenn-ios/releases/download/v1.0.3-ios/fenn.ipa) or [fenn releases (in this repository)] 
6. drag the IPA file into the Sideloadly window or manually select it by pressing the IPA file icon and locating it in your file explorer (usually in downloads)
7. enter your apple ID in the account field
8. click **start**
9. enter your apple ID password when prompted
10. wait for it to finish — fenn will appear on your home screen

**after installing:**
go to **settings** → **general** → **VPN & device management** → tap your apple ID → tap **trust**

fenn will now open. re-sign it with Sideloadly every 7 days to keep it working.

---

### option 3 — TrollStore

if your device and iOS version are compatible with TrollStore, this is by far the best option. apps installed with TrollStore never expire and don't need re-signing.

check if your device is compatible at [github.com/opa334/TrollStore](https://github.com/opa334/TrollStore)

if compatible:
1. install TrollStore using the instructions for your specific iOS version
2. download the fenn IPA from [fenn-ios releases](https://github.com/ac3d1t/fenn-ios/releases/download/v1.0.3-ios/fenn.ipa) or [fenn releases (in this repository)]
3. open the IPA file on your device
4. tap **open in TrollStore**
5. tap **install**

done. fenn is installed permanently with no expiry.

---

## android

fenn is available as an APK for android. no account needed, no expiry — just download and install.

requires android 7.0 or later.

### step 1 — enable unknown sources

android blocks installs from outside the play store by default. you need to allow it once:

**android 8.0 and later:**
1. go to **settings** → **apps**
2. tap **special app access**
3. tap **install unknown apps**
4. find your browser or files app and toggle **allow from this source**

**android 7.0:**
1. go to **settings** → **security**
2. toggle on **unknown sources**
3. tap ok on the warning

### step 2 — download the APK

download fenn.apk from the [fenn-ios releases page](https://github.com/ac3d1t/fenn-ios/releases/latest) or [fenn releases (in this repository)]

### step 3 — install

1. open your downloads folder
2. tap `fenn.apk.zip`
3. unzip the file by long pressing it and finding the unzip option in the dropdown
4. tap **install**
5. tap **open** when it finishes

no re-signing, no expiry, no account needed.

---

## troubleshooting

**macOS: app says it's damaged and can't be opened**

open terminal and run:
```
xattr -cr /Applications/fenn.app
```
then try opening it again.

**macOS: fenn won't open after update**

delete the old version from your applications folder first, then install the new one fresh.

**iOS: app crashes immediately after opening**

make sure you've trusted the developer certificate in settings → general → VPN & device management. if you already did, try re-signing with AltStore or Sideloadly. if this doesnt work, try updating your device. the app only works on iOS 14+.

**iOS: "app is no longer available"**

your 7-day signing period expired. re-sign the app using AltStore or Sideloadly.

**iOS: can't find the IPA after downloading**

the IPA file should be in your downloads folder. if safari downloaded it, go to the Files app → downloads → look for fenn.ipa. then tap and hold → share → open in AltStore or Sideloadly.

---

## support

if you run into issues not covered here, open an issue on the [github repo](https://github.com/ac3d1t/fenn/issues) or reach out directly. [chrispy1331@gmail.com]

if fenn has been useful, a coffee is always appreciated — [buymeacoffee.com/ac3d1t](https://buymeacoffee.com/ac3d1t)
