---
layout: default
title: "Privacy Policy"
---

# Privacy Policy for AIO

**Publisher:** AppForge  
**App:** AIO (`com.appforge.aio`) — Android & iOS  
**Contact:** appforge91@gmail.com  
**Last updated:** 16 November 2026

## 1. Summary

AIO is a local-first personal organizer. Your notes and media are stored on your device.

If you turn on backup, encrypted copies go to your Google Drive app-data folder.

On Android, AIO may send limited onboarding analytics to Meta (Facebook App Events). Optional AIO Premium uses Google Play Billing via RevenueCat. Reminders are primarily scheduled on your device; in some builds they may also use Firebase Cloud Messaging for delivery.

We do not show display ads. We do not sell your personal data. We do not include a crash-reporting SDK (such as Crashlytics or Sentry). Optional feedback is sent only if you email us.

## 2. Data Stored on Your Device

Depending on what you create, AIO may store:

- Text notes, expenses, book reviews, and similar content you enter.
- Photos (product dates, business cards, book reviews) and voice recordings.
- Business-card details you scan or type (name, company, phones, email, website, address, OCR text) — including details about other people.
- Links you save, plus preview title/description/image fetched for those links.
- Subscription **reminder** titles/dates and manually entered reminder names (not your phone’s address book). These reminder notes are separate from optional **AIO Premium** (paid app subscription).
- Content you share into AIO from other apps (text, links, audio).
- App preferences and backup status (including your Google account email if you enable backup).
- On Android, a Meta anonymous identifier used for App Events.
- When Premium / monetization is active on Android: a RevenueCat anonymous app user ID (and related entitlement state).
- When remote reminder delivery is enabled: a Firebase anonymous user ID, FCM device token, timezone, app flavor/platform metadata, and schedule timing metadata (note/item IDs, rules, next fire times — not reminder title or body text).

We do not access your device contacts list or your location sensors.

## 3. Optional Google Sign-In & Drive Backup

Backup is optional. If you sign in with Google, AIO requests access to Google Drive app data only.

Notes and media are encrypted on your device with Argon2id key derivation and AES-256-GCM before upload.

AppForge cannot read your encrypted backup contents. Google cannot read the encrypted note contents either, but Google still processes your Google account identity and stores the encrypted files (and vault setup parameters such as salt in a plaintext vault metadata file) under your account, subject to Google’s policies.

Your Google account email may be stored locally on the device for backup status.

When monetization is enabled, backup may require AIO Premium.

You are responsible for keeping your passphrase and recovery key safe. Losing both means the backup cannot be recovered.

## 4. Permissions

- **Camera / photos** — product dates, business cards, book reviews.
- **Microphone** — voice notes.
- **Notifications / alarms** — reminders. By default these are scheduled locally on your device. In builds where remote reminder delivery is enabled, Google Firebase Cloud Messaging may also be used to wake the app and show reminders. Reminder text may appear on your lock screen and can include names or titles you entered.
- **Internet** — backup, link previews, store billing, analytics/attribution SDKs, and (when enabled) remote reminder delivery.
- **Android advertising ID** — may be collected by Meta and/or RevenueCat for measurement and attribution. AIO does not use it to show display ads.

You can deny or revoke permissions in system settings; related features will not work.

## 5. Meta App Events (Android)

On Android, AIO initializes Meta’s App Events SDK at launch.

Events we log are limited to onboarding funnel steps (for example step name, selected category types, starter choice, and completion). Parameters use short enum-style names. We do not send note titles, note bodies, contacts, or media contents in these events.

Meta may also receive standard SDK signals such as app activation and advertising identifiers, subject to Meta’s policies and your device settings.

Third-party policy: [Meta Privacy Policy](https://www.facebook.com/privacy/policy/)

## 6. AIO Premium (Android)

AIO Premium is an optional paid subscription that unlocks features such as higher free-tier limits and (when monetization is enabled) backup.

Purchases and restores are processed by Google Play Billing. RevenueCat helps us verify entitlements. RevenueCat may receive an anonymous app user ID, purchase/entitlement status, device identifiers (including advertising ID where available), and a Meta anonymous ID used to match attribution.

Card numbers and full payment credentials are handled by Google Play, not by AppForge.

This is separate from in-app “subscription reminder” notes, which are local reminders you create about third-party services you pay for elsewhere.

Third-party policies:

- [RevenueCat Privacy Policy](https://www.revenuecat.com/privacy)
- [Google Play Privacy Policy](https://policies.google.com/privacy)

## 7. Reminders & Optional Remote Delivery

By default, reminder notifications are scheduled with the operating system’s local notification APIs. There is no separate push vendor in that mode.

In some builds, remote reminder delivery may be enabled. When it is:

- AIO creates an anonymous Firebase Authentication user (no email/password AIO account).
- An FCM token and device metadata (platform, flavor, timezone, optional RevenueCat app user ID) may be stored in Firebase (Firestore).
- Schedule timing metadata may be stored (type, note/item IDs, payload identifiers, next fire time, recurrence rules). Reminder title and body text are not uploaded; they are resolved on the device from your local notes when a message arrives.
- AppForge-operated Cloud Functions may send data-only FCM messages so the device can show the reminder.

Uninstalling the app or clearing app data removes local note content. You can also revoke notification permission in system settings.

## 8. Optional Email Feedback

AIO does not include a crash-reporting, performance-tracing, or product-analytics SDK such as Crashlytics, Sentry, or Firebase Analytics.

If you choose to send feedback, the app opens your device’s email app with a draft that may include feedback type, optional area, app version, build number, and platform. Whatever you include in that message (and any attachments you add) is sent through your email provider to AppForge.

We do not automatically attach screenshots, device logs, or note contents.

## 9. Link Previews

When you save certain links, AIO may request page metadata or preview images from that website (and providers such as TikTok oEmbed or YouTube thumbnails).

Those servers receive a normal request from your device (such as IP address and User-Agent).

## 10. On-Device OCR

Text recognition for business cards and book notes runs on your device using Google ML Kit.

AppForge does not operate a server that receives those images for OCR.

## 11. App Updates (Android)

On Android, AIO may use Google Play’s in-app update API to check for and apply updates. That contact is with Google Play, not an AppForge note server.

## 12. What We Do Not Do

- No display ads or ad-mediation SDKs in the app.
- No sale of personal data.
- No Crashlytics, Sentry, or Firebase Analytics SDK.
- No App Tracking Transparency prompt for advertising on iOS (Meta App Events and Premium billing paths described above are Android-focused in the current app).
- No separate email/password AIO cloud account, and no AppForge-hosted database of your full note contents.
- No access to your device contacts list or location sensors.
- We do not process your payment card numbers ourselves (Google Play handles Premium payments).

## 13. Who We Share Data With

- **Google** — Sign-In, Drive app-data backup, on-device ML Kit / related Google libraries, Google Play (billing and updates), and Firebase (Auth, FCM, Firestore) when remote reminder delivery is enabled.
- **Meta** — App Events / attribution on Android (see §5).
- **RevenueCat** — Premium entitlements and related identifiers on Android when monetization is active (see §6).
- **Websites / CDNs you link to** — when fetching link previews.
- **Apps you choose** — when you share content out of AIO or open phone, email, or web links.
- **Your email provider and AppForge** — only if you send us feedback by email.

Third-party policies:

- [Google Privacy Policy](https://policies.google.com/privacy)
- [Meta Privacy Policy](https://www.facebook.com/privacy/policy/)
- [RevenueCat Privacy Policy](https://www.revenuecat.com/privacy)

## 14. Retention

- **On device:** until you delete the content or uninstall the app.
- **Google Drive backup:** until you delete it or revoke Google access.
- **Firebase (remote reminders, when enabled):** device tokens and schedule metadata until they are overwritten, cleaned up, or you stop using the app / clear data; subject to our operational retention and applicable law.
- **Meta / RevenueCat:** retained under those providers’ policies for events, attribution, and purchase records.
- **Email feedback:** until we handle your request and delete it, unless we must keep it longer to comply with law.
- **Link-preview cache:** temporary on-device cache.

## 15. Security

Data is stored in the app sandbox.

Optional backups are encrypted on-device (Argon2id + AES-256-GCM) before upload.

No method is 100% secure. Protect your device and your recovery key.

## 16. Your Choices

You can:

- Use AIO without Google Sign-In (local only).
- Use AIO without purchasing AIO Premium.
- Sign out / revoke Google Drive access in Google account settings.
- Delete notes in-app and clear backup if enabled.
- Control camera, mic, photos, and notifications in system settings.
- Control advertising / ad-personalization settings in your Android system settings (affects advertising ID availability).
- Choose not to send feedback, and avoid including sensitive information in any email you send us.
- Email us to request deletion of feedback you previously sent.

## 17. Children

AIO is not directed at children under 13 (or the minimum digital-consent age in your country).

Do not use the app to store children’s personal data unless you are allowed to do so.

## 18. International Transfers

If you use Google Sign-In/Drive, Meta App Events, RevenueCat, Google Play, Firebase, or link previews, data may be processed in countries other than yours under those providers’ terms.

If you email us feedback, your message may also be processed by your email provider in other countries.

## 19. Your Rights

Depending on where you live, you may have rights to access, correct, delete, or restrict processing of personal data, and to lodge a complaint with a regulator.

- **India (DPDP):** contact us to exercise applicable rights under Indian law.
- **EEA/UK (GDPR):** you may request access, rectification, erasure, restriction, or objection, and complain to your supervisory authority.
- **California (CCPA/CPRA):** we do not sell personal information or share it for cross-context behavioral advertising as those terms are commonly understood for “sale.” Limited advertising identifiers may be used for attribution via Meta/RevenueCat as described above. You may request to know or delete personal information we hold (for example, feedback you emailed us) by emailing us.

**Contact:** appforge91@gmail.com

We will respond as required by applicable law.

## 20. Changes

We may update this policy.

We will change the Last updated date and, where required, provide additional notice in the app or store listing.

## 21. Contact

AppForge

**Email:** appforge91@gmail.com
