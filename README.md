# Privacy Policy — AutoAudit

**Last updated: July 19, 2026**

AutoAudit ("the App", "we", "us") is a personal finance tracking app published by Adilabz-Orgsec. This policy explains what data the App accesses, how it is used, where it is stored, and what control you have over it.

If anything below doesn't match what you see in the App, please tell us — contact details are at the bottom.

## Summary

- Your financial data (transactions, budgets, accounts) is processed **on your device**. We do not operate a server that stores your transaction history.
- SMS, notification, and call-log content are read **locally to detect and categorize transactions** — this content is never uploaded to us or any third party, except as part of an **encrypted backup you explicitly enable to your own Google Drive**.
- We use Google Firebase and ad-mediation partners for sign-in, crash reporting, analytics, and ads, as detailed below. Where required (EEA/UK/GDPR regions), analytics and crash reporting are **off until you consent**.
- You can delete your account and all associated data at any time, from inside the App or by email.

## Data We Access, and Why

| Data | Why we access it | Where it goes |
|---|---|---|
| **SMS messages** (`READ_SMS`, `RECEIVE_SMS`) | To automatically detect and categorize bank/payment transactions from your bank's SMS alerts | Processed on-device only. Included in your encrypted Drive backup only if backup is enabled. |
| **Notifications** (Notification Listener access) | To detect transactions from your banking and payment apps in real time, as an alternative/complement to SMS | Processed on-device only; not uploaded |
| **Call log** (`READ_CALL_LOG`, optional) | Only if you turn on "Include Call Logs" in Backup settings, to help identify banks/entities that have called you | Included only in your encrypted Drive backup; not accessed otherwise |
| **Contacts** (`READ_CONTACTS`) | To let you pick friends by name when splitting a shared expense | Processed on-device only; used for local name-matching, never uploaded |
| **Camera / photos** | To scan receipts and payment screenshots and extract amounts via on-device OCR (Google ML Kit) | Text extraction happens on-device. Receipt images you save are stored locally (and in your Drive backup, if enabled) |
| **Google account** (Sign-In) | To identify you across devices and, if you choose, to enable Google Drive backup | Handled via Firebase Authentication (Google); we store your Firebase UID, email, display name, and profile photo URL |
| **Advertising ID** | To serve and measure ads via Google AdMob and its mediation partners | Shared with AdMob, AppLovin, and Unity Ads — see "Advertising" below |
| **Device/usage diagnostics** | To fix crashes and understand feature usage | Firebase Crashlytics and Firebase Analytics — gated by consent where required, see "Analytics & Crash Reporting" |

We do **not** access your device location, microphone, or files outside what's described above.

## Where Your Data Lives

- **On your device:** transactions, budgets, categories, accounts, and receipt images are stored in a local database encrypted at rest (SQLCipher). This data never leaves your device unless you enable Google Drive backup.
- **Your Google Drive (optional):** if you enable backup, an encrypted copy of your SMS-derived transaction data, (optionally) call log, and app data is written to a private app folder in **your own Google Drive account** (`appDataFolder`, not visible in your normal Drive file list, not accessible to us or anyone else). The encryption key is stored alongside it, scoped to your Google account. Disabling backup or deleting your account disconnects this; the physical files remain in your Drive until you delete them there, since Google's model doesn't let an app force-delete a user's own Drive files.
- **Our servers:** we do not run a backend database of your financial data. The only server-side data associated with your account is what Firebase Authentication stores for sign-in (UID, email, display name, photo URL) and aggregated, non-identifying analytics/crash data (see below).

## Analytics & Crash Reporting

We use Firebase Analytics and Firebase Crashlytics to understand feature usage and fix bugs.

- If you're in the EEA, UK, or another GDPR-applicable region, both are **disabled by default** until you explicitly consent via the in-app prompt. You can withdraw consent at any time from Settings.
- Outside those regions, analytics is on by default and can be turned off in Settings.

## Advertising

AutoAudit shows ads via Google AdMob, mediated through **AppLovin** and **Unity Ads** to fill inventory. These partners receive your Advertising ID and standard ad-event data (impressions, clicks) to serve and measure ads. We don't share your financial data, SMS content, or contacts with any advertising partner.

## Account Deletion

You can permanently delete your account and data at any time:

- **In the App:** Settings → Account → Delete Account. This immediately wipes your local database, preferences, disconnects Google Drive backup, and deletes your Firebase Authentication record.
- **By email**, if you've already uninstalled the App: **aditya@adilabz.com**, subject "Data Deletion Request - AutoAudit". We purge all cloud-associated data within 7 business days.

Full details: [Account Deletion Request](https://adilabz-orgsec.github.io/autoaudit-policy/)

Note: because backups live in *your own* Google Drive, deleting your account disconnects and stops updating them, but you'll need to manually delete the "AutoAudit_Backup" data from your Drive if you want those specific files gone too.

## Data Security

- Local data is encrypted at rest (SQLCipher / AndroidX Security Crypto).
- All network traffic uses HTTPS/TLS; cleartext traffic is disabled at the OS level.
- Google Sign-In tokens are cryptographically verified server-side before establishing a session.

## Children's Privacy

AutoAudit is not directed at children under 13 (or the minimum age required by your local law), and we do not knowingly collect data from children.

## Your Rights

Depending on your location, you may have rights under GDPR, CCPA, India's DPDP Act, Brazil's LGPD, or similar laws to access, export, correct, or delete your data, and to withdraw consent for analytics/ads. You can exercise most of these directly in the App (Settings → Account/Backup/Privacy) or by contacting us below.

## Changes to This Policy

We'll update this page when what the App collects or does changes, and update the "Last updated" date above. Material changes will be reflected in the App's release notes.

## Contact

Adilabz-Orgsec — **aditya@adilabz.com**
