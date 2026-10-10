---
title: Cedar Privacy Policy
---

# Privacy Policy for Cedar

*Last updated: October 9, 2026*

Cedar ("the App", Android package `com.simplejournal.app`) is a private journal. This policy explains exactly what
happens to your information. The short version:

- **Your journal stays on your device.** Entries, photos, moods, tags and settings are stored only in the App's private storage.
- **We have no servers and no accounts.** The developer never receives your journal, your photos, or anything you type.
- **No ads, no analytics SDKs, no tracking.**
- A few optional features rely on Google or your device's built-in services. Each one is described below so you can decide whether to use it.

---

## 1. What is stored on your device

| Data | Where it lives | Leaves the device? |
|---|---|---|
| Journal entries (title, text, date, mood, tags) | Private app database | Only if you export or share it (Section 3.4), or via Android device backup (Section 3.5) |
| Attached photos | Copies in the App's private folder | Same as above |
| Custom moods, theme, font and other preferences | Private app settings | Same as above |
| App Lock PIN or pattern | Stored only as a one-way hash, never in readable form | No |
| Backup password (if you set one) | Never stored. Only a key derived from it is kept, protected by the Android Keystore | No |
| Recently deleted entries | Private app database, for 30 days after you delete them | Not included in exports or backups |
| Reminder settings (time, days) | Private app settings | Same as other preferences |

Streaks, statistics, "days this week", favorites, the daily prompt, "On this day" memories and the "What's new" notes are all
computed and stored on your device from your own entries.

The App uses the Android **system Photo Picker**. It cannot browse your gallery; it only receives the specific photos you choose,
and it copies them into its private folder.

## 2. App Lock is a privacy screen, not encryption

App Lock (PIN, pattern, or biometrics) stops someone who picks up your unlocked phone from opening your journal. It does **not**
encrypt the journal database. Biometric checks are performed by Android; the App never receives your fingerprint or face data.

## 3. Features that involve Google or other apps

### 3.1 Handwriting transcription (on-device)
Recognizing text in a photo of a handwritten or printed note is done **entirely on your device** using Google's ML Kit
text-recognition library, delivered through Google Play services. **Your photos and the recognized text are not sent anywhere.**

The ML Kit library itself sends limited **technical diagnostics** to Google, as described in Google's
[ML Kit data disclosure](https://developers.google.com/ml-kit/android-data-disclosure): device model and OS version, app package and
version, a per-installation identifier, performance timings, feature configuration, and error codes. Google states this data is used for
diagnostics and usage analytics, is encrypted in transit, and is not shared with third parties. It does not include your journal
content. The developer does not receive this data.

### 3.2 Voice dictation
When you tap the microphone, the App asks Android's speech-recognition service (for example, the Google app) to listen and return
text. That service records and processes your voice under **its own** privacy policy and settings, which may include sending audio to
its provider's servers. Cedar only receives the resulting text and never has access to your microphone itself.

### 3.3 Ratings and the free trial (Google Play)
After you finish a couple of entries, the App may show Google Play's own rating sheet. Your rating and review go to Google Play under
Google's terms; the App never sees them, or whether you rated at all. If you start the Cedar Pro free trial, Google Play handles the
subscription and payment details, as with any other purchase (see section 3.6).

### 3.4 Exports, backups and sharing (you control these)
Backups (ZIP) and PDF exports are created **only when you tap Export, Save or Share**, or by automatic backup if you turn it on. When
you save a file to a location you pick, or send it through the Android share sheet (for example to Google Drive or email), the
destination's privacy policy applies.

**Automatic backup (off unless you turn it on).** You choose one backup file with Android's file picker (on your device, in Google
Drive, Proton Drive or any other app the picker offers). After changes to your journal, the App rewrites that file on your device's
behalf; the app that owns the location (for example Google Drive) stores and syncs it under its own privacy policy. The App itself
never connects to those services or to any server. You can turn it off or change the location in Settings at any time.

**Backup protection.** By default a backup file is not encrypted: anyone with a copy can read it, so store and share it with care. In
Settings you can choose a **backup password**. Every backup, manual and automatic, is then encrypted on your device (AES-256) and can be
opened only with that password, which the developer cannot recover or reset. The key derived from your password stays on your device,
protected by the Android Keystore, so automatic backups can run without asking for it.

**Text exports.** Markdown and plain-text exports are ordinary, readable files that you save or share where you choose, like any other export.

### 3.5 Android device backup
If Android's device backup is on, Android includes Cedar's journal, photos and settings in your Google account backup **only when
that backup is end-to-end encrypted**, which Android does when your phone has a screen lock (PIN, pattern or password). Without a
screen lock, Cedar's data is left out of cloud backups. Moving to a new phone with Android's transfer tool also carries the journal
over. You can turn device backup off in your phone's system settings.

### 3.6 Purchases
If you buy Cedar Pro, the payment is processed entirely by Google Play. The developer receives confirmation that a purchase exists, never
your payment details.

### 3.7 Daily reminder (off unless you turn it on)
If you turn on the daily reminder, the App asks Android for permission to show notifications and schedules the reminder with Android's
alarm service on your device. The notification contains a writing prompt only, never anything from your journal, and is marked private so
it is hidden on a locked screen when your phone is set to hide sensitive content. No server is involved. You can turn it off in Settings
or in Android's notification settings at any time.

### 3.8 Importing from other journal apps
"Import from another app" reads an export file that you pick (from Day One, Journey, Daylio, or Markdown and text files) and copies its
entries and photos into your journal on your device. The file is read locally and nothing is sent anywhere. The temporary copy made while
you preview an import is deleted when you finish or cancel.

## 4. Permissions the App uses

| Permission | Why |
|---|---|
| Internet / network state | Added by Google's ML Kit library for its diagnostics (Section 3.1). Cedar's own code makes no network requests. |
| Biometrics (`USE_BIOMETRIC`) | Fingerprint or face unlock for App Lock, if you enable it. |
| Vibration (`VIBRATE`) | Subtle haptic feedback on taps and saves; can be turned off in Settings. |
| Notifications (`POST_NOTIFICATIONS`) | Shows the daily reminder, only if you turn it on; Android asks you first. |
| Background work (`WAKE_LOCK`, `RECEIVE_BOOT_COMPLETED`) | Lets an automatic backup you turned on finish in the background, and re-schedules your reminder after a restart. |

The App does **not** request access to your microphone, photo library, files, contacts, location, camera, or phone state.

## 5. What the developer collects

Nothing. There is no developer-operated server, no account system, no crash reporting, no advertising, and no analytics in the App
other than the Google-library diagnostics described in Section 3.1.

## 6. Keeping and deleting your data

- Delete any entry from the entry editor. It moves to **Settings → Recently deleted**, where you can restore it or delete it for
  good; anything left there is permanently deleted after 30 days.
- Erase everything immediately with **Settings → Delete All Journal Data**.
- Uninstalling the App removes all of its data from your device. Copies you exported, shared, or that are in an Android device backup
  are not affected and must be removed separately.

## 7. Children

The App is not directed at children under 13, and the developer does not collect personal information from anyone.

## 8. Changes to this policy

If this policy changes, the new version will be published at this address with a new "Last updated" date. Material changes will also be
noted in the App's release notes.

## 9. Contact

Questions about this policy or your data: **contact.cedar@pm.me**
