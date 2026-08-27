# Privacy Policy

**Effective date:** August 27, 2026

LampedUp ("we," "us," or "our") operates the Buckets mobile application (the "App"). Buckets is operated by LampedUp, a business of Justin Prappas (the App Store seller of record). This Privacy Policy explains what information the App collects, how it is used, and your choices. By using Buckets, you agree to the practices described here.

If you have questions, contact us at **justinp@lampedup.co**.

## 1. Information We Collect

### 1.1 Account Information
When you create an account, we collect the identity information needed to authenticate you: your email address (email/password sign-in), or the identifier provided by Apple Sign-In or Google Sign-In. We use Supabase Auth to manage this process; we do not receive or store your Apple/Google account password.

### 1.2 Bank and Financial Account Data
Buckets connects to your bank and investment accounts through **Plaid**, a third-party financial data provider. When you link an account:

- You enter your bank login credentials directly into Plaid's own secure interface (Plaid Link). **Buckets never receives, sees, or stores your bank username or password.**
- Plaid returns a token representing your linked account. That token is exchanged and stored **server-side**, in our Supabase backend — it is never transmitted to or stored on your device.
- Using that token, our server retrieves and stores your account balances and transaction history (merchant, amount, date, category) so the App can display your dashboard, budget, and spending breakdowns.

### 1.3 NIL Income Data You Enter
Deal/income records you manually enter (company name, amount, date, payment status) are stored in our database and associated with your account so you can track NIL earnings and estimated taxes.

### 1.4 Push Notification Data
If you enable notifications, we store a device push token (an opaque identifier issued by Apple) so we can deliver reminders (e.g., tax deadlines, large-transaction alerts) to your device. This token is not used for advertising or cross-app tracking.

### 1.5 Crash and Diagnostic Data
We use **Sentry** to capture crash reports and performance diagnostics so we can fix bugs. Our Sentry configuration explicitly strips user-identifying information (no email, no account ID, no user object) from every event before it is sent — diagnostic events are anonymized technical data (device/OS type, stack traces, performance timings), not tied back to your identity by us.

## 2. How We Use Information

We use the information above only to operate and improve the App's core functionality:

- Authenticate you and keep your account secure
- Display your linked account balances, transactions, and budget breakdowns
- Track your NIL income and calculate informational tax set-aside estimates
- Send the notifications you've opted into
- Diagnose and fix crashes/bugs

**We do not sell your data. We do not use your data for advertising. We do not track you across other companies' apps or websites, and the App does not use the App Tracking Transparency framework because no such tracking occurs.**

## 3. Third-Party Service Providers (Subprocessors)

We rely on the following service providers to operate the App. Each processes data on our behalf under their own privacy and security terms:

| Provider | Purpose | Data Involved |
|---|---|---|
| **Supabase** | Authentication, database, and server-side logic (including Plaid token exchange) | Account identity, financial data, app data |
| **Plaid** | Bank/investment account linking and data retrieval | Bank credentials (held only by Plaid, never by us), account balances/transactions |
| **Sentry** | Crash and performance diagnostics | Anonymized technical/crash data |
| **Apple (Sign in with Apple, APNs)** | Authentication option; push notification delivery | Apple ID identifier (if used), device push token |
| **Google (Google Sign-In)** | Authentication option | Google account identifier (if used) |

## 4. Data Storage and Security

Your account and financial data are stored in our Supabase-hosted database, protected by row-level security policies that restrict access to your own data. Bank access tokens issued by Plaid are held only on our server (never on your device) and are never exposed to the iOS app. Infrastructure-level encryption (in transit via TLS/HTTPS, and at the storage-provider level) protects data. In addition, bank access tokens are encrypted at the application layer using Supabase Vault before they are ever written to the database — the stored record holds only an opaque reference, not the token itself. This protects your bank access token even in the unlikely event a database backup or export were exposed. It does not replace the server-side access controls described above, which remain the primary safeguard against unauthorized access.

## 5. Data Retention and Deletion

We retain your account and financial data for as long as your account is active, so the App can function. If you would like your data deleted, contact us at **justinp@lampedup.co** and we will delete your account data upon request. (Removing a linked bank account within the App also deletes the associated transaction and balance data for that account from our database.)

## 6. Children's Privacy

Buckets is intended for users who are college-age (18+) student-athletes. We do not knowingly collect information from children under 13.

## 7. Your Choices

- You can unlink a bank account at any time from within the App, which removes its stored balances and transactions from our database.
- You can disable push notifications at any time in iOS Settings or within the App's notification preferences.
- You can request deletion of your account and associated data at any time by emailing us.

## 8. Changes to This Policy

We may update this Privacy Policy from time to time. Material changes will be reflected by updating the "Effective date" above. Continued use of the App after changes constitutes acceptance of the updated policy.

## 9. Contact Us

LampedUp
Email: **justinp@lampedup.co**

This Privacy Policy is not legal, tax, or financial advice.
