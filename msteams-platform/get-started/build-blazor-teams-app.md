---
title: Build your first Teams app with Blazor
author: adrianhall
description: Build a Microsoft Teams app that displays a "Hello, World!" message using the Microsoft Teams Toolkit and .NET Blazor.
ms.author: adhal
ms.date: 04/27/2021
ms.topic: quickstart
ms.localizationpriority: none
---

# Build and run your first Microsoft Teams app with Blazor

After you set up your project workspace with Teams Toolkit, build your tab project. You'll need to sign in to your Microsoft 365 account.

:::image type="content" source="../assets/images/get-started/app-roadmap/roadmap-p3.png" alt-text="Image showing phase 3 of building an app." border="false":::

In this page, you'll learn to:
- [Build and run your first app](#build-and-run-your-app-locally-in-visual-studio-code)

## Sign in to your Microsoft 365 account

After the project is created, set up single sign-on with Microsoft 365:

   1. Select **Project** > **TeamsFx** > **Configure for SSO...**.
   1. Sign in to your Microsoft 365 administrator account when prompted.

## Build and run your app locally in Visual Studio Code

To build and run your app locally:

1. From Visual Studio Code, press the **F5** key to run your application in debug mode.
    <!-- markdownlint-disable MD033 -->
    <details>
    <summary>Learn what happens when you run your app locally in the debugger.</summary>

    When you select **F5**, the Teams Toolkit:

    1. Registers your application with Azure Active Directory.
    1. Registers your application for "sideloading" in Microsoft Teams.
    1. Starts your application backend running locally.
    1. Starts your application front-end hosted locally.
    1. Starts Microsoft Teams in a web browser with a command to instruct Teams to side load the application (the URL is registered inside the application manifest).

    </details>
1. If requested, install the self-signed SSL certificate for local debugging.

   :::image type="content" source="../assets/images/teams-toolkit-v2/ssl-prompt.png" alt-text="Screenshot showing how the prompt to install an SSL certificate to enable Teams to load your application from localhost.":::
1. Teams is loaded in a web browser. After you sign in, if you're prompted to open Microsoft Teams, select **Cancel** to remain in the browser. Sign in with your Microsoft 365 account.
1. When prompted to install the app to Teams, select **Add**.
   Your app will now be displayed:

   :::image type="content" source="../assets/images/teams-toolkit-v2/blazor-completed-app.png" alt-text="Screenshot of the completed app":::

   You can do normal debugging activities, such as setting breakpoints, as if it were any other web application. The app supports hot reloading.  If you change any file within the project, the page will be reloaded.

<!-- markdownlint-disable MD033 -->
<details>
<summary>Learn how to troubleshoot if your app doesn't run locally.</summary>

To run your app in Teams, you need a Microsoft 365 development account that allows app sideloading. For more information about account opening, see [Blazor App Prerequisites](blazor-app-prerequisites.md).

</details>

| **<<** | **>>** |
|:--- | ---:|
| **Back** : [1. Create your first Teams Blazor app](first-app-blazor.md) | [4. Deploy your first Teams Blazor app](deploy-blazor-app.md) : **Next**|
|

## See also

* [Tutorials Overview](code-samples.md)
* [Code Samples](https://github.com/OfficeDev/Microsoft-Teams-Samples)