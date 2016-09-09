---
title: "Manage BranchCache in Windows Server Essentials"
ms.custom: na
ms.date: 08/29/2016
ms.prod: windows-server-2012-r2-essentials
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
applies_to: 
  - Windows Server 2012 Essentials
  - Windows Server 2012 R2 Essentials
ms.assetid: f6e05aec-d07c-4e0b-94ab-f20279e9ffd1
caps.latest.revision: 18
author: DonGill
manager: stevenka
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pt-br
  - ru-ru
  - zh-cn
  - zh-tw
---
# Manage BranchCache in Windows Server Essentials
BranchCache can help you optimize Internet usage, improve performance of networked applications, and reduce traffic on your wide-area network (WAN) when the --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows Server Essentials server is located remotely from your office, or when client computers connected to a local server use cloud-based resources such as SharePoint Online libraries.  
  
 With BranchCache enabled, when a client computer requests content from a remote --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows Server Essentials server, the content is cached in the local office. After that, other computers in the same office can obtain the content locally instead of downloading the content from the server again over the WAN. This can improve the performance of networked applications and reduces bandwidth consumption over the WAN.  
  
 Whether your --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows Server Essentials server is local or remote, BranchCache can improve response times for server shared folders and Web content that is hosted on the server (such as SharePoint Online libraries).  
  
 Because BranchCache does not require new hardware or network topology changes, this feature gives you a simple way to optimize bandwidth usage and improve response times for services and resources accessed over the WAN.  
  
## BranchCache scenarios  
 There are three basic scenarios for using BranchCache with a remote server:  
  
-   Your --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows Server Essentials server is hosted in --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Microsoft Azure.  
  
-   Your --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows Server Essentials server is hosted in the datacenter of a third-party service provider.  
  
-   Your --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows Server Essentials server is in another office in a different physical location.  
  
## Distributed cache mode  
 In --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows Server Essentials, BranchCache is implemented in *distributed cache mode*, one of two cache modes available in BranchCache. In distributed cache mode, the content cache in the branch office is distributed among client computers. Because no additional hardware or topology changes are required, this mode works well for small offices that use a remote server or use a local server to access cloud-based services such as SharePoint Online. When you turn on BranchCache in --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows Server 2012 R2 Essentials, distributed cache mode is implemented.  
  
> [!NOTE]
>  In larger branch offices with more than one subnet or with a large number of employees using networked applications, it can be beneficial to implement BranchCache in *hosted cache mode*. In hosted cache mode, the content cache is stored on one or more hosted cache servers in the branch office. For more information, see [Choosing a BranchCache Design](assetId:///eb9dc5d3-bfdd-4b90-88b5-a7ee0bc98e17). For information about setting up BranchCache in hosted cache mode, see the [BranchCache Deployment Guide](assetId:///9a8217ed-f85d-4b6b-a339-926e258b713d).  
  
## Requirements  
 To use BranchCache in --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows Server Essentials, your server and client computers must meet the following requirements:  
  
-   The server must be running the --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows Server 2012 R2 Essentials operating system or the --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows Server 2012 R2 Standard or --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows Server 2012 R2 Datacenter operating system with the Windows Server Essentials Experience role.  
  
     On a --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows Server 2012 R2 Standard or --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows Server 2012 R2 Datacenter server, BranchCache is added when you add the Windows Server Essentials Experience role. To turn on BranchCache, you will need to sign in to the --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows Server Essentials Dashboard with domain administrator credentials.  
  
-   Client computers must be running the --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows 7 Enterprise, --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows 7 Ultimate, --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows 8 Enterprise, or --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows 8.1 Enterprise operating system.  
  
-   In distributed cache mode, all client computers must be on same subnet.  
  
    > [!NOTE]
    >  If you connected client computers to your Windows Server Essentials server without joining them to the domain, those computers are excluded from caching by default. To include a client computer that is not domain-joined in caching, run the [Enable-BCDistributed](http://technet.microsoft.com/library/hh848398.aspx) Windows PowerShell cmdlet on the client computer. For more information, see [BranchCache Cmdlets in Windows PowerShell](http://technet.microsoft.com/library/hh848392.aspx).  
  
> [!NOTE]
>  These requirements are for BranchCache in distributed cache mode. If you plan to use hosted cache mode, see the [BranchCache Deployment Guide](assetId:///9a8217ed-f85d-4b6b-a339-926e258b713d) for server and topology requirements.  
  
## Turn BranchCache on  
 To turn BranchCache on in distributed cache mode, you simply click a button on the --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows Server 2012 R2 Essentials Dashboard. Caching begins immediately and is performed transparently.  
  
#### To turn on BranchCache in Windows Server Essentials  
  
1.  Sign in on the --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows Server Essentials server with your Administrator account.  
  
2.  On the --- translation.priority.ht:    - cs-cz   - de-at   - de-de   - es-es   - fr-be   - fr-fr   - hu-hu   - it-ch   - it-it   - ja-jp   - ko-kr   - nl-be   - nl-nl   - pl-pl   - pt-br   - pt-pt   - ru-ru   - sv-se   - tr-tr   - zh-cn   - zh-tw --- Windows Server Essentials Dashboard, click **Settings**.  
  
     The Settings Wizard opens.  
  
3.  Click **BranchCache**.  
  
4.  On the **BranchCache settings** page, click **Turn on**.  
  
## Use Windows PowerShell to turn BranchCache on or off  
 You can use Windows PowerShell to check the status of BranchCache (Enabled or Disabled) and to turn BranchCache on or off.  
  
#### To turn BranchCache on or off using Windows PowerShell  
  
1.  On the server, open Windows PowerShell as an administrator. On the **Start** page, right-click **Windows PowerShell**, click **Run as Administrator**, and then click **Yes**.  
  
2.  Enter any of the following cmdlets at the command prompt.  
  
    -   To check the status of BranchCache (Enabled or Disabled), enter:  
  
        ```powershell  
        Get-WSSBranchCacheStatus  
        ```  
  
    -   To turn BranchCache on, enter:  
  
        ```powershell  
        Enable-WSSBranchCache  
        ```  
  
    -   To turn BranchCache off, enter:  
  
        ```powershell  
        Disable-WSSBranchCache  
        ```  
  
## See also  
  
-   [Choosing a BranchCache Design](assetId:///eb9dc5d3-bfdd-4b90-88b5-a7ee0bc98e17)  
  
-   [BranchCache Overview](http://technet.microsoft.com/library/hh831696.aspx)  
  
-   [Manage Windows Server Essentials](../windows-server-essentials-manage/Manage-Windows-Server-Essentials.md)