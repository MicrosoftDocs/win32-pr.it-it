---
title: Panoramica dell'uso del provider WMI DNS
description: I passaggi generali seguenti illustrano come creare uno script o un programma personalizzato che usa il provider WMI DNS.
ms.assetid: d9d64bda-0564-4074-9f0a-a249c7315042
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9eaa50e4ed1a237ed5b42abd4375ab301a2106498e929e42993cd634ca9ba18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077031"
---
# <a name="overview-of-using-the-dns-wmi-provider"></a>Panoramica dell'uso del provider WMI DNS

I passaggi generali seguenti illustrano come creare uno script o un programma personalizzato che usa il provider WMI DNS.

**Per creare uno script o un programma utilizzando il provider WMI DNS**

1.  Connessione al provider WMI DNS.
    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")

    'Connect to the namespace which is either local or remote
    Set objService = objLocator.ConnectServer (strServer, strNameSpace, _
                                                                                                                                                                                strUserName, strPassword)
    ```

    

    > [!Note]  
    > Lo spazio dei nomi per il provider WMI DNS sarà sempre "root \\ microsoftdns".

     

2.  Ottenere un'istanza del server DNS.
    ```VB
    set objServer = objService.Get("MicrosoftDNS_Server.name="".""")
    ```

    

3.  A seconda dell'azione di tipo che si vuole eseguire, ottenere una zona DNS o un'istanza di record.
    ```VB
    Set objDNSSet = objService.Get("MicrosoftDNS_ZONE")
    Set objDNSset = objService.Get("MicrosoftDNS_Zone.ContainerName=""" _
                                                                    & strZoneArray(0) & """,DnsServerName=""" & _ 
                    objServer.Name & """,Name=""" & _
                    strZoneArray(0) & """")
    ```

    

4.  Eseguire le azioni desiderate:
    -   Eseguire un metodo
    -   Visualizzare una proprietà
    -   Modificare una proprietà (deve avere accesso in lettura/scrittura)

 

 




