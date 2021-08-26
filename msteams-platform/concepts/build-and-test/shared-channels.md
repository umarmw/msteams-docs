---
title: Shared channels
author: Rajeshwari-v
description:  Collaborating with shared channels.
ms.author: surbhigupta
localization_priority: Normal
ms.topic: conceptual
---

# Shared channels

> [!NOTE]     
> Shared channels are currently available in [developer preview](~/resources/dev-preview/developer-preview-intro.md) only.

Shared channels in Teams allow members of a channel to collaborate with users across other Teams and organizations. You can create and share a shared channel with:

* Members of another Team within the same organization
* Individuals within the same organization
* Individuals and other Teams of other organizations 

This allows external users outside of your organization to collaborate with internal users in Teams without changing their user context. This is adventageous because, unlike when using guest accounts, where members must sign out of Teams and sign in again using a guest account, shared channels facilitates this collaboration seamlessly. Teams applications can now extend this powerful collaboration space. 

[Place holder for image]

## Get context in shared channels

When the content UX is loaded in a shared channel, use the data received from `getContext` call for  shared channel changes. `getContext` call publishes two new properties, `hostTeamGroupID ` and `hostTenantID`, which are used to retrieve channel membership from the Microsoft Graph API. "Host Team" refers to the Team that created the shared channel. For more information, see [Get context in shared channels](~/tabs/how-to/access-teams-context.md#get-context-in-shared-channels).  

## Apps and permissions in shared channels

You can collaborate with external members outside of your organization using shared channels. App permissions in shared channels follow the host team's app roster and host tenant's app policy. 

> [!NOTE]
> The [Activity Feed Notification Graph API](https://docs.microsoft.com/en-us/graph/teams-send-activityfeednotifications) does not support cross-tenant notifications for apps in a Shared Channel.

## Get shared channel membership

You can get direct shared channel membership by using the `hostTeamGroupID` from `getContext` and following these steps:

1. Get direct members with [GET channel members API](/graph/api/channel-list-members?view=graph-rest-beta&tabs=http&preserve-view=true) API. 

    ```http
    GET /teams/{host-team-group-id}/channels/{channel-id}/members
    ```
2. Get each shared team with GET `sharedWithTeams` API.

    ```http
    GET /teams/{host-team-group-id}/channels/{channel-id}/sharedWithTeams
    ```
3. Use GET members of each shared team (Team X) with GET `sharedWithTeams` API.

    ```http
   GET /teams/{host-team-group-id}/channels/{channel-id}/sharedWithTeams/{teamX}/members
    ```

## Classify members in the shared channel as in-tenant or out-tenant

You can classify members as in-tenant or out-tenant by comparing `tenantID` of the member or team with `hostTeamTenantID` as follows: 

1. Get the member you wish to compare.
```http
GET /teams/{host-team-group-id}/channels/{channel-id}/members
```
2.	Using `getContext`, compare the `tenantID` of the member to the `hostTenantID` property.

## AAD native identity

Apps must function cross-tenant in installation and usage. The following table lists the channel types and their corresponding group IDs: 
     
|Channel type| groupId | hostTeamGroupId |
|----------|---------|-----------------|
|Regular | Team AAD group ID | Team AAD group ID |
|Shared	| Empty | Host Team AAD group ID |