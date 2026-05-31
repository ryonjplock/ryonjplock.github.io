# Privacy Policy for SwipeBack

**Effective Date:** May 30, 2026

This Privacy Policy explains how SwipeBack ("we," "our," or "the Application") handles user data. SwipeBack is built as an offline-first notification history utility designed to let users review, search, and manage historical notification logs on their Android devices.

## 1. Developer Identity
* **Application Name:** SwipeBack
* **Package Name:** com.pan.handling.swipeback
* **Contact Email:** ryonandrock@gmail.com

---

## 2. Sensitive Permissions & Data Collection
SwipeBack requires Android's **Notification Listener Access** (NotificationListenerService) to fulfill its core functionality[cite: 3]. Without this permission, the app cannot operate.

### Data We Process:
When notifications are posted or dismissed by other applications on your device, SwipeBack temporarily intercepts and reads the following data points:
* **Application Metadata:** The human-readable application name and raw system package identifier (e.g., com.android.settings).
* **Notification Content:** Notification titles, tickers, body texts, and expanded text lines.
* **Timing Indicators:** The exact unix timestamps indicating when a notification was posted, modified, or removed from the system.

---

## 3. Data Storage & Local Processing (100% Offline)
Google Play requirements demand transparency regarding data transmission. SwipeBack adheres to a strict local-only data architecture:

* **Zero Cloud Transmission:** SwipeBack does **not** own, lease, or operate external servers. No user notification data or behavioral analytics ever leave your physical device.
* **Local Database Storage:** The intercepted notification text and app metadata are committed to a secure, private, sandboxed SQLite database (managed via Android’s Room persistent library) accessible only to SwipeBack.
* **Exclusions:** SwipeBack includes configuration mechanisms to actively ignore sensitive notification contexts, including ongoing background media player instances or self-generated app alerts to avoid recursive loops.

---

## 4. User Control, Data Retention, and Deletion
You retain absolute custody and control over your data. SwipeBack provides transparent utilities to manage and purge its data stack directly:

* **Manual Item Removal:** Users can use swipe-to-delete contextual gestures directly within the primary activity interface to drop isolated notification strings from the local database.
* **Targeted Application Purging:** Through contextual dialog options ("Mute & Purge"), users can delete all cumulative database histories related to a specific app bundle package identifier at once.
* **Automated Life-cycle Cleanup:** The application features an integrated auto-delete algorithm designed to clean up and overwrite data rows older than a specified duration (e.g., 30 days) to optimize on-device storage space.
* **Total Clear:** If you uninstall SwipeBack, the Android operating system completely and permanently purges the application’s sandboxed database instance and all associated preferences from your hardware.

---

## 5. Third-Party Access & Sharing
* **No Third-Party Analytics:** We do not include third-party advertising SDKs, telemetry tracking libraries, or crash-reporting frameworks that transmit background diagnostics to third-party endpoints.
* **No Monetization of Data:** Because your data is completely inaccessible to us, it is physically impossible for us to sell, share, trade, or distribute your notification history logs to data brokers, advertising agencies, or marketing companies.

---

## 6. Security
We rely on the foundational Android Sandboxing security architecture. Android isolates application storage containers at the kernel level, ensuring that third-party applications without explicit system root privileges cannot access SwipeBack's local log databases.

---

## 7. Changes to This Privacy Policy
We may update our Privacy Policy from time to time to reflect modifications to app mechanics or framework compliance constraints. Any updates will be pushed directly as an in-app notice or via an updated description listing on the Google Play Store.

## 8. Contact Us
If you have questions regarding this offline policy or the privacy mechanisms engineered into SwipeBack, please contact us via our developer email: **ryonandrock@gmail.com**.
