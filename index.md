# QUIX CHAT PRIVACY POLICY AND QUIX CHAT TERMS OF USE
<br><br>
# Quix Chat Privacy Policy
<sub>Version PP-2026-10-31_v01 r1</sub>

<br>
Effective date: October 31, 2026

Last updated: October 31, 2026


This Privacy Policy explains how Quix Chat processes personal data when you use the Quix Chat mobile application, related websites, support channels, and backend services (together, the "Services").

Quix Chat is a privacy-first messaging product built around email-based sign-in, device trust, encrypted direct messaging, encrypted attachments, voice messages, and short video messages (including view-once photos and videos), optional voice and video calling, groups, subgroups, broadcast-style Station channels, ephemeral Global Chat rooms, group polls, and backend-controlled advertising surfaces outside core message threads.

If you have questions about this Privacy Policy, contact:

- Legal entity / controller: Quixyr LLC
- Trade name: Quix Chat / QuixChat
- Email: support@quixyr.com
- Address: 9231 53rd Ave #1A, Elmhurst, NY 11373, USA

## 1. Scope

This Privacy Policy applies to:

- account registration and sign-in using email-based one-time-password (OTP) authentication;
- direct chats (including short video messages and view-once photos and videos), groups, subgroups, broadcast-style Station channels (including Station video posts), ephemeral Global Chat rooms, group polls, voice messages, voice calls, and video calls;
- contact discovery and pairing, including link-based contact and group joining, multi-slot contact re-pairing, and device-trust features;
- support requests, privacy requests, and account deletion or transfer workflows;
- optional advertising placements, if enabled;
- related operational, security, and compliance processing.

Quix Chat previously supported phone-number-based OTP sign-in and account recovery. That functionality has been fully retired and is no longer present in the app; all accounts now register, sign in, and recover access using email.

This Privacy Policy does not govern third-party services you choose to use separately from Quix Chat, such as your mobile carrier, the Apple App Store, Google Play, device backup providers, external payment providers, or third-party websites opened from links inside the app. Those services have their own terms and privacy notices.

## 2. Product Privacy Model

Quix Chat is designed to reduce unnecessary data exposure:

- direct message content, and content stored in the optional private storage feature, is encrypted on the client using keys the backend does not hold, before storage on the server;
- attachments, voice messages, and video messages sent in direct chats are encrypted locally before upload;
- group chats, subgroups, and Station channels (including Station video posts and their attachments) are also encrypted before storage, but use a conversation-derived key rather than a key private to the two participants; this content is not end-to-end encrypted in the same sense as direct messages, and Quix Chat discloses this distinction in the app itself;
- Global Chat rooms are ephemeral and are not stored on our servers at all; messages are relayed in real time and are not persisted server-side beyond the session;
- device trust and recovery-key flows are used to control access to encrypted conversation data;
- ads are configured to stay outside core message threads, including group and Station message threads;
- runtime flags allow us to disable sensitive features or ad placements from the backend without forcing an app update;
- accounts are registered and authenticated using email; internal identifiers such as UUIDs are used for service operations wherever possible instead of using contact or authentication details as general-purpose identifiers.

Quix Chat is not currently launched for the European Economic Area ("EEA"). We are preparing EEA launch separately so that GDPR-specific documentation, regional governance, transfer controls, vendor terms, and compliance operations are complete before rollout.

## 3. Information We Collect

### 3.1 Information you provide directly

We may collect:

- your email address for authentication, account recovery, and security purposes;
- profile information such as display name, avatar, about text, language choice, and notification preferences;
- contact labels you assign inside the app;
- content you choose to send through the Services, including messages, reactions, replies, group and Station participation, group polls, attachments, and voice-message content, which may be stored in encrypted form where applicable;
- encrypted attachments and encrypted voice-message files you choose to upload;
- nicknames and messages you send in Global Chat rooms, which are not stored on our servers (see Section 4.3);
- support or legal/privacy request content you send to us;
- recovery-key and device-transfer inputs you voluntarily use;
- link-based contact or group join codes you generate or redeem.

We use third-party service providers to deliver one-time passwords (OTP) and related verification services by email. Your email address may be shared with these providers solely for authentication, verification, and security purposes.

Quix Chat previously supported phone-number-based sign-in and account recovery. That path has been fully retired: phone numbers are no longer collected, are no longer used to authenticate or recover any account, and are no longer shared with SMS/OTP providers.

### 3.2 Information generated through use of the Services

We may collect:

- account identifiers, conversation identifiers, group identifiers, device identifiers, and session identifiers;
- metadata about conversations and activity, including timestamps, message status, delivery events, unread counts, and call/session state;
- registered-device records, trust state, and device labels;
- notification events, push-token registration state, push-platform details, and badge-count state;
- voice/video call metadata needed to establish and manage calling sessions;
- contact re-pairing history and link-based join/invite metadata, such as code expiry and usage limits;
- security logs, fraud-prevention logs, abuse-prevention logs, operational telemetry, and error diagnostics.

### 3.3 Information from your device

Depending on your permissions and feature use, Quix Chat may access:

- microphone access for voice messages, video messages, voice calls, and video calls;
- camera access for video messages, video calls, and avatars;
- photo library or file-picker access for attachments and avatars;
- contact access if you choose to sync or use contact-based features;
- notification permissions;
- approximate location inferred from IP or regional routing where needed for compliance, fraud prevention, or service routing.

Quix Chat asks for device permissions through the operating system. If you deny a permission, related features may not work.

### 3.4 Information from others

We may receive information about you from:

- users who add or label you as a contact;
- users who invite you to conversations, groups, Stations, or calls;
- other users who report abuse, spam, or policy violations;
- app stores, device platforms, and infrastructure providers that return diagnostic or operational information.

## 4. Encryption and Server Storage

Quix Chat uses different encryption models for different features, described below. Where we say a feature is "end-to-end encrypted," we mean the backend never has access to a key capable of decrypting that content. Where content is described as "encrypted at rest" without the end-to-end description, our backend infrastructure retains the technical ability to derive the relevant key, even though we do not do so as a matter of routine operations.

### 4.1 Direct Messages and Private Storage

Direct message content, encrypted attachments, encrypted voice-message files, and encrypted video messages sent in one-to-one chats are encrypted on the client before they are stored on the backend, using a key derived from information exchanged only between the two participating devices. The backend stores ciphertext, not plain-text copies of this content, and does not hold a key capable of decrypting it.

**Video messages.** You can send short video messages (up to 16 seconds) in one-to-one chats. Videos are encrypted on your device with the same chat key as your other direct messages before they are uploaded; we store only the encrypted file and the metadata needed to deliver it, such as its length, file size, timestamps, and whether it was sent as view-once. A video message becomes unavailable 7 days after it is sent, and the encrypted file is then deleted from our servers by an automated cleanup job.

**View once.** You can send a photo or video as "view once." The recipient can open it one time. When the recipient opens it, the encrypted file is deleted from our servers and cannot be replayed in the app. A view-once item that is not opened expires after 3 hours and is then deleted from our servers by an automated cleanup job. View once limits how long content is available in the app, but it cannot prevent every form of capture. On supported Android devices, screenshots are blocked while a view-once item is open. On iOS, the app hides the content while screen recording is detected and shows a warning when a screenshot is taken, but iOS does not allow screenshots to be blocked. No setting can stop someone from photographing the screen with another device. A copy of what you send may also remain on your own device.

Quix Chat also offers an optional private storage feature for certain content you choose to keep, protected using per-device key wrapping and, if you enable it, an additional PIN-based safeguard. As with direct messages, the backend does not hold a key capable of decrypting this content.

### 4.2 Groups, Subgroups, and Station Channels

Group chats, subgroups, and Station channels (including Station video posts and any attachments sent within them) are also encrypted before storage. However, unlike direct messages, the encryption key for this content is derived deterministically from the conversation itself, rather than from a secret known only to participating devices. This means our backend retains the technical ability to derive the key for this content, even though we do not do so as a matter of routine operations, and this content should not be understood to carry the same end-to-end confidentiality guarantee as direct messages. Quix Chat discloses this distinction inside the app itself wherever these features are used.

### 4.3 Global Chat Rooms

Global Chat rooms are public or semi-public, channel-style spaces. Messages and nicknames sent in Global Chat rooms are relayed in real time and are not encrypted and are not stored on our servers; we do not retain a server-side copy of Global Chat message content. A local copy may remain on your own device for a limited period after a conversation thread ends, for your convenience. Because Global Chat content is not persisted server-side, some safety and moderation tools available elsewhere in the Services work differently for Global Chat; see Section 7.7.

### 4.4 Group Polls and Station Polls

Poll questions and answer options created in group chats are stored in readable, non-encrypted form on our backend, consistent with our general approach to server-readable, user-generated metadata described in Section 7.2, and are subject to the same proactive content filtering described there. Individual votes are also stored on our backend and are not encrypted.

### 4.5 Calls

Voice and video calls are transmitted using secure real-time communication protocols; see Section 5 for details on call-related processing.

### 4.6 Limits That Apply Regardless of Encryption Model

- metadata such as timestamps, sender/recipient/account identifiers, delivery state, call state, and group or channel structure is still processed on the backend;
- if you communicate with another user, that user can still copy, screenshot, forward, record, or disclose what you send;
- if you report content, lawfully disclose content, or share information with third parties, encryption does not prevent that onward disclosure. When you choose to attach a direct-chat video to a report, your device decrypts that video and sends a readable copy to our moderation team, as described in Section 7.3.

## 5. Calls

Quix Chat supports voice and video calling. To make calls work, we process call-related metadata such as:

- caller/callee or session participant identifiers;
- call type (voice or video);
- conversation or room identifiers;
- acceptance, decline, missed-call, join, leave, and end events;
- technical session credentials and connection state.

Media transport for calling is handled through our real-time communications vendor. Call content is not used by Quix Chat for advertising.

## 6. Ads and Monetization

Quix Chat may use advertising, but only in selected placements configured from the backend. As currently designed, Quix Chat does not place ads inside the message stream of conversation in direct and group chat.

Potential placements include:

- first-card native ads in certain list surfaces, such as chats, contacts, and groups lists;
- selected scrolled list positions within those lists;
- native ad placements within a group or Station conversation's side panels (such as a member list or rooms list), separate from the message thread itself;
- app-open ads;
- interstitial ads tied to certain optional account actions;
- rewarded ads tied to optional flows, such as unlocking certain message, contact, or device-management actions;
- small banner placements on certain voice/video-call screens.

Quix Chat does not place ads inside the body of any message thread of direct chat and group chat.

Advertising is governed by:

- backend feature flags and placement controls;
- platform unit IDs;
- consent state and regional privacy choices where required by law.

If advertising is disabled globally in the backend, no individual placement should load even if a placement-specific switch remains enabled.

Depending on your region, device platform, and consent choices, Quix Chat may request or honor advertising preferences, including whether ads may be personalized.

We do not use the content of your messages, calls, voice messages, or attachments in direct chats or group chats to personalize advertising.

## 7. Safety, Moderation, and Prohibited Content

Quix Chat includes user-generated content, private messaging, groups, Stations, Global Chat rooms, avatars, profile fields, and related metadata. We use safety and moderation controls to reduce abuse, support legal compliance, and protect users.

### 7.1 Prohibited content and conduct

You may not use Quix Chat to create, share, organize, request, promote, or facilitate content or conduct that is illegal or prohibited under our Terms, including:

- child sexual abuse material, child exploitation, or grooming-related activity;
- trafficking, exploitation, coercion, or abuse;
- illegal sexual content or non-consensual intimate imagery;
- violent threats or violent extremist content;
- illegal sales, including drugs, weapons, or other unlawful goods or services;
- impersonation, scam activity, fraud, spam, or coordinated abuse.

Violations may result in immediate content restriction, group removal, account suspension, account termination, or other enforcement action.

### 7.2 Server-readable metadata filtering

Quix Chat applies proactive filtering to server-readable user-generated surfaces. Depending on product state and feature rollout, this may include:

- account or member display names;
- group names;
- room or subgroup names;
- group descriptions;
- Station names and descriptions;
- group poll questions and answer options;
- other server-readable metadata fields that we determine require safety review.

When filtering rules are triggered, Quix Chat may block the attempted save, log the event for abuse-prevention or moderation purposes, and require the user to choose different content before continuing.

### 7.3 Encrypted direct-message distinction

Quix Chat is designed so that supported direct-message bodies, encrypted attachments, and encrypted voice messages are encrypted on the client before backend storage. Because those encrypted direct-message bodies are not server-readable by design, Quix Chat does not rely on the same proactive server-side text filtering model for that content as it does for server-readable metadata.

Instead, private direct-message safety is supported through:

- consent-based contact and pairing flows;
- user blocking controls;
- reporting flows that allow users to submit screenshots or other evidence, including a copy of a video message the reported contact sent them;
- moderation review and account or group enforcement when reports are validated;
- backend logging and enforcement for safety events such as blocks, reports, and related actions.

**Attaching a video to a report.** When you report a contact, you can choose to attach one video message that contact sent you. Because direct messages are end-to-end encrypted, we cannot read that video on our own. Instead, your device decrypts only the video you select and uploads a readable copy to our moderation system. The rest of your conversation, and the encryption key that protects it, never leave your device. The copy is not end-to-end encrypted: our authorized moderation staff can view it, and it may be disclosed as described in Sections 7.6 and 10. To check that reported videos are genuine, we confirm that the reported contact sent the original message in that chat and that the copy matches the original's recorded file size. A video can be attached only while it is still available; a view-once video can be attached only before it is opened.

This distinction does not mean private abuse is permitted. It reflects the product's encryption model and the technical limits that follow from it.

### 7.4 Group entry acknowledgements

In some group-join flows, Quix Chat may require users to acknowledge that they will not post, generate, or share illegal or exploitative content before they are allowed to join the group. We may log that acknowledgement with the group, user, policy version, and acceptance timestamp.

### 7.5 Reporting, blocking, and moderation review

Quix Chat may process moderation-related data when users block other users, report users, report groups, or submit moderation evidence. This may include:

- reporter and reported user or group identifiers;
- timestamps, case numbers, and moderation status;
- screenshots, video copies, or other evidence uploaded with a report, together with a reference to the message an attached video came from;
- immutable report-time snapshots of relevant account, contact, or group metadata;
- moderation event logs, reviewer actions, and enforcement history.

We aim to review objectionable-content reports promptly and, where required by platform policy or law, act within applicable response windows. In appropriate cases, Quix Chat may remove content, restrict a group, suspend an account, or terminate an account without prior notice.

### 7.6 Moderation retention

Moderation evidence and related safety records may be retained for up to 28 days after a case is closed, or longer where necessary for legal obligations, fraud prevention, abuse prevention, audits, dispute handling, law-enforcement requests, or an active legal hold.

Reports that include an attached video are placed on legal hold automatically when they are submitted. Video evidence and the related report records under a legal hold are not removed by the 28-day closed-case schedule; they are kept until our moderation team reviews the case and releases the hold, and they may be kept longer where the law requires us to preserve them, including after a report to child-safety authorities.

If a report results in account or group enforcement, certain related records may be retained longer where reasonably necessary to document the action taken, prevent repeat abuse, or comply with law.

Because Global Chat message content is not stored on our servers, this retention section does not apply to ordinary Global Chat message content; moderation actions taken in response to a report (such as a block or restriction) are still recorded as described in Section 7.5.

### 7.7 Global Chat Rooms — Safety Limitations

Global Chat rooms are designed as ephemeral, real-time spaces and are not persisted on our backend (see Section 4.3). As with encrypted direct messages, we do not have server-side access to Global Chat message content to review it directly. As a result:

- nicknames used in Global Chat rooms are validated for basic formatting on your device, but are not currently screened against the server-side content-filtering system used for other server-readable fields such as group and Station names;
- reporting in Global Chat works the same way it does for encrypted direct messages: you can report a user or submit screenshots or other evidence through in-app reporting, which our moderation team reviews and acts on, rather than Quix Chat proactively scanning message content.

We are working on strengthening safety tooling for Global Chat, including server-side review mechanisms appropriate to its ephemeral design. In the meantime, we encourage users to use available blocking and reporting controls and to avoid sharing sensitive personal information in Global Chat rooms.

## 8. How We Use Personal Data

We use personal data to:

- create and secure your account;
- authenticate sign-in and account recovery;
- route you to the correct backend region;
- deliver messaging, calling, groups, subgroups, Station channels, Global Chat rooms, group polls, and attachment features;
- manage device trust, recovery, and encrypted transfer workflows;
- provide customer support and respond to legal/privacy requests;
- detect abuse, spam, fraud, suspicious behavior, and security incidents;
- improve reliability, performance, accessibility, localization, and feature quality;
- comply with legal obligations and protect users, the service, and the public;
- serve and measure ads, if ads are enabled and lawfully permitted.

We do not need to place ads inside direct message threads in order to monetize the service, and Quix Chat is designed to keep that boundary.

## 9. Legal Bases

Depending on your jurisdiction, we rely on one or more of the following legal bases:

- performance of a contract, when processing is necessary to provide the Services you request;
- legitimate interests, including security, abuse prevention, operations, product improvement, and feature integrity;
- consent, where required for particular permissions, advertising, or privacy-choice flows;
- compliance with legal obligations;
- protection of vital interests, rights, safety, and legal claims where applicable.

For users in the EEA or UK, if and when Quix Chat launches there, we will provide additional region-specific disclosures identifying the specific lawful bases we rely on for each relevant category of processing.

## 10. Sharing of Personal Data

We may share personal data with:

- infrastructure, hosting, authentication, storage, notification, and database vendors;
- OTP and verification service providers used for authentication;
- real-time communications vendors used for calling;
- ad vendors and mediation/measurement partners, if ads are enabled;
- analytics, diagnostics, crash-reporting, anti-abuse, and fraud-prevention vendors;
- law enforcement, regulators, courts, or advisors when required by law or needed to protect rights and safety, including reports of apparent child sexual exploitation to the National Center for Missing & Exploited Children (NCMEC) or other authorities as the law requires;
- a successor entity in the event of a merger, acquisition, restructuring, financing, or asset transfer, subject to applicable law.

Quix Chat does not position itself as part of a large cross-service social advertising ecosystem. Compared with Meta-operated WhatsApp, Quix Chat is designed to keep data sharing narrower and product-specific. Compared with Telegram's cloud-chat model, Quix Chat is designed to keep direct message content encrypted before backend storage rather than relying on server-readable cloud chats as the default private-chat model.

## 11. International Transfers

Quix Chat uses regional infrastructure and may transfer data across borders where necessary to operate the Services, maintain security, or support users.

Data may be processed in the United States and in other countries where our providers operate.

For territories with transfer restrictions, we intend to use appropriate safeguards before launch or rollout, such as:

- contractual transfer clauses;
- regional hosting strategies;
- vendor data-processing terms;
- access controls and encryption;
- internal transfer governance.

## 12. Retention

We retain data only for as long as reasonably necessary for the purposes described in this Privacy Policy, including:

- while your account is active;
- while content or metadata is needed to provide the service;
- while records are needed for security, dispute resolution, audits, or legal obligations;
- until a configured expiration or deletion job applies — for example, voice-message files (unavailable 72 hours after sending), direct-chat video messages and Station video posts (unavailable 7 days after sending), and image attachments in chats, groups, subgroups, Station channels, and post comments (unavailable 60 days after sending), each of which is then deleted from our servers by an automated job; and view-once photos and videos (deleted from our servers when opened, or after 3 hours if never opened).

Global Chat room content is not retained on our servers at all, as described in Section 4.3.

When a conversation or message is deleted, for example when you delete a contact, erase a chat's history, or delete a group, the encrypted photos, voice messages, and videos attached to it are queued for deletion from our storage and removed by an automated job. As a backstop, our systems also remove any stored message media that is no longer linked to a message, normally within about 7 days.

When you delete your account, we will delete or de-identify data according to our retention rules and legal obligations. Some data may persist longer in logs, backups, legal records, or records needed to defend legal claims or prevent abuse.

## 13. Your Rights

Depending on your jurisdiction, you may have the right to:

- access personal data;
- correct inaccurate personal data;
- delete personal data;
- export or port certain data;
- object to or restrict certain processing;
- withdraw consent where processing is based on consent;
- appeal a denied privacy request where local law provides that right;
- lodge a complaint with a regulator.

Quix Chat already includes product-level features intended to support these rights, including:

- account deletion;
- data export requests;
- contact and device management;
- notification and privacy choices;
- backend-controlled ad and consent behavior.

Account deletion request instructions (including an off-app request route) are published here:

- [Quix Chat Account and Data Deletion Requests](https://quixyr-devteam.github.io/quix_chat_account_deletion_request/)

## 14. Privacy Laws Quix Chat Is Structured to Support

Quix Chat is designed to support the practical requirements commonly associated with:

- California Consumer Privacy Act, as amended by the CPRA;
- other U.S. state privacy laws with access, deletion, correction, portability, and appeal concepts;
- UK GDPR and the UK Data Protection Act framework;
- Swiss revFADP;
- broader international data-minimization, security, and user-rights norms.

For the EEA, Quix Chat is not yet launched. That is deliberate. Before EEA launch, we plan to finalize:

- GDPR lawful-basis mapping by processing purpose;
- Article 27 or equivalent representation, if needed;
- processor and sub-processor contract review;
- transfer impact and safeguards review;
- age-threshold and parental-consent analysis;
- records of processing, retention mapping, and DSAR operations.

This Privacy Policy is therefore written to be globally structured and privacy-forward, but EEA availability is deferred until the EEA-specific legal work is complete.

## 15. Children

Quix Chat is not intended for user under 16 years old of age.

For users under the age required to form a binding agreement or to consent to data processing in their jurisdiction, use may be limited or require parent or legal guardian authorization where permitted by law.

Certain future features, including unmoderated or publicly accessible chat environments if introduced, may be restricted to users aged 18 or older.

If you believe a child provided personal data in violation of this policy, contact us so we can investigate and take appropriate action.

## 16. Security

We use technical and organizational safeguards appropriate to the risk, including:

- client-side encryption for message content and media in supported flows;
- access controls;
- device-trust controls;
- push-token controls;
- abuse monitoring and operational logging;
- backend feature flags and rollout controls;
- deletion and expiry jobs for selected data classes.

We also implement safeguards designed to minimize unnecessary access to sensitive account identifiers, including limiting authentication-related data to what is needed for account security and using internal identifiers for service operations wherever possible.

No system can guarantee absolute security. You are responsible for securing your device, account access, email account, recovery key, and any backups or screenshots you make.

## 17. Changes to this Privacy Policy

We may update this Privacy Policy from time to time. If we make material changes, we may notify users through the app, the website, or other reasonable channels. The "Effective date" above will reflect the latest version.

## 17A. App Platform Requirements and Permissions

Quix Chat is distributed through third-party application platforms such as the Apple App Store and Google Play. These platforms may impose additional requirements regarding privacy, data use, user-generated content, and user permissions.

Quix Chat:

- requests access to device features such as microphone, camera, photos, files, and notifications only when necessary to enable specific functionality;
- does not access such features without user permission;
- does not use message content, call content, voice-message content, or attachments for advertising personalization;
- allows users to manage permissions through their device settings at any time.

You may also review platform-specific privacy disclosures provided by Apple or Google in connection with your device or account.

## 18. Contact and Complaints

To contact us about privacy, data requests, or complaints:

- Privacy email: privacy@quixyr.com
- Legal address: 9231 53rd Ave #1A, Elmhurst, NY 11373, USA
- Support route: support@quixyr.com

If local law gives you the right to complain to a supervisory authority or data protection regulator, you may do so.

## 18A. Data Requests and Account Controls (DSAR)

Quix Chat provides mechanisms for users to manage their data and submit privacy-related requests.

### Access and Export

You may request a copy of your personal data in a structured, commonly used format. This may include account information, profile data, linked-device records, notification preferences, and other data associated with your account, subject to technical limitations and the rights of others.

### Correction

You may update certain account information directly within the app. If you need assistance correcting inaccurate data, you may contact us using the privacy contact details listed in this policy.

### Deletion

You may request deletion of your account and associated data. Upon deletion:

- active account data will be removed or de-identified in accordance with our retention rules;
- certain data may be retained for a limited period in backups, logs, legal records, or security records;
- retained data may continue to be used where necessary for fraud prevention, abuse prevention, legal compliance, dispute resolution, or defense of legal claims.

### Request Process

To submit a data request:

- use in-app account controls where available; or
- contact us through the privacy contact details listed in this policy.

We may require verification of your identity before fulfilling certain requests in order to protect account security and the rights of others.

Account deletion request instructions (including an off-app request route) are published here:

- [Quix Chat Account and Data Deletion Requests](https://quixyr-devteam.github.io/quix_chat_account_deletion_request/)

### Response Timing

We aim to respond to valid requests within a reasonable timeframe. Where applicable law sets specific deadlines, we will seek to comply with those deadlines.

### Limitations

Some requests may be limited where:

- fulfilling the request would adversely affect the rights, safety, or privacy of other users;
- data must be retained for legal, security, fraud-prevention, abuse-prevention, or recordkeeping purposes;
- technical limitations prevent full extraction of certain encrypted, ephemeral, or device-local data.

Where appropriate, we will explain the basis for any limitation.

## 18B. European Economic Area (EEA) and United Kingdom

If and when Quix Chat becomes available in the EEA or the United Kingdom, additional terms and disclosures will apply to users in those regions.

For EEA/UK users, Quix Chat will, as applicable:

- identify the relevant data controller and, where required, an EU or UK representative;
- document specific legal bases for categories of processing under applicable data protection laws;
- provide additional transparency regarding international data transfers and safeguards;
- implement DSAR handling procedures aligned with applicable statutory timelines;
- review and, where required, obtain consent for certain processing activities, including advertising and optional features;
- apply age-of-consent rules specific to the relevant jurisdiction.

We will update this Privacy Policy and related notices before making the Services available in the EEA or UK.

## Governing Law/ Terms of use

This Privacy Policy is incorporated into and subject to our Terms of Use. Any disputes relating to this Privacy Policy will be governed by the governing law and venue provisions specified in the Terms of Use.

## Language

These Terms and the Privacy Policy are provided in English. Translations may be provided for convenience. In the event of any conflict or inconsistency between a translated version and the English version, the English version will prevail to the extent permitted by applicable law.

<br><br><br>
// //============================================================
<br><br><br>

# Quix Chat Terms of Use
<sub>Version TOU-2026-10-26_v01 r1</sub>

<br>
Effective date: October 26, 2026
Last updated: October 26, 2026

These Terms of Use ("Terms") govern your access to and use of Quix Chat and related services, software, and features (the "Services").

If you do not agree to these Terms, do not use the Services.

## 1. Parties

The Services are provided by Quixyr LLC doing business as Quix Chat / QuixChat ("Quix Chat," "we," "our," or "us").

Contact:

- Legal entity: Quixyr LLC
- Email: admin@quixyr.com
- Address: 9231 53rd Ave, Elmhurst, NY 11373, USA

## 2. Eligibility

You may use the Services only if:

- you meet the minimum age required by applicable law in your jurisdiction;
- you have the legal capacity to agree to these Terms;
- you are not prohibited from using the Services under applicable law;
- your use does not violate export controls, sanctions, or access restrictions we apply by region.

Certain features may be subject to additional age restrictions, usage conditions, or eligibility requirements based on their nature and risk profile. If Quix Chat introduces unmoderated or publicly accessible chat environments in the future, those features may be restricted to users aged 18 or older.

If you are using the Services on behalf of an organization, you represent that you have authority to bind that organization.

## 3. The Services

Quix Chat is a privacy-first messaging platform that may include:

- email-based authentication;
- contact pairing and direct chats;
- encrypted direct messaging;
- encrypted attachments, encrypted voice messages, and encrypted short video messages in direct chats, including view-once photos and videos;
- voice and video calling;
- groups, subgroups, and broadcast-style Station channels, including Station video posts;
- ephemeral Global Chat rooms;
- group polls;
- link-based contact and group joining, and multi-slot contact re-pairing;
- device-trust, recovery-key, and account-transfer features;
- backend-controlled announcements, updates, and advertising placements.

Features may vary by country, device, app version, backend configuration, trust state, legal requirements, moderation status, or runtime flags.

Certain features may be subject to additional terms, age restrictions, or usage policies depending on their nature and risk profile.

## 4. Your Account

You are responsible for:

- keeping your device, email account, and account access secure;
- providing accurate and current account information where required;
- maintaining control of your recovery key and trusted devices;
- reviewing access when you change your email address, change devices, or lose device control.

You must not:

- impersonate another person or entity;
- create accounts using an email address you do not control;
- share recovery keys or access credentials irresponsibly;
- use the Services to evade trust, safety, or access controls.

## 5. Acceptable Use

You may not use Quix Chat to:

- break the law;
- harass, threaten, exploit, or defraud others;
- send spam, phishing, malware, or unauthorized automation;
- distribute illegal sexual content, child sexual abuse material, non-consensual intimate imagery, or violent extremist content;
- send sexual content to, or request sexual or intimate images or videos from, anyone under 18, or use view-once, disappearing, or private messaging features to groom, pressure, threaten, or extort anyone;
- record, capture, or redistribute another person's view-once or private content without their consent;
- infringe intellectual property or privacy rights;
- scrape, reverse engineer, probe, or interfere with the Services beyond what law permits;
- misuse bugs, rate limits, or admin workflows;
- interfere with call infrastructure, device trust, or encryption mechanisms.

We may investigate, suspend, restrict, or terminate access where necessary to protect users, our systems, or legal compliance.

## 6. User Content

You retain rights you hold in the content you create or upload, subject to the rights needed for us to operate the Services.

By using the Services, you grant Quix Chat a limited, non-exclusive, worldwide license to host, process, transmit, store, format, display, and technically adapt your content solely as needed to provide, secure, and improve the Services, and to comply with law.

This license ends for content we no longer need once it is deleted from the Service, except where retention is required for legal, security, backup, abuse-prevention, or dispute-resolution purposes.

You represent that:

- you have the rights required to share the content;
- your content and conduct do not violate law or these Terms;
- you accept that recipients can copy, record, forward, or disclose what you send.

## 7. Encryption, Calls, and Technical Limits

Quix Chat uses client-side encryption for supported direct-message, private-storage, and media flows. Group chats, subgroups, and Station channels use a different encryption model with different confidentiality guarantees, and Global Chat rooms are not encrypted or stored server-side at all, each as described in the Privacy Policy. However:

- metadata is still processed to operate the Services;
- other users can disclose what you send;
- encryption does not prevent lawful disclosure, user reporting, screenshots, or device compromise;
- view-once and screenshot protections limit, but cannot fully prevent, capture of content by a recipient — for example, with another device;
- if you are reported, the reporting user may share a readable copy of a video you sent them with our moderation team, as described in the Privacy Policy;
- call quality and availability depend on networks, devices, vendors, permissions, and backend state.

Quix Chat does not guarantee uninterrupted, error-free, or globally available service.

## 7A. Platform Safety and User Responsibility

Quix Chat may not actively monitor all user content, particularly in encrypted or private communications. You are responsible for your interactions and content shared through the Services.

You acknowledge that:

- other users may share content that is offensive, harmful, inappropriate, or unlawful;
- Quix Chat does not guarantee the behavior of other users;
- Quix Chat does not guarantee real-time moderation of all interactions;
- you should use caution when interacting with unknown users or sharing sensitive information.

Some features of the Services may allow interaction with other users without prior connection or moderation. You understand that such environments may expose you to content or behavior that is offensive, inappropriate, harmful, or unlawful.

We may provide tools to report abuse, block users, mute users, or restrict interactions, but availability and effectiveness may vary by feature, device, region, and product state.

## 8. Ads, Promotions, and Monetization

Quix Chat may show ads or sponsored placements in selected product surfaces, subject to backend configuration, consent requirements, and applicable law.

Quix Chat is designed not to place ads inside the message thread of direct chat and group chat. Ads may, however, appear in selected lists, conversation side-panels, support surfaces, app-open moments, or certain optional flows if enabled.

If Quix Chat uses rewarded ads for optional actions:

- the flow will be presented in the interface before the ad is shown;
- failing to complete the ad may prevent that optional rewarded action from continuing where the product logic requires ad completion.

We may change monetization features at any time.

## 9. Privacy

Your use of the Services is also governed by the Quix Chat Privacy Policy.

Please read it carefully.

## 10. Software, Updates, and Access Controls

We may:

- release bug fixes, security updates, and feature updates;
- require or strongly encourage updates;
- block or limit outdated versions where necessary for safety, compatibility, or legal compliance;
- enable, disable, or limit features remotely through backend configuration;
- restrict access by country or region.

Some features may be unavailable if you do not install required updates.

## 11. Third-Party Services

The Services may rely on third-party providers for infrastructure, notifications, calling, advertising, hosting, storage, authentication, crash reporting, analytics, or app distribution.

Your use of third-party devices, app stores, carriers, or linked services may also be governed by third-party terms and policies. Quix Chat is not responsible for third-party services we do not control.

## 12. Suspension and Termination

We may suspend, restrict, or terminate your access immediately if:

- you violate these Terms;
- we reasonably suspect fraud, abuse, illegal activity, or security risk;
- we are required to do so by law or competent authority;
- continued access creates harm to users, partners, or Quix Chat.

You may stop using the Services at any time. If supported in your jurisdiction and current product state, you may also delete your account through available account controls.

Some provisions of these Terms survive termination, including sections relating to intellectual property, disclaimers, limitations of liability, indemnity, disputes, and lawful retention.

## 13. Disclaimers

THE SERVICES ARE PROVIDED ON AN "AS IS" AND "AS AVAILABLE" BASIS TO THE MAXIMUM EXTENT PERMITTED BY LAW.

To the maximum extent permitted by law, Quix Chat disclaims warranties of any kind, whether express, implied, or statutory, including warranties of merchantability, fitness for a particular purpose, title, non-infringement, availability, security, reliability, and accuracy.

We do not warrant that:

- the Services will always be available or uninterrupted;
- the Services will be free from bugs or vulnerabilities;
- any content will be preserved without loss;
- any communication will be successfully delivered in all circumstances.

## 14. Limitation of Liability

To the maximum extent permitted by law, Quix Chat and its affiliates, officers, employees, contractors, licensors, and service providers will not be liable for indirect, incidental, special, consequential, exemplary, or punitive damages, or for loss of profits, revenues, goodwill, data, business, or opportunity, arising out of or related to the Services or these Terms.

To the maximum extent permitted by law, Quix Chat's aggregate liability for claims arising from or related to the Services will not exceed the greater of:

- the amount you paid us for the Services in the twelve months before the event giving rise to the claim; or
- USD $100.

Some jurisdictions do not allow certain liability limits, so some of the above may not apply to you.

## 15. Indemnity

To the maximum extent permitted by law, you will defend, indemnify, and hold harmless Quix Chat and its affiliates, officers, employees, contractors, licensors, and service providers from claims, losses, liabilities, damages, judgments, costs, and expenses (including reasonable legal fees) arising from:

- your content;
- your misuse of the Services;
- your violation of these Terms;
- your violation of law or the rights of another person.

## 16. Governing Law and Disputes

These Terms are governed by the laws of the State of New York, without regard to conflict-of-law rules, except to the extent local consumer law applies mandatorily.

Any dispute arising out of or relating to these Terms or the Services will be brought exclusively in the courts of the state and federal courts located in Queens County, New York, unless mandatory law gives you another right.

If you are a consumer, nothing in these Terms removes rights you have under mandatory consumer-protection law.

## 17. Regional Availability and EEA Position

Quix Chat may restrict or defer availability in some territories for legal, operational, or product-readiness reasons.

Quix Chat is not yet launched in the EEA. That decision is intentional and reflects ongoing preparation for EEA-specific compliance and operational readiness. If and when Quix Chat launches in the EEA, we expect to update our Privacy Policy, notices, contracts, and service operations as appropriate for that launch.

## 18. Changes to These Terms

We may update these Terms from time to time. If we make material changes, we may notify you in-app, on a website, or through another reasonable method. Your continued use of the Services after the effective date of updated Terms means you accept the updated Terms, to the extent permitted by law.

## 19. Contact

For legal, support, or Terms-related questions:

- Email: support@quixyr.com
- Address: 9231 53rd Ave, Elmhurst, NY 11373, USA
- Support URL: support@quixyr.com

## Language

These Terms and the Privacy Policy are provided in English. Translations may be provided for convenience. In the event of any conflict or inconsistency between a translated version and the English version, the English version will prevail to the extent permitted by applicable law.
