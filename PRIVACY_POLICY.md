# Privacy Policy for Zen

**Last updated: March 18, 2026**
**App:** Zen (`com.zenvy.com`)
**Developer:** Zenvy Cloud
**Contact:** privacy@zenvytechno.com

---

## 1. Introduction

Zen is a personal finance app that helps you track expenses, split costs with friends, and settle payments. This Privacy Policy explains exactly what data we collect, why we collect it, how we use and share it, and how we protect it.

We built Zen on a simple principle: **your financial data belongs to you**. We collect only what is necessary to make the app work.

By using Zen, you agree to the practices described in this policy. If you do not agree, please do not use the app.

---

## 2. Information We Collect

We collect information in the following ways: directly from you when you use the app, automatically through the services we use, and optionally through device permissions you choose to grant.

### 2.1 Account Information
- **Email address** â€” when you sign up with email/password
- **Phone number** â€” when you sign in via OTP; also used to match you with contacts in split expenses
- **Display name and profile photo** â€” sourced from your Google account if you sign in with Google

### 2.2 Financial Data
- **Expenses** â€” amount, merchant/description, category, date, payment method, notes, receipt photos
- **Splits** â€” who paid, how much each person owes, settlement status
- **Settlements** â€” payment records between you and your contacts

This data is stored locally on your device and synced to Firebase Firestore under your account.

### 2.3 SMS Text *(optional â€” user-initiated only)*
The app can parse an SMS message to help you log an expense quickly. This works in two ways:

- **Manual paste** â€” you open the app and paste an SMS text yourself into the SMS entry screen
- **Share from messaging app** â€” you share an SMS from your messaging app to Zen; the app shows you the parsed result and you confirm before anything is saved

In both cases: **you initiate the action**, you see the parsed result before it is saved, and the raw SMS text is never sent to our servers. Only the structured expense fields you confirm (amount, merchant, date, category) are saved to your account.

### 2.4 Contacts *(optional â€” requires Contacts permission)*
Contact names and phone numbers are read to help you select friends when splitting an expense. Contacts are used in-app only and are never uploaded to our servers.

### 2.5 Camera and Photos *(optional â€” requires Camera permission)*
If you photograph receipts, images are stored locally. If you back up your data, images are stored in your own Google Drive. Images are also processed on-device for OCR (text extraction to auto-fill expense fields).

### 2.6 Usage Analytics
We collect anonymous, aggregated usage events via Firebase Analytics:
- Screen views and navigation flows
- Feature usage (expense added, split created, settlement completed)
- Authentication method chosen
- App errors and crash signals

Analytics data does **not** include your financial amounts, merchant names, or contact information.

### 2.7 Device Information
Firebase automatically collects basic device information (device model, OS version, app version, language) to provide analytics and improve app stability. This is not linked to your personal identity.

### 2.8 Push Notification Tokens
Your Firebase Cloud Messaging (FCM) device token is stored in Firestore to deliver push notifications (settlement reminders, incoming settlement alerts) to your device.

---

## 3. How We Use Your Information

| Information | Purpose |
|---|---|
| Email / phone / name | Create and manage your account; identify you in shared expenses |
| Financial data (expenses, splits) | Core app functionality â€” tracking, splitting, settling |
| SMS text (user-initiated) | Parse expense details (amount, merchant, date) that you choose to log; raw text stays on-device |
| Contacts | Suggest friends when creating a split expense |
| Receipt photos | Attach to expenses; OCR auto-fill of amount and merchant |
| Analytics events | Understand how features are used; improve the app |
| Device info | Crash reporting and stability improvements |
| FCM token | Deliver settlement reminders and payment notifications |
| Expense history (anonymised, opt-in) | Generate AI spending insights via Google Gemini when you request it |

We do **not** use your data for advertising, profiling, or selling to third parties.

---

## 4. Sharing of Information

We do not sell your personal data. We share data only in the following limited circumstances:

**With other Zen users you choose to interact with:**
When you split an expense or settle a payment with a contact, your display name, phone number, and the relevant expense details are shared with that contact within the app.

**With our service providers (processors):**
We use the following third-party services that process data on our behalf. Each is contractually bound to use your data only to provide their service to us.

| Service | Provider | Data shared | Purpose |
|---|---|---|---|
| Firebase Auth | Google | Email, phone, UID | Authentication |
| Firebase Firestore | Google | Expenses, splits, user profile | Cloud data sync |
| Firebase Analytics | Google | Anonymous usage events | App analytics |
| Firebase Cloud Messaging | Google | FCM device token | Push notifications |
| Google Sign-In | Google | Email, name, profile photo | Authentication |
| Google Drive API | Google | AES-256 encrypted backup files | Backup storage in your Drive |
| Google Gemini API | Google | Anonymised expense amounts and categories | AI spending insights (opt-in only) |

Links to their privacy policies: [Firebase](https://firebase.google.com/support/privacy) Â· [Google](https://policies.google.com/privacy) Â· [Gemini API](https://ai.google.dev/gemini-api/terms)

**For legal reasons:**
We may disclose information if required by law, court order, or to protect the rights and safety of our users or the public.

**No other sharing.** We do not share data with advertisers, data brokers, or any other third party not listed above.

---

## 5. Data We Do NOT Collect

- Notification content from your bank or payment apps â€” we do not read or access notifications in the background
- SMS messages in the background â€” SMS text is only processed when you explicitly share or paste it yourself
- Your precise or approximate location
- Advertising identifiers (AD_ID permission is explicitly removed from the app)
- Browsing history or cross-app tracking data
- Any data from children under 13 (intentionally)

---

## 6. Data Security

We take the following measures to protect your data:

| Mechanism | Detail |
|---|---|
| Backup encryption | AES-256-GCM encryption applied before data leaves your device; key stored in Android Keystore |
| Transport security | All network traffic uses HTTPS/TLS; cleartext traffic is disabled |
| Firebase security rules | Firestore rules enforce that users can only access their own data |
| App sandbox | On-device SQLite database is protected by Android's app sandbox |

We do not claim that any system is 100% secure. If you discover a security issue, please report it to privacy@zenvytechno.com.

---

## 7. Data Retention

- **Active account:** Data is retained as long as your account exists
- **Deleted account:** Firestore data is deleted within 30 days of account deletion
- **On-device data:** Deleted when you uninstall the app or clear app data
- **Analytics:** Anonymised event data retained for 14 months (Firebase default)
- **Google Drive backups:** Retained in your Drive until you delete them; we have no access

---

## 8. Your Rights

You have the following rights regardless of where you are located:

- **Access** â€” view all your data through the app's expense history and profile screens
- **Export** â€” export your data as CSV or PDF via Profile â†’ Export
- **Delete** â€” delete your account via Profile â†’ Settings â†’ Delete Account (removes all Firestore data within 30 days)
- **Opt out of analytics** â€” Profile â†’ Settings â†’ Privacy â†’ toggle off Analytics
- **Delete backups** â€” open Google Drive and delete the "Zen Backups" folder
- **Correct your data** â€” update your display name and profile via Profile â†’ Edit

To exercise any right or make a data request, email **privacy@zenvytechno.com**. We will respond within 30 days.

### GDPR (European Union Users)
If you are located in the EU or EEA, you have additional rights under the General Data Protection Regulation:

- **Legal basis for processing:** We process your data on the basis of (a) contract performance â€” to provide the app's core functions; (b) legitimate interests â€” analytics to improve the app; and (c) consent â€” optional permissions (contacts, camera, AI insights)
- **Right to erasure** ("right to be forgotten") â€” request deletion of your data at any time
- **Right to data portability** â€” request your data in a machine-readable format (use CSV export)
- **Right to object** â€” object to processing based on legitimate interests
- **International transfers:** Your data is processed on Google's servers, which may be located outside the EU. Google complies with the EU-US Data Privacy Framework and Standard Contractual Clauses

To exercise GDPR rights, email privacy@zenvytechno.com with "GDPR Request" in the subject line.

### CCPA (California Users)
If you are a California resident, you have rights under the California Consumer Privacy Act:

- **Right to know** â€” what personal information we collect and how we use it (this document)
- **Right to delete** â€” request deletion of your personal information
- **Right to opt out of sale** â€” we do not sell your personal information to any third party
- **Right to non-discrimination** â€” we will not discriminate against you for exercising your rights

To exercise CCPA rights, email privacy@zenvytechno.com with "CCPA Request" in the subject line.

---

## 9. Children's Privacy

Zen is not directed at children under 13 (or under 16 in the EU). We do not knowingly collect personal information from children. If you believe a child has provided us with personal data, please contact us immediately and we will delete it.

---

## 10. Changes to This Policy

We may update this policy as the app adds features or regulations change. When we make significant changes we will:
- Update the **Last updated** date at the top
- Show an in-app notice on the next app launch

Continued use of the app after an update constitutes acceptance of the revised policy.

---

## 11. Legal Notice

Zen handles financial data. While we follow industry-standard security practices, this policy does not constitute legal advice. If you are deploying this app in a regulated context, we recommend consulting a qualified legal professional familiar with data protection laws in your jurisdiction.

---

## 12. Contact Us

**Zenvy Cloud**
Email: privacy@zenvytechno.com
Support: support@zenvytechno.com
GitHub: [github.com/zenvy-cloud](https://github.com/zenvy-cloud)

For data requests, GDPR enquiries, or CCPA requests, email privacy@zenvytechno.com. We aim to respond within 30 days.

---

*This privacy policy applies to the Zen Android app (`com.zenvy.com`) distributed on Google Play.*
