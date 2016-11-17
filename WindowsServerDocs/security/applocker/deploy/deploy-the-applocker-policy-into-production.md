---
title: Deploy the AppLocker Policy into Production
description: "Windows Server Security"
ms.custom: na
ms.prod: windows-server-threshold
ms.reviewer: na
ms.suite: na
ms.technology: security-applocker
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 26fd78e0-393d-4dec-b96a-66fe81c366c3
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/12/2016
---
# Deploy the AppLocker Policy into Production

>Applies To: Windows Server 2016, Windows Server 2012 R2, Windows Server 2012

This topic for the IT professional describes the tasks that should be completed before you deploy AppLocker application control settings.

After successfully testing and modifying the AppLocker policy for each Group Policy Object (GPO), you are ready to deploy the enforcement settings into production. For most organizations, this means switching the AppLocker enforcement setting from **Audit only** to **Enforce rules**. However, it is important to follow the deployment plan that you created earlier. For more information, see the [AppLocker Policies Design Guide](../design/applocker-policies-design-guide.md). Depending on the needs of different business groups in your organization, you might deploy different enforcement settings for linked GPOs.

### Understand your design decisions
Before you deploy an AppLocker policy, you should determine:

-   For each business group, which applications will be controlled and in what manner. For more information, see [Create List of Applications Deployed to Each Business Group](../design/create-list-of-applications-deployed-to-each-business-group.md).

-   How to handle requests for application access. For information about what to consider when developing your support policies, see [Plan for AppLocker Policy Management](../design/plan-for-applocker-policy-management.md).

-   How to manage events, including forwarding events. For information about event management in AppLocker, see [Monitor Application Usage with AppLocker](../manage/monitor-application-usage-with-applocker.md).

-   Your GPO structure, including how to include policies generated by Software Restriction Policies and AppLocker policies. For more information, see [Determine Group Policy Structure and Rule Enforcement](../design/determine-group-policy-structure-and-rule-enforcement.md).

For information about how AppLocker deployment is dependent on design decisions, see [Understand AppLocker Policy Design Decisions](../design/understand-applocker-policy-design-decisions.md).

### AppLocker deployment methods
If you have configured a reference computer, you can create and update your AppLocker policies on this computer, test the policies, and then export the policies to the appropriate GPO for distribution. Another method is to create the policies and set the enforcement setting on **Audit only**, then observe the events that are generated.

-   [Use a Reference Computer to Create and Maintain AppLocker Policies](use-a-reference-computer-to-create-and-maintain-applocker-policies.md)

    This topic describes the steps to use an AppLocker reference computer to prepare application control policies for deployment by using Group Policy or other means.

-   [Deploy AppLocker Policies by Using the Enforce Rules Setting](../manage/deploy-applocker-policies-by-using-the-enforce-rules-setting.md)

    This topic describes the steps to deploy the AppLocker policy by changing the enforcement setting to **Audit only** or to **Enforce rules**.

## See also
[AppLocker Policies Deployment Guide](applocker-policies-deployment-guide.md)

