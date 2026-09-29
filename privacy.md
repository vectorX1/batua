---
title: Privacy policy
permalink: /privacy.html
---

# Batua privacy policy

**Effective date:** October 1, 2027

This policy explains what the Batua Android app ("Batua", "the app") stores, where it stores it, and what it does with it. Batua is published by **Utilio Apps** ("we", "us").

## The short version

- Batua keeps your card details **only on your phone**.
- The app has **no internet permission**, so it can't send data anywhere, including to us.
- We **don't collect, receive, sell or share** any of your data. We can't see your cards.
- There is **no account, no advertising, no analytics and no crash reporting** inside the app.

## What the app stores on your phone

**Card details you enter, scan or tap:**

| Data | How it's stored |
|---|---|
| Card number | Encrypted |
| Cardholder name | Encrypted |
| Expiry date | Encrypted |
| Bank hotline number (optional) | Encrypted |
| Card type (credit or debit), bank name, nickname, category, favorite mark, card color, date added | Stored without encryption, inside the app's private storage |

**The CVV is never stored.** Storing the CVV (the 3 or 4 digit security code) is intentionally disabled. The app has no CVV field, scanning the back of a card doesn't read it, and tapping a card can't read it because it isn't on the chip. The CVV is what proves you hold the physical card, so it stays on the card and nowhere else. If an earlier version of the app saved a CVV on your phone, updating the app deletes it.

**App settings:**
- theme
- auto-lock time
- whether you've seen the welcome screen
- whether you've been asked for notification permission
- which expiry notices you've dismissed or been reminded about, stored as card ID numbers only, never card details

These settings are stored in the app's private storage and contain no card details.

**How encryption works:** the encrypted fields use AES-256-GCM with a random 256-bit key. That key is itself encrypted by a key held in the Android Keystore, which on most phones is protected by the phone's secure hardware and can't be copied off the phone.

Android keeps the app's private storage away from other apps. Batua also blocks Android's automatic cloud backup and phone-to-phone transfer of its data, so your cards aren't copied to Google's servers or to another phone by Android.

## What leaves your phone

**Nothing.**
- The app has no internet permission. Card scanning uses Google's ML Kit text recognition with a model **bundled inside the app**, so it runs entirely on your phone. It sends nothing, and camera images are never saved.
- **Tap to add (NFC):** when you hold a card to the phone in Tap mode, the app reads the card number, expiry and (if the card has one) cardholder name from the card's chip, on your phone. It asks only for what a payment terminal reads first and never asks the card to approve a payment, so nothing is charged. Some cards also return a one-time security code during this step. That code, and everything else the card returns apart from the number, expiry and name, is discarded straight away and never sent to your bank or anyone else.
- **No export or backup:** the app has no way to export, share or back up your cards, and Android's own backup and phone-to-phone transfer are blocked for it. Your card details exist only on your phone.
- **Links:** if you tap "Privacy policy" or "Support" in the app, your browser or email app opens outside Batua. They follow their own privacy policies.

## Permissions the app uses

| Permission | Why |
|---|---|
| Camera | To scan a card when you open the scanner. Asked only then; the app works without it. |
| NFC | To read a card you tap on the phone, only while the scanner's Tap mode is open. Granted at install (Android doesn't ask); nothing is read at any other time. |
| Notifications | To remind you before a card expires. Optional. |
| Biometric | To unlock the vault with your fingerprint (or secure face unlock), through Android's screen-lock prompt. |
| Run at startup, keep awake, view network state | Used by Android's scheduler (WorkManager) to run the daily expiry check, including after a restart. "View network state" can't send data; the app has no internet permission. |

## Notifications

Expiry reminders show only the card's nickname (or bank) and its last four digits. On the lock screen they show only a title, with no card details.

## Clipboard

If you copy a card number, Batua marks it as sensitive, so Android hides it in clipboard previews. The app clears it after 45 seconds, unless you've copied something else since.

## Your control over your data

- **Delete one card:** open the card and tap Delete. You'll be asked to confirm with your screen lock.
- **Delete everything:** Settings, then Reset vault. This deletes every card and the encryption keys.
- **Uninstall:** uninstalling Batua deletes all of its data from your phone.

Because we never receive your data, there's nothing for us to access, correct or delete on our side. We can't restore cards you've deleted or lost, and neither can the app: there is no backup.

## Children

Batua is meant for adults who hold payment cards. It isn't directed at children, and it collects no data from anyone.

## Payments

You buy Batua through Google Play. Google handles the purchase under its own terms and privacy policy. We get sales reports from Google Play, which don't include your card details.

## Changes to this policy

If the app's handling of data changes, we'll update this page and its effective date before releasing that version. Any change that would send data off your phone would be clearly announced in the app and on its store listing first.

## Contact

Questions about privacy: [{{ site.support_email }}](mailto:{{ site.support_email }})
