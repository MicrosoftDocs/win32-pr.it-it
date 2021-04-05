---
title: Panoramica dell'uso del provider WMI DNS
description: I passaggi generali seguenti consentono di iniziare a creare uno script o un programma personalizzato che usa il provider WMI DNS.
ms.assetid: d9d64bda-0564-4074-9f0a-a249c7315042
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9188e14e0a0b1f73380434be0d4298b0748da12f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044998"
---
# <a name="overview-of-using-the-dns-wmi-provider"></a><span data-ttu-id="dd014-103">Panoramica dell'uso del provider WMI DNS</span><span class="sxs-lookup"><span data-stu-id="dd014-103">Overview of Using the DNS WMI Provider</span></span>

<span data-ttu-id="dd014-104">I passaggi generali seguenti consentono di iniziare a creare uno script o un programma personalizzato che usa il provider WMI DNS.</span><span class="sxs-lookup"><span data-stu-id="dd014-104">The following general steps get you started in creating your own script or program that makes use of the DNS WMI Provider.</span></span>

<span data-ttu-id="dd014-105">**Per creare uno script o un programma utilizzando il provider WMI DNS**</span><span class="sxs-lookup"><span data-stu-id="dd014-105">**To create a script or program using the DNS WMI Provider**</span></span>

1.  <span data-ttu-id="dd014-106">Connettersi al provider WMI DNS.</span><span class="sxs-lookup"><span data-stu-id="dd014-106">Connect to the DNS WMI Provider.</span></span>
    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")

    'Connect to the namespace which is either local or remote
    Set objService = objLocator.ConnectServer (strServer, strNameSpace, _
                                                                                                                                                                                strUserName, strPassword)
    ```

    

    > [!Note]  
    > <span data-ttu-id="dd014-107">Lo spazio dei nomi per il provider WMI DNS sarà sempre "root \\ MicrosoftDNS".</span><span class="sxs-lookup"><span data-stu-id="dd014-107">The name space for the DNS WMI Provider will always be "root\\microsoftdns".</span></span>

     

2.  <span data-ttu-id="dd014-108">Ottenere un'istanza del server DNS.</span><span class="sxs-lookup"><span data-stu-id="dd014-108">Get a DNS Server instance.</span></span>
    ```VB
    set objServer = objService.Get("MicrosoftDNS_Server.name="".""")
    ```

    

3.  <span data-ttu-id="dd014-109">A seconda dell'azione del tipo che si vuole eseguire, ottenere una zona DNS o un'istanza di record.</span><span class="sxs-lookup"><span data-stu-id="dd014-109">Depending on the type action you want to perform, get a DNS zone or record instance.</span></span>
    ```VB
    Set objDNSSet = objService.Get("MicrosoftDNS_ZONE")
    Set objDNSset = objService.Get("MicrosoftDNS_Zone.ContainerName=""" _
                                                                    & strZoneArray(0) & """,DnsServerName=""" & _ 
                    objServer.Name & """,Name=""" & _
                    strZoneArray(0) & """")
    ```

    

4.  <span data-ttu-id="dd014-110">Eseguire le azioni desiderate:</span><span class="sxs-lookup"><span data-stu-id="dd014-110">Perform the desired actions:</span></span>
    -   <span data-ttu-id="dd014-111">Eseguire un metodo</span><span class="sxs-lookup"><span data-stu-id="dd014-111">Execute a method</span></span>
    -   <span data-ttu-id="dd014-112">Visualizza una proprietà</span><span class="sxs-lookup"><span data-stu-id="dd014-112">Display a property</span></span>
    -   <span data-ttu-id="dd014-113">Modificare una proprietà (deve avere accesso in lettura/scrittura)</span><span class="sxs-lookup"><span data-stu-id="dd014-113">Modify a property (must have Read/Write access)</span></span>

 

 




