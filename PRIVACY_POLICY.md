# Privacy Policy - Zen

**Last updated: March 18, 2026**
**App:** Zen (`com.zenvy.com`)
**Developer:** Zenvy Cloud
**Contact:** privacy@zenvytechno.com

---

## 1. Introduction

Zen is a personal finance and productivity app that helps you track expenses, split costs with friends, settle payments, and collaborate on tasks with the people around you. This Privacy Policy explains exactly what data we collect, why we collect it, how we use and share it, and how we protect it.

We built Zen on a simple principle: **your data belongs to you**. We collect only what is necessary to make the app work.

By using Zen, you agree to the practices described in this policy. If you do not agree, please do not use the app.

---

## 2. Information We Collect

We collect information in the following ways: directly from you when you use the app, automatically through the services we use, and optionally through device permissions you choose to grant.

### 2.1 Account Information
- **Email address** - when you sign up with email/password or Google
- **Phone number** - used to identify your account and to match you with contacts in split expenses and collaborative tasks
- **Display name and profile photo** - sourced from your Google account if you sign in with Google, or set by you during onboarding

### 2.2 Financial Data
- **Expenses** - amount, merchant/description, category, date, payment method, notes, receipt photos
- **Splits** - who paid, how much each person owes, settlement status
- **Settlements** - payment records between you and your contacts

This data is stored locally on your device and synced to Firebase Firestore under your account.

### 2.3 Task Data
- **Tasks** - title, description, status, priority, due date, assignee, and checklist items
- **Task activity** - who created a task, who it is assigned to, and status changes (accepted, started, completed, declined)

Task data is stored in Firebase Firestore and shared between participants (creator and assignee) to enable real-time collaboration.

### 2.4 SMS Text *(optional - user-initiated only)*
The app can parse an SMS message to help you log an expense quickly. This works in two ways:

- **Manual paste** - you open the app and paste an SMS text yourself into the SMS entry screen
- **Share from messaging app** - you share an SMS from your messaging app to Zen; the app shows you the parsed result and you confirm before anything is saved

In both cases: **you initiate the action**, you see the parsed result before it is saved, and the raw SMS text is never sent to our servers. Only the structured expense fields you confirm (amount, merchant, date, category) are saved to your account.

### 2.5 Contacts *(optional - requires Contacts permission)*
Contact names and phone numbers are read from your device to help you select friends when splitting an expense or assigning a task. When you add a contact as a participant in a split or task, their name and phone number are saved to our backend to enable matching and collaboration features. Contacts are not bulk-uploaded — only contacts you explicitly interact with inside the app are stored on our servers.

### 2.6 Camera and Photos *(optional - requires Camera permission)*
If you photograph receipts, images are stored locally. If you back up your data, images are stored in your own Google Drive. Images are also processed on-device for OCR (text extraction to auto-fill expense fields).

### 2.7 Usage Analytics
We collect anonymous, aggregated usage events via Firebase Analytics:
- Screen views and navigation flows
- Feature usage (expense added, split created, settlement completed, task created)
- Authentication method chosen
- App errors and crash signals

Analytics help us understand how the app is used and where to focus improvements. The scope of analytics may expand as the app grows; this policy will be updated to reflect any meaningful changes.

### 2.8 Device Information
Firebase automatically collects basic device information (device model, OS version, app version, language) to provide analytics and improve app stability. This is not linked to your personal identity.

### 2.9 Push Notification Tokens
Your Firebase Cloud Messaging (FCM) device token is stored in Firestore to deliver push notifications (settlement reminders, task assignments, task status updates) to your device.

---

## 3. How We Use Your Information

| Information | Purpose |
|---|---|
| Email / phone / name | Create and manage your account; identify you in shared expenses and tasks |
| Financial data (expenses, splits) | Core app functionality - tracking, splitting, settling |
| Task data | Core app functionality - creating, assigning, and tracking collaborative tasks |
| SMS text (user-initiated) | Parse expense details (amount, merchant, date) that you choose to log; raw text stays on-device |
| Contacts | Suggest friends when creating a split or assigning a task; store participants you interact with |
| Receipt photos | Attach to expenses; OCR auto-fill of amount and merchant |
| Analytics events | Understand how features are used; improve the app |
| Device info | Crash reporting and stability improvements |
| FCM token | Deliver settlement reminders, task assignment alerts, and status notifications |
| Expense history (anonymised, opt-in) | Generate AI spending insights via Google Gemini when you request it |

We do **not** use your data for advertising, profiling, or selling to third parties.

---

## 4. Sharing of Information

We do not sell your personal data. We share data only in the following limited circumstances:

**With other Zen users you choose to interact with:**
When you split an expense, settle a payment, or collaborate on a task with a contact, your display name, phone number, and the relevant expense or task details are shared with that contact within the app.

**With our service providers (processors):**
We use the following third-party services that process data on our behalf. Each is contractually bound to use your data only to provide their service to us.

| Service | Provider | Data shared | Purpose |
|---|---|---|---|
| Firebase Auth | Google | Email, phone, UID | Authentication |
| Firebase Firestore | Google | Expenses, splits, tasks, user profile, contacts | Cloud data sync |
| Firebase Analytics | Google | Anonymous usage events | App analytics |
| Firebase Cloud Messaging | Google | FCM device token | Push notifications |
| Google Sign-In | Google | Email, name, profile photo | Authentication |
| Google Drive API | Google | AES-256 encrypted backup files | Backup storage in your Drive |
| Google Gemini API | Google | Anonymised expense amounts and categories | AI spending insights (opt-in only) |

Links to their privacy policies: [Firebase](https://firebase.google.com/support/privacy) - [Google](https://policies.google.com/privacy) - [Gemini API](https://ai.google.dev/gemini-api/terms)

**For legal reasons:**
We may disclose information if required by law, court order, or to protect the rights and safety of our users or the public.

**No other sharing.** We do not share data with advertisers, data brokers, or any other third party not listed above.

---

## 5. Data We Do NOT Collect

- Notification content from your bank or payment apps - we do not read or access notifications in the background
- SMS messages in the background - SMS text is only processed when you explicitly share or paste it yourself
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

- **Access** - view all your data through the app's expense history and profile screens
- **Export** - export your data as CSV or PDF via Profile -> Export
- **Delete** - delete your account via Profile -> Settings -> Delete Account (removes all Firestore data within 30 days)
- **Opt out of analytics** - Profile -> Settings -> Privacy -> toggle off Analytics
- **Delete backups** - open Google Drive and delete the "Zen Backups" folder
- **Correct your data** - update your display name and profile via Profile -> Edit

To exercise any right or make a data request, email **privacy@zenvytechno.com**. We will respond within 30 days.

### GDPR (European Union Users)
If you are located in the EU or EEA, you have additional rights under the General Data Protection Regulation:

- **Legal basis for processing:** We process your data on the basis of (a) contract performance - to provide the app's core functions; (b) legitimate interests - analytics to improve the app; and (c) consent - optional permissions (contacts, camera, AI insights)
- **Right to erasure** ("right to be forgotten") - request deletion of your data at any time
- **Right to data portability** - request your data in a machine-readable format (use CSV export)
- **Right to object** - object to processing based on legitimate interests
- **International transfers:** Your data is processed on Google's servers, which may be located outside the EU. Google complies with the EU-US Data Privacy Framework and Standard Contractual Clauses

To exercise GDPR rights, email privacy@zenvytechno.com with "GDPR Request" in the subject line.

### CCPA (California Users)
If you are a California resident, you have rights under the California Consumer Privacy Act:

- **Right to know** - what personal information we collect and how we use it (this document)
- **Right to delete** - request deletion of your personal information
- **Right to opt out of sale** - we do not sell your personal information to any third party
- **Right to non-discrimination** - we will not discriminate against you for exercising your rights

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

Zen handles financial and personal data. While we follow industry-standard security practices, this policy does not constitute legal advice. If you are deploying this app in a regulated context, we recommend consulting a qualified legal professional familiar with data protection laws in your jurisdiction.

---

## 12. Contact Us

**Zenvy Cloud**
Email: privacy@zenvytechno.com
Support: support@zenvytechno.com
GitHub: [github.com/zenvy-cloud](https://github.com/zenvy-cloud)

For data requests, GDPR enquiries, or CCPA requests, email privacy@zenvytechno.com. We aim to respond within 30 days.

---

*This privacy policy applies to the Zen Android app (`com.zenvy.com`) distributed on Google Play.*
