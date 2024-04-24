---
title: Overview - Advanced hunting
description: Learn about advanced hunting queries in Microsoft 365 and how to use them to proactively find threats and weaknesses in your network
ms.service: defender-xdr
ms.pagetype: security
f1.keywords: 
  - NOCSH
ms.author: maccruz
author: schmurky
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: 
  - m365-security
  - m365initiative-m365-defender
  - tier1
ms.topic: conceptual
ms.custom: seo-marvel-apr2020
search.appverid: met150
ms.date: 03/28/2024
---

# Proactively hunt for threats with advanced hunting in Microsoft Defender XDR

[!INCLUDE [Microsoft Defender XDR rebranding](../includes/microsoft-defender.md)]


**Applies to:**
- Microsoft Defender XDR

Advanced hunting is a query-based threat hunting tool that lets you explore up to 30 days of raw data. You can proactively inspect events in your network to locate threat indicators and entities. The flexible access to data enables unconstrained hunting for both known and potential threats.

Advanced hunting supports two modes, guided and advanced. Use [guided mode](/defender-xdr/advanced-hunting-query-builder) if you are not yet familiar with Kusto Query Language (KQL) or prefer the convenience of a query builder. Use [advanced mode](/defender-xdr/advanced-hunting-query-language) if you are comfortable using KQL to create queries from scratch. 

**To start hunting, read [Choose between guided and advanced modes to hunt in Microsoft Defender XDR](/defender-xdr/advanced-hunting-modes).**

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4G6DO]

You can use the same threat hunting queries to build custom detection rules. These rules run automatically to check for and then respond to suspected breach activity, misconfigured machines, and other findings.

Advanced hunting supports queries that check a broader data set coming from:

- Microsoft Defender for Endpoint
- Microsoft Defender for Office 365
- Microsoft Defender for Cloud Apps
- Microsoft Defender for Identity

To use advanced hunting, [turn on Microsoft Defender XDR](/defender-xdr/m365d-enable).


For more information on advanced hunting in Microsoft Defender for Cloud Apps data, see the [video](https://www.microsoft.com/en-us/videoplayer/embed/RWFISa). 



## Get access
To use advanced hunting or other [Microsoft Defender XDR](/defender-xdr/microsoft-365-defender) capabilities, you need an appropriate role in Microsoft Entra ID. [Read about required roles and permissions for advanced hunting](/defender-xdr/custom-roles).

Also, your access to endpoint data is determined by role-based access control (RBAC) settings in Microsoft Defender for Endpoint. [Read about managing access to Microsoft Defender XDR](/defender-xdr/m365d-permissions).


## Data freshness and update frequency
Advanced hunting data can be categorized into two distinct types, each consolidated differently.

- **Event or activity data**—populates tables about alerts, security events, system events, and routine assessments. Advanced hunting receives this data almost immediately after the sensors that collect them successfully transmit them to the corresponding cloud services. For example, you can query event data from healthy sensors on workstations or domain controllers almost immediately after they are available on Microsoft Defender for Endpoint and Microsoft Defender for Identity.
- **Entity data**—populates tables with information about users and devices. This data comes from both relatively static data sources and dynamic sources, such as Active Directory entries and event logs. To provide fresh data, tables are updated with any new information every 15 minutes, adding rows that might not be fully populated. Every 24 hours, data is consolidated to insert a record that contains the latest, most comprehensive data set about each entity.


## Time zone
### Queries
Advanced hunting data uses the UTC (Universal Time Coordinated) timezone. 
![Screenshot of custom time range.](/defender/media/custom-time-range.png)

Queries should be created in UTC.

### Results
Advanced hunting results are converted to the [timezone](/defender-xdr/m365d-time-zone) set in Microsoft Defender XDR. 




## Related topics
- [Choose between guided and advanced hunting modes](/defender-xdr/advanced-hunting-modes)
- [Build hunting queries using guided mode](/defender-xdr/advanced-hunting-query-builder)
- [Learn the query language](/defender-xdr/advanced-hunting-query-language)
- [Understand the schema](/defender-xdr/advanced-hunting-schema-tables)
- [Microsoft Graph security API](/graph/api/resources/security-api-overview#advanced-hunting)
- [Custom detections overview](/defender-xdr/custom-detections-overview)
[!INCLUDE [Microsoft Defender XDR rebranding](../includes/defender-m3d-techcommunity.md)]