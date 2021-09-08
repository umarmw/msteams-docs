---
title: Guidelines for apps linked with SaaS offer
author: Rajeshwari-v
description: Describes guidelines for Teams app linked to SaaS offer
ms.topic: conceptual
localization_priority: Normal
ms.author: surbhigupta
---

# Guidelines for apps linked with SaaS offer

If your Teams app is linked to SaaS offer ensure it adheres to the following guidelines: 

* Teams monetization capabilities are designed to support a per-user pricing model for assigning licenses to users. 

* ISVs should support the ability for multiple users (Subscribers) in the same tenant to manage their own subscription and assign licenses to users in the tenant. 

* The offer must meet all the [technical requirements](http://aka.ms/saasoffer) for Teams apps linked to a SaaS offer. 

* The Teams apps linked to SaaS offer must meet all requirements defined in [1000 Software as a Service (SaaS)](/legal/marketplace/certification-policies#1000-software-as-a-service-saas). 

## Link SaaS offer to Teams app 

* `subscriptionOffer` details mentioned in manifest file must be accurate. 

In your app manifest, add or update node `subscriptionOffer` with value `<publisher id>.<offer id>` as follows: 

For example, if your publisher ID is `contoso1234` and your offer ID is `offer01`, the value that you specify in your app manifest must be `contoso1234.offer01`.

Following image illustrates the discussed condition:

![Link SaaS offer to Teams app1](~/assets/images/store-detail-page/link-saas-offer-to-teams-app-screen1.png)

* Linked SaaS offer to the Teams app must be live in AppSource and preview offers are not accepted for store approval. 

Following image illustrates the discussed condition:

![Link SaaS offer to Teams app2](~/assets/images/store-detail-page/link-saas-offer-to-teams-app-screen2.png)

## Offer metadata 

* Offer metadata should match across the Teams manifest, the Teams app listing in AppSource, and the SaaS offer in AppSource.

* Teams app and SaaS offer must be from same publisher/developer. The SaaS offer referenced in the App manifest should belong to the same publisher as the Teams app being submitted to the commercial marketplace. 

* As your submitted offer is a Teams app linked to SaaS offer, you must select **Additional purchases** as **Yes, my product requires purchase of a service or offers additional in-app purchases​** in Partner Center product setup section of your offer listing. 

Following image illustrates the discussed condition:

   ![Offer metadata](~/assets/images/store-detail-page/offer-metadata.png)

* Plan descriptions and pricing details must provide enough information for users to clearly understand the offer listings.   

* Any limitations, dependencies on additional services and exceptions to features offered must be accurately called out in plan descriptions.     

* The Teams apps linked to SaaS offer is designed to support licenses assigned on a named, per-user basis, if your SaaS offer is built with any another method or has specialized purchase flows, you must clearly state this in the app metadata and subscription plan details.  

## Purchase flows 

### Teams Client purchase expereince

Admin/non-admin users should be able to buy a subscription plan with minimum license quantity and assign them to self or other users in the tenant. 

Admin/non-admin should be able to buy a subscription with bulk license quantity and assign them to self or other users in the tenant. 

Admin/Non-Admin should be able to complete end to end purchase experience from Teams Client, post purchase should be able to manage the licenses/s in MAC and should have the feasibility to activate, manage and assign licenses in SaaS application.  

### Teams Admin Center purchase expereince 

* Admins must be able to purchase bulk licenses from the Teams Admin Center.  

* Admins should be able to complete end to end purchase experience from TAC, should be able to manage the licenses in MAC and should have the feasibility to activate, manage and assign licenses in SaaS application.  

> [!NOTE]
> Your offer must provide messages, further guidance to users in all applicable states of purchase flow and must guide a new user. 

## SaaS offer home page and license management  

* Subscriber should be able to navigate to SaaS web application landing page by selecting **configure now** in Teams.     
Following image illustrates the home page:

   ![Home page](~/assets/images/store-detail-page/home-page.png)

* Users completing the purchase must be able to Activate and configure their subscription on your SaaS application landing page.     
Following image illustrates the home page:

   ![Configure subscription ](~/assets/images/store-detail-page/configure-subscription.png)

> [TIP] 

> * Provide introduction to subscriber on how to use the product 

>  Allow the subscriber to assign licenses 

> * Provide way to engage with support for issues (FAQ, knowledgebase, and/or email address) 

* Users completing a purchase must be able to manage the licenses and must have the following options in SaaS application: 

    * Assign and remove licenses 

    * Reassign licenses among users

    * Authorize users to manage licenses 

Following image illustrates the license management:

   ![Manage license](~/assets/images/store-detail-page/manage-license.png)

## Manage Subscriptions 

* Users completing the purchase must be able to Manage Subscriptions.  

Subscribers must be able to do the following: 

   * Adjust licenses, buy, remove licenses  

   * Change subscription plan

   * Cancel, re-purchase the subscription 

   * Renew subscriptions

* Any modifications in purchased licenses or plans must be reflected in SaaS application with correct license counts, subscription details, and the right user assignments. 

## Usability and functionality  

* After successful purchase and assignment of licenses, users must have access to the subscribed plan features described in plan listing. 

* Post license assignment, users should have a value addition and significant benefits of subscription plan when compared to users without license assignment. 

* From your Teams app, provide link back to the SaaS application landing page for subscriber to manage the licenses in the future. 

## Provide sufficient Details to Configure the SaaS application and Test 

If setup of your app for testing purposes is complex or non-intuitive, provide an end-to-end functional document, linked SaaS offer configuration steps, and instructions for license and user management as part of your **Notes for Certification**.   

> [TIP]  

> Add a video recording of how your app and license management works to assist the team for testing. 

 






