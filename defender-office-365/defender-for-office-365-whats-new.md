---
title: What's new in Microsoft Defender for Office 365
description: Learn about the new features and functionality available in the latest release of Microsoft Defender for Office 365.
keywords: what's new in Microsoft Defender for Office 365, ga, generally available, capabilities, available, new
search.appverid: met150
f1.keywords: NOCSH
ms.author: chrisda
author: chrisda
manager: deniseb
ms.localizationpriority: medium
ms.date: 07/26/2024
audience: ITPro
ms.collection:
  - m365-security
  - tier1
ms.topic: conceptual
ms.custom: seo-marvel-apr2020
ms.reviewer: vippand
ms.service: defender-office-365
appliesto:
  - ✅ <a href="https://learn.microsoft.com/defender-office-365/mdo-about#defender-for-office-365-plan-1-vs-plan-2-cheat-sheet" target="_blank">Microsoft Defender for Office 365 Plan 1 and Plan 2</a>
  - ✅ <a href="https://learn.microsoft.com/defender-xdr/microsoft-365-defender" target="_blank">Microsoft Defender XDR</a>
---

# What's new in Microsoft Defender for Office 365

[!INCLUDE [MDO Trial banner](../includes/mdo-trial-banner.md)]

This article lists new features in the latest release of Microsoft Defender for Office 365. Features that are currently in preview are denoted with **(preview)**.

Learn more by watching [this video](https://www.youtube.com/watch?v=Tdz6KfruDGo&list=PL3ZTgFEc7LystRja2GnDeUFqk44k7-KXf&index=3).

To search the Microsoft 365 Roadmap for Defender for Office 365 features, use [this link](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=Microsoft%2CDefender%2Cfor%2COffice%2C365).

For more information on what's new with other Microsoft Defender security products, see:

- [What's new in Microsoft Defender XDR](/defender-xdr/whats-new)
- [What's new in Microsoft Defender for Endpoint](/defender-endpoint/whats-new-in-microsoft-defender-endpoint)
- [What's new in Microsoft Defender for Identity](/defender-for-identity/whats-new)
- [What's new in Microsoft Defender for Cloud Apps](/cloud-app-security/release-notes)

## July 2024

- **Tenant Allow/Block List in Microsoft 365 GCC, GCC High, DoD and and Office 365 operated by 21Vianet environments**: The [Tenant Allow/Block List](tenant-allow-block-list-about.md) is now available these environments. They are on parity with the WW commercial experiences.

- **45 days after last used date**: The value **Remove allow entry after** \> **45 days after last used date** is now the default on new allow entries from submissions and existing allow entries in the [Tenant Allow/Block List](tenant-allow-block-list-about.md). The allow entry is triggered and the **LastUsedDate** property is updated when the entity is encountered and identified as malicious during mail flow or at time of click. After the filtering system determines that the entity is clean, the allow entry is automatically removed after 45 days. By default, allow entries for spoofed senders never expire.

- (GA) Learning hub resources have moved from the Microsoft Defender portal to [learn.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2273118). Access Microsoft Defender XDR Ninja training, learning paths, training modules and more. Browse the [list of learning paths](/training/browse/?products=m365-ems-cloud-app-security%2Cdefender-for-cloud-apps%2Cdefender-identity%2Cm365-information-protection%2Cm365-threat-protection%2Cmdatp%2Cdefender-office365&expanded=m365%2Coffice-365), and filter by product, role, level, and subject. 

- (GA) SecOps personnel can now release email messages from quarantine or move messages from quarantine back to user Inboxes directly from :::image type="icon" source="media/m365-cc-sc-take-actions-icon.png" border="false"::: **Take action** in Threat Explorer, Advanced hunting, custom detection, the Email entity page, and the Email summary panel. This capability allows security operators to manage false positives more efficiently and without losing context. For more information, see [Threat hunting: Email remediation](threat-explorer-threat-hunting.md#email-remediation).  

## May 2024

- **Top level domain and subdomain blocking in Tenant Allow/Block List**: You will be able to create block entries under domains & email addresses, using the format `*.TLD`, where `TLD` can be any top-level domain or `*.SD1.TLD, *.SD2.SD1.TLD`, `*.SD3.SD2.SD1.TLD`, and similar patterns for subdomain blocking. The entries block all email received from or sent to any email addresses in the domain or subdomain during mail flow.

- **Automated end user feedback**: The user submission automatic feedback response capability in Microsoft Defender for Office 365 enables organizations to automatically respond to end user submissions of phishing based on the verdict from the automated investigation. [Learn more](air-user-automatic-feedback-response.md).

- We are introducing **Sender's copy clean-up features** in Threat Explorer, email entity, Summary Panel, and Advanced hunting. These new features will streamline the process of managing Sent items, particularly for admins who use the actions **Move to mailbox folder** \> **Soft delete** and **Move to mailbox folder** \> **Inbox**. For more information, see [Threat hunting: The Take action wizard](threat-explorer-threat-hunting.md#the-take-action-wizard). Key highlights:
- Integration with Soft delete: Sender's copy clean-up will be incorporated as part of the Soft delete action.
  - Wide support: This action will be supported across various Defender XDR platforms including Threat Explorer, Take Action wizard from the email entity, Summary Panel, Advanced hunting, and through Microsoft Graph API.
  - Undo capability: An undo action will be available, allowing you to reverse the clean-up by moving items back to the Sent folder.

## April 2024

- **Last used date** added to Tenant Allow/Block List entries for domains and email addresses, files, and URLs.
- **Enhanced clarity in submissions results**: Admins and security operators now see enhanced results within submissions across email, Microsoft Teams messages, email attachments, URLs, and user-reported messages. These updates aim to eliminate any ambiguity associated with the current submission results. The results are refined to ensure clarity, consistency, and conciseness, making the submission results more actionable for you. [Learn more](submissions-admin.md).
- :::image type="icon" source="media/m365-cc-sc-take-actions-icon.png" border="false"::: **Take action** replaces the **Message actions** drop down list on the **Email** tab (view) of the details area of the **All email**, **Malware**, or **Phish** views in [Threat Explorer (Explorer)](threat-explorer-real-time-detections-about.md):
  - SecOps personnel can now create tenant-level block entries on URLs and files via the [Tenant Allow/Block List](tenant-allow-block-list-about.md) directly from Threat Explorer.
  - For 100 or fewer messages selected in Threat Explorer, SecOps personnel can take multiple actions on the selected messages from the same page. For example:
    - Purge email messages or propose email remediation.
    - Submit messages to Microsoft.
    - Trigger investigations.
    - Block entries in the Tenant Allow/Block List.
  - Actions are contextual based on the latest delivery location of the message, but SecOps personnel can use the **Show all response actions** toggle to allow all available actions.
  - For 101 or more messages selected, only email purge and propose remediation options are available.

  > [!TIP]
  > A new panel allows SecOps personnel to look for indicators of compromise at the tenant level, and the block action is readily available.

  For more information, see [Threat hunting: Email remediation](threat-explorer-threat-hunting.md#email-remediation).

## March 2024

- **Copy simulation functionality in Attack simulation training**: Admins can now duplicate existing simulations and customize them to their specific requirements. This feature saves time and effort by using previously launched simulations as templates when creating new ones. [Learn more](attack-simulation-training-simulations.md#copy-simulations).
- Attack simulation training is now available in **Microsoft 365 DoD**. [Learn more](/office365/servicedescriptions/microsoft-defender-for-office-365-features#attack-simulation-training).

## February 2024

- **Hunting and responding to QR code-based attacks**: Security teams are now able to see the URLs extracted from QR codes with **QR code** as URL source on the **URL** tab of the [Email entity page](mdo-email-entity-page.md), and **QRCode** in the **UrlLocation** column of **EmailUrlInfo** table in [Advanced Hunting](/defender-xdr/advanced-hunting-overview). You can also filter for email with URLs embedded within QR codes using the **URL Source** filter value **QR code** in the **All email**, **Malware**, and **Phish** views in [Threat Explorer (Explorer)](threat-explorer-real-time-detections-about.md).

## January 2024

- **New training modules available in Attack Simulation Training**: Teach your users to recognize and protect themselves against QR code phishing attacks. For more information, see [this blog post](https://techcommunity.microsoft.com/t5/microsoft-defender-for-office/train-your-users-to-be-more-resilient-against-qr-code-phishing/ba-p/4022667).
- **Providing intent while submitting is now generally available**: Admins can identify if they're submitting an item to Microsoft for a second opinion or they're submitting the message because it's malicious and was missed by Microsoft. With this change, Microsoft analysis of admin submitted messages (email and Microsoft Teams), URLs, and email attachments is further streamlined and results in a more accurate analysis. [Learn more](submissions-admin.md).

## December 2023

- **QR code related phishing protection within Exchange Online Protection and Microsoft Defender for Office 365**: New detection capabilities using image detection, threat signals, URL analysis now extracts QR codes from URLs and blocks QR code based phishing attacks from the body of an email. To learn more, see our [blog](https://techcommunity.microsoft.com/t5/microsoft-defender-for-office/protect-your-organizations-against-qr-code-phishing-with/ba-p/4007041).
- **Microsoft Defender XDR Unified RBAC is now generally available**: Defender XDR Unified RBAC supports all Defender for Office 365 scenarios that were previously controlled by [Email & collaboration permissions](mdo-portal-permissions.md) and [Exchange Online permissions](/exchange/permissions-exo/permissions-exo). To learn more about the supported workloads and data resources, see [Microsoft Defender XDR Unified role-based access control (RBAC)](/defender-xdr/manage-rbac).

  > [!TIP]
  > Defender XDR Unified RBAC isn't generally available in Microsoft 365 Government Community Cloud High (GCC High) or Department of Defense (DoD).

## November 2023

- **Enhanced Action experience from Email Entity/ Summary Panel**: As part of the change security admins can take multiple actions as part of FP/FN flows. [Learn more](mdo-email-entity-page.md).
- The [Tenant Allow/Block List](tenant-allow-block-list-about.md) supports more entries in each category (Domains & email addresses, Files, and URLs:
  - Microsoft Defender for Office 365 Plan 2 supports 10,000 block entries and 5,000 allow entries (via admin submissions) in each category.
  - Microsoft Defender for Office 365 Plan 1 supports 1,000 block entries and 1,000 allow entries (via admin submissions) in each category.
  - Exchange Online Protection remains at 500 block entries and 500 allow entries (via admin submissions) in each category.

## October 2023

- **Create and manage simulations using the Graph API** in Attack simulation training. [Learn more](/graph/api/attacksimulationroot-post-simulation)
- **Exchange Online permission management in Defender for Office 365 is now supported in Microsoft Defender XDR Unified role-based access control (RBAC)**: In addition to the existing support for [Email & collaboration permissions](mdo-portal-permissions.md), Defender XDR Unified RBAC now also supports protection-related [Exchange Online permissions](/exchange/permissions-exo/permissions-exo). To learn more about the supported Exchange Online permissions, see [Exchange Online permissions mapping](/defender-xdr/compare-rbac-roles#exchange-online-permissions-mapping).

## September 2023

- URL top-level domain blocking is available in the **Tenant allow block list**. [Learn more](tenant-allow-block-list-urls-configure.md).
- Attack simulation training is now available in **Microsoft 365 GCC High**. [Learn more](/office365/servicedescriptions/microsoft-defender-for-office-365-features#attack-simulation-training).

## August 2023

- If the [User reported settings](submissions-user-reported-messages-custom-mailbox.md) in the organization send user reported messages (email and [Microsoft Teams](submissions-teams.md)) to Microsoft (exclusively or in addition to the reporting mailbox), we now do the same checks as when admins submit messages to Microsoft for analysis from the **Submissions** page.
- **Default intra-organizational protection**: By default, messages sent between internal users that are identified as high confidence phishing are quarantined. Admins change this setting in the default anti-spam policy or in custom policies (opt-out of intra-org protection or include other spam filtering verdicts). For configuration information, see [Configure anti-spam policies in EOP](anti-spam-policies-configure.md).

## July 2023

- Use anti-phishing policies to control what happens to messages where the sender fails explicit [DMARC](email-authentication-dmarc-configure.md) checks and the DMARC policy is set to `p=quarantine` or `p=reject`. For more information, see [Spoof protection and sender DMARC policies](anti-phishing-policies-about.md#spoof-protection-and-sender-dmarc-policies).
- [User tags](user-tags-about.md) are now fully integrated with Defender for Office 365 reports, including:
  - [Threat protection status report](reports-email-security.md#threat-protection-status-report)
  - [Compromised users report](reports-email-security.md#compromised-users-report)
  - [Top senders and recipients report](reports-email-security.md#top-senders-and-recipients-report)
  - [URL protection report](reports-email-security.md#url-protection-report)

## May 2023

- Built-in reporting in Outlook on the web supports reporting messages from shared mailboxes or other mailboxes by a delegate.
  - Shared mailboxes require Send As or Send On Behalf permission for the user.
  - Other mailboxes require Send As or Send On Behalf permission _and_ Read and Manage permissions for the delegate.

## April 2023

- [Using machine learning to drive more effective simulations in Attack Simulation and Training](https://techcommunity.microsoft.com/t5/microsoft-defender-for-office/attack-simulation-training-using-machine-learning-to-drive-more/ba-p/3791023): Make use of intelligent predicted compromise rate (PCR) and Microsoft Defender for Office 365 payload recommendations for utilizing high-quality payloads in your simulation.
- [Training only campaigns available with an expanded library](https://techcommunity.microsoft.com/t5/microsoft-defender-for-office/training-only-campaign-is-now-available-with-an-expanded/ba-p/3795237): You can now directly assign training content to your organization without needing to tie training to a phishing simulation campaign. We have also expanded our training module library to more than 70 different modules.

## March 2023

- **Collaboration security for Microsoft Teams**: With the increased use of collaboration tools like Microsoft Teams, the possibility of malicious attacks using URLs and messages has increased as well. Microsoft Defender for Office 365 is extending its [Safe Links](safe-links-about.md) protection with increased capabilities for zero-hour auto purge (ZAP), quarantine, and end user reporting of potential malicious messages to their admins. For more information, see [Microsoft Defender for Office 365 support for Microsoft Teams (Preview)](mdo-support-teams-about.md).
- **Built-in protection: Safe Links time of click protection enabled for email**: By default, Microsoft now protects URLs in email messages at time of click as part of this update to Safe Links settings (_EnableSafeLinksForEmail_) within the Built-in protection preset security policy. To learn about the specific Safe Links protections in the Built-in protection policy, see [Safe Links policy settings](recommended-settings-for-eop-and-office365.md#safe-links-policy-settings).
- **Quarantine notifications enabled in preset security policies**: If your organization has enabled or will enable the Standard or Strict preset security policies, the policies will be automatically updated to use the new DefaultFullAccessWithNotificationPolicy quarantine policy (notifications enabled) wherever the DefaultFullAccessPolicy (notifications disabled) was used. To learn more about quarantine notifications, see [Quarantine notifications](quarantine-quarantine-notifications.md). For more information about specific settings in preset security policies, see [Microsoft recommendations for EOP and Defender for Office 365 security settings](recommended-settings-for-eop-and-office365.md).

## January 2023

- [Automatic Tenant Allow/Block List expiration management is now available in Microsoft Defender for Office 365](https://techcommunity.microsoft.com/t5/microsoft-defender-for-office/automatic-tenant-allow-block-list-expiration-management-is-now/ba-p/3723447): Microsoft now automatically removes allow entries from the Tenant Allow/Block List once the system has learned from it. Alternatively, Microsoft extends the expiration time of the allow entries if the system hasn't learned yet. This behavior prevents legitimate email from going to junk or quarantine.
- **Configuring third-party phishing simulations in Advanced Delivery:** We expanded "Simulation URLs to allow" limit to 30 URLs. To learn how to configure, see [Configure the delivery of third-party phishing simulations to users and unfiltered messages to SecOps mailboxes](advanced-delivery-policy-configure.md)
- [Enhanced user telemetry in the simulation reports in Attack Simulation Training](https://techcommunity.microsoft.com/t5/microsoft-defender-for-office/attack-simulation-training-new-insights-into-targeted-user/ba-p/3673105): As part of our enhanced user telemetry, administrators can now view additional details about how their targeted users are interacting with the phishing payload from phishing simulation campaigns.

## December 2022

- The new Microsoft Defender XDR role-based access control (RBAC) model, with support for Microsoft Defender for Office, is now available in public preview. For more information, see [Microsoft Defender XDR role-based access control (RBAC)](/defender-xdr/manage-rbac).

- [Use the built-in Report button in Outlook on the web](submissions-outlook-report-messages.md#use-the-built-in-report-button-in-outlook-on-the-web): Use the built-in Report button in Outlook on the web to report messages as phish, junk, and not junk.

## October 2022

- [Automated Investigations email cluster action deduplication](air-review-approve-pending-completed-actions.md): We have added additional checks. If the same investigation cluster is already approved during the past hour, new duplicate remediation isn't processed again.

- [Manage allows and blocks in the Tenant Allow/Block List](tenant-allow-block-list-about.md):
  - With **allow expiry management** (currently in Private Preview), if Microsoft hasn't learned from the allow, Microsoft automatically extends the expiry time of allows, which are going to expire soon, by 30 days to prevent legitimate email from going to junk or quarantine again.
  - Customers in government cloud environments are now able to create allow and block entries for URLs and attachments in the Tenant Allow/Block List using admin submissions for URLs and email attachments. The data submitted through the submissions experience doesn't leave the customer tenant, thus satisfying the data residency commitments for government cloud clients.
- **Enhancement in URL click alerts:**
  - With the new lookback scenario, the "A potentially malicious URL click was detected" alert now includes any clicks during the _past 48 hours_ (for email) from the time the malicious URL verdict is identified.

## September 2022

- **Anti-spoofing enhancement for internal domains and senders:**
  - For spoofing protection, the allowed senders or domains defined in the [anti-spam policy](anti-spam-policies-configure.md) and within user allow lists must now pass authentication in order for the allowed messages to be honored. The change only affects messages that are considered to be internal (the sender or sender's domain is in an accepted domain in the organization). All other messages continue to be handled as they are today.

- **Automatic redirection from Office action center to unified action center:** The action center in the Email & Collaboration section **Email & Collaboration** > **Review** > **Action center** <https://security.microsoft.com/threatincidents> is automatically redirected to **Actions & Submissions** \> **Action center** \> **History** <https://security.microsoft.com/action-center/history>.

- **Automatic redirection from Office 365 Security & Compliance Center to Microsoft Defender portal:** Automatic redirection begins for users accessing the security solutions in Office 365 Security & Compliance center (protection.office.com) to the appropriate solutions in Microsoft Defender portal (security.microsoft.com). This change is for all security workflows like (for example, Alerts, Threat Management, and Reports).

  - Redirection URLs:
    - GCC Environment:
      - From Office 365 Security & Compliance Center URL: protection.office.com
      - To Microsoft Defender XDR URL: security.microsoft.com
    - GCC-High Environment:
      - From Office 365 Security & Compliance Center URL: scc.office365.us
      - To Microsoft Defender XDR URL: security.microsoft.us
    - DoD Environment:
      - From Office 365 Security & Compliance Center URL: scc.protection.apps.mil
      - To Microsoft Defender XDR URL: security.apps.mil
- Items in the Office 365 Security & Compliance Center that aren't related to security aren't redirected to Microsoft Defender XDR. For compliance solutions redirection to Microsoft 365 Compliance Center, see Message Center post 244886.
- This change is a continuation of [Microsoft Defender XDR delivers unified XDR experience to GCC, GCC High and DoD customers - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/public-sector-blog/microsoft-365-defender-delivers-unified-xdr-experience-to-gcc/ba-p/3263702), announced in March 2022.
- This change enables users to view and manage additional Microsoft Defender XDR security solutions in one portal.
- This change impacts all customers who use the Office 365 Security & Compliance Center (protection.office.com), including Microsoft Defender for Office (Plan 1 or Plan 2), Microsoft 365 E3 / E5, Office 365 E3/ E5, and Exchange Online Protection. For the full list, see [Microsoft 365 guidance for security & compliance](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance)
- This change impacts all users who sign in to the Office 365 Security and Compliance portal (protection.office.com), including security teams and end-users who access the Email Quarantine experience, at the **Microsoft Defender Portal** \> **Review** \> **Quarantine**.
- Redirection is enabled by default and impacts all users of the Tenant.
- Global Administrators<sup>\*</sup> and Security Administrators can turn on or off redirection in the Microsoft Defender portal by navigating to **Settings** \> **Email & collaboration** > **Portal redirection** and switch the redirection toggle.

  > [!IMPORTANT]
  > <sup>\*</sup> Microsoft recommends that you use roles with the fewest permissions. Using lower permissioned accounts helps improve security for your organization. Global Administrator is a highly privileged role that should be limited to emergency scenarios when you can't use an existing role.

- **Built-in protection**: A profile that enables a base level of Safe Links and Safe Attachments protection that's on by default for all Defender for Office 365 customers. To learn more about this new policy and order of precedence, see [Preset security policies](preset-security-policies.md). To learn about the specific Safe Links and Safe Attachment controls that are set, see [Safe Attachments settings](recommended-settings-for-eop-and-office365.md#safe-attachments-settings) and [Safe Links policy settings](recommended-settings-for-eop-and-office365.md#safe-links-policy-settings).
- **Bulk Complaint Level** is now available in the EmailEvents table in Advanced Hunting with numeric BCL values from 0 to 9. A higher BCL score indicates that bulk message is more likely to generate complaints and is more likely to be spam.

## July 2022

- [Introducing actions into the Email entity page](mdo-email-entity-page.md): Admins can take preventative, remediation, and submission actions from the Email entity page.

## June 2022

- [Create allow entries for spoofed senders](tenant-allow-block-list-email-spoof-configure.md#create-allow-entries-for-spoofed-senders): Create allowed spoofed sender entries using the Tenant Allow/Block List.

- [Impersonation allows using admin submission](tenant-allow-block-list-email-spoof-configure.md#about-impersonated-domains-or-senders): Add allows for impersonated senders using the **Submissions** page in Microsoft Defender XDR.

- [Submit user reported messages to Microsoft for analysis](submissions-admin.md#submit-user-reported-messages-to-microsoft-for-analysis): Configure a reporting mailbox to intercept user-reported messages without sending the messages to Microsoft for analysis.

- View the associated alerts for [user reported messages](submissions-admin.md#actions-for-user-reported-messages-in-defender-for-office-365) and [admin submissions](submissions-admin.md#actions-for-admin-submissions-in-defender-for-office-365): View the corresponding alert for each user reported phishing message and admin email submission.

- [Configurable impersonation protection custom users and domains and increased scope within Preset policies](https://techcommunity.microsoft.com/t5/microsoft-defender-for-office/configurable-impersonation-protection-and-scope-for-preset/ba-p/3294459):
  - (Choose to) Apply Preset Strict/Standard policies to entire organization and avoid the hassle of selecting specific recipient users, groups, or domains, thereby securing all recipient users of your organization.
  - Configure impersonation protection settings for custom users and custom domains within Preset Strict/Standard policies and automatically protect your targeted users and targeted domain against impersonation attacks.

- [Simplifying the quarantine experience (part two) in Microsoft Defender XDR for office 365](https://techcommunity.microsoft.com/t5/microsoft-defender-for-office/simplifying-the-quarantine-experience-part-two/ba-p/3354687): Highlights additional features to make the quarantine experience even easier to use.

- [Introducing differentiated protection for priority accounts in Microsoft Defender for Office 365](https://techcommunity.microsoft.com/t5/microsoft-defender-for-office/introducing-differentiated-protection-for-priority-accounts-in/ba-p/3283838): Introducing GCC, GCC-H, and DoD availability of differentiated protection for priority accounts.

## April 2022

- [Introducing the URLClickEvents table in Microsoft Defender XDR Advanced Hunting](https://techcommunity.microsoft.com/t5/microsoft-defender-for-office/introducing-the-urlclickevents-table-in-advanced-hunting-with/ba-p/3295096): Introducing the UrlClickEvents table in advanced hunting with Microsoft Defender for Office 365.
- [Manual email remediation enhancements](remediate-malicious-email-delivered-office-365.md): Bringing manual email purge actions taken in Microsoft Defender for Office 365 to the Microsoft Defender XDR (M365D) unified Action Center using a new action-focused investigation.
- [Introducing differentiated protection for priority accounts in Microsoft Defender for Office 365](https://techcommunity.microsoft.com/t5/microsoft-defender-for-office/introducing-differentiated-protection-for-priority-accounts-in/ba-p/3283838): Introducing the general availability of differentiated protection for priority accounts.

## March 2022

- [Streamlined the submission experience in Microsoft Defender for Office 365](https://techcommunity.microsoft.com/t5/microsoft-defender-for-office/streamlining-the-submissions-experience-in-microsoft-defender/ba-p/3152080): Introducing the new unified and streamlined submission process to make your experience simpler.

## January 2022

- [Updated Hunting and Investigation Experiences for Microsoft Defender for Office 365](https://techcommunity.microsoft.com/t5/microsoft-defender-for-office/updated-hunting-and-investigation-experiences-for-microsoft/ba-p/3002015): Introducing the email summary panel for experiences in Defender for Office 365, along with experience updates for Threat Explorer and Real-time detections.

## October 2021

- [Advanced Delivery DKIM enhancement](advanced-delivery-policy-configure.md): Added support for DKIM domain entry as part of third-party phishing simulation configuration.
- [Secure by Default](secure-by-default.md): Extended Secure by Default for Exchange mail flow rules (also known as transport rules).

## September 2021

- [Improved reporting experience in Defender for Office 365](https://techcommunity.microsoft.com/t5/microsoft-defender-for-office/improving-the-reporting-experience-in-microsoft-defender-for/ba-p/2760898)
- [Quarantine policies](quarantine-policies.md): Admins can configure granular control for recipient access to quarantined messages and customize end-user spam notifications.
  - [Video of admin experience](https://youtu.be/vnar4HowfpY)
  - [Video of end-user experience](https://youtu.be/s-vozLO43rI)
  - Other new capabilities coming to the quarantine experience are described in this blog post: [Simplifying the Quarantine experience](https://techcommunity.microsoft.com/t5/microsoft-defender-for-office/simplifying-the-quarantine-experience/ba-p/2676388).
- Portal redirection by default begins, redirecting users from Security & Compliance to Microsoft Defender XDR <https://security.microsoft.com>.

## August 2021

- [Admin review for reported messages](submissions-admin-review-user-reported-messages.md): Admins can now send templated messages back to end users after they review reported messages. The templates can be customized for your organization and based on your admin's verdict as well.
- You can now add allow entries to the Tenant Allow/Block List if the blocked message was submitted as part of the admin submission process. Depending on the nature of the block, the submitted URL, file, and/or sender allow will be added to the Tenant Allow/Block List. In most cases, the allows are added to give the system some time and allow it naturally if warranted. In some cases, Microsoft manages the allow for you. For more information, see:
  - [Report good URLs to Microsoft](submissions-admin.md#report-good-urls-to-microsoft)
  - [Report good email attachments to Microsoft](submissions-admin.md#report-good-email-attachments-to-microsoft)
  - [Report good email to Microsoft](submissions-admin.md#report-good-email-to-microsoft)

## July 2021

- [Email analysis improvements in automated investigations](email-analysis-investigations.md)
- [Advanced Delivery](advanced-delivery-policy-configure.md): Introducing a new capability for configuring the delivery of third-party phishing simulations to users and unfiltered messages to security operation mailboxes.
- [Safe Links for Microsoft Teams](safe-links-about.md#safe-links-settings-for-microsoft-teams)
- New alert policies for the following scenarios: compromised mailboxes, Forms phishing, malicious mails delivered due to overrides and rounding out ZAP
  - Suspicious email forwarding activity
  - User restricted from sharing forms and collecting responses
  - Form blocked due to potential phishing attempt
  - Form flagged and confirmed as phishing
  - [New alert policies for ZAP](/purview/new-defender-alert-policies)
- Microsoft Defender for Office 365 alerts is now integrated into Microsoft Defender XDR - [Microsoft Defender XDR Unified Alerts Queue and Unified Alerts Queue](/defender-xdr/investigate-alerts)
- [User Tags](user-tags-about.md) are now integrated into Microsoft Defender for Office 365 alerting experiences, including: the alerts queue and details in Office 365 Security & Compliance, and scoping custom alert policies to user tags to create targeted alert policies.
  - Tags are also available in the unified alerts queue in the Microsoft Defender portal (Microsoft Defender for Office 365 Plan 2)

## June 2021

- New first contact safety tip setting within anti-phishing policies. This safety tip is shown when recipients first receive an email from a sender or don't often receive email from a sender. For more information on this setting and how to configure it, see the following articles:
  - [First contact safety tip](anti-phishing-policies-about.md#first-contact-safety-tip)
  - [Configure anti-phishing policies in EOP](anti-phishing-policies-eop-configure.md)
  - [Configure anti-phishing policies in Microsoft Defender for Office 365](anti-phishing-policies-mdo-configure.md)

## April/May 2021

- [Email entity page](mdo-email-entity-page.md): A unified 360-degree view of an email with enriched information around threats, authentication and detections, detonation details, and a brand-new email preview experience.
- [Office 365 Management API](/office/office-365-management-api/office-365-management-activity-api-schema#email-message-events): Updates to EmailEvents (RecordType 28) to add delivery action, original and latest delivery locations, and updated detection details.
- [Threat Analytics for Defender for Office 365](/defender-xdr/threat-analytics): View active threat actors, popular techniques and attack surfaces, along with extensive reporting from Microsoft researchers around ongoing campaigns.

## February/March 2021

- Alert ID integration (search using Alert ID and Alert-Explorer navigation) in [hunting experiences](threat-explorer-real-time-detections-about.md)
- Increasing the limits for Export of records from 9990 to 200,000 in [hunting experiences](threat-explorer-real-time-detections-about.md)
- Extending the Explorer (and Real-time detections) data retention and search limit for trial tenants from 7 (previous limit) to 30 days in [hunting experiences](threat-explorer-real-time-detections-about.md)
- New hunting pivots called **Impersonated domain** and **Impersonated user** within Explorer and Real-time detections to search for impersonation attacks against protected users or domains. For more information, see [Phish view in Threat Explorer and Real-time detections](threat-explorer-real-time-detections-about.md#phish-view-in-threat-explorer-and-real-time-detections).

## Microsoft Defender for Office 365 Plan 1 and Plan 2

Did you know that Microsoft Defender for Office 365 is available in two plans? [Learn more about what each plan includes](mdo-about.md#defender-for-office-365-plan-1-vs-plan-2-cheat-sheet).

## See also

- [Microsoft 365 roadmap](https://www.microsoft.com/microsoft-365/roadmap)
- [Microsoft Defender for Office 365 Service Description](/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)
