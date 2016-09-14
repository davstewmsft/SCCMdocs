---
title: "Introduction to hardware inventory in System Center Configuration Manager"
ms.custom: na
ms.date: 2015-12-08
ms.prod: configuration-manager
ms.reviewer: na
ms.suite: na
ms.technology:
  - configmgr-other
ms.tgt_pltfrm: na
ms.topic: get-started-article
ms.assetid: 3969952e-9d05-49c9-82a2-e7e90ccef511
caps.latest.revision: 6
caps.handback.revision: 0
author: barlanmsft
translation.priority.ht:
  - cs-cz
  - de-de
  - en-gb
  - es-es
  - fr-fr
  - hu-hu
  - it-it
  - ja-jp
  - ko-kr
  - nl-nl
  - pl-pl
  - pt-br
  - pt-pt
  - ru-ru
  - sv-se
  - tr-tr
  - zh-cn
  - zh-tw
---
# Introduction to hardware inventory in System Center Configuration Manager
Use hardware inventory in System Center Configuration Manager to collect information about the hardware configuration of client devices in your organization. To collect hardware inventory, the **Enable hardware inventory on clients** setting must be enabled in client settings.  

 After hardware inventory is enabled and a hardware inventory cycle is run by the client, the client sends the inventory information that it has collected to a management point in the client’s site. The management point then forwards the inventory information to the Configuration Manager site server which stores the inventory information in the site database. Hardware inventory runs on clients according to the schedule that you specify in client settings.  

 You can use several methods to view the hardware inventory data that Configuration Manager collects. These include the following:  

-   Create queries that return devices that are based on a specific hardware configuration. For more information, see [Queries technical reference for System Center Configuration Manager](../../../../core/servers/manage/queries-technical-reference.md).  

-   Create query-based collections that are based on a specific hardware configuration. Query-based collection memberships automatically update on a schedule. You can use collections for several tasks, which include software deployment. For more information, see [Collections technical reference for System Center Configuration Manager](../../../../core/clients/manage/collections/collections-technical-reference.md).  

-   Run reports that display specific details about hardware configurations in your organization. For more information, see [Reporting in System Center Configuration Manager](../../../../core/servers/manage/reporting.md).  

-   Use Resource Explorer to view detailed information about the hardware inventory that is collected from client devices. For more information, see [How to use Resource Explorer to view hardware inventory in System Center Configuration Manager](../../../../core/clients/manage/inventory/use-resource-explorer-to-view-hardware-inventory.md).  

 When hardware inventory runs on a client device, the first inventory data that the client returns is always a full inventory. Subsequent inventory information contains only delta inventory information. The site server processes delta inventory information in the order in which it is received. If delta inventory information for a client is missing, the site server rejects additional delta inventory information and instructs the client to run a full inventory cycle.  

 Configuration Manager provides limited support for dual-boot computers. Configuration Manager can discover dual-boot computers but only returns inventory information from the operating system that was active at the time the inventory cycle ran.  

> [!NOTE]  
>  For information about how to use hardware inventory with clients that run Linux and UNIX, see [Hardware inventory for Linux and UNIX in System Center Configuration Manager](../../../../core/clients/manage/inventory/hardware-inventory-for-linux-and-unix.md).  

## Extending Configuration Manager hardware inventory  
 In addition to the built-in hardware inventory in Configuration Manager, you can also use one of the following methods to extend hardware inventory to collect additional information:  

|Method|Description|  
|------------|-----------------|  
|Add and remove inventory classes from the Configuration Manager console|In Configuration Manager, you can enable, disable, add and remove inventory classes for hardware inventory from the Configuration Manager console.|  
|NOIDMIF files|Use NOIDMIF files to collect information about client devices that cannot be inventoried by Configuration Manager. For example, you might want to collect device asset number information that exists only as a label on the device. NOIDMIF inventory is automatically associated with the client device that it was collected from.|  
|IDMIF files|Use IDMIF files to collect information about assets in your organization that are not associated with a Configuration Manager client, for example, projectors, photocopiers and network printers.|  

 For more information about using these methods to extend Configuration Manager hardware inventory, see [How to configure hardware inventory in System Center Configuration Manager](../../../../core/clients/manage/inventory/configure-hardware-inventory.md).  