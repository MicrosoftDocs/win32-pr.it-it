---
description: WMI esegue automaticamente il mapping delle trap SNMP agli eventi WMI. Il sistema inserisce i dati contenuti nella trap nelle proprietà corrispondenti di un'istanza di evento WMI per l'accesso da parte del computer host WMI.
ms.assetid: 549f58a9-9d3b-41b9-a374-ab83877f63a7
ms.tgt_platform: multiple
title: Ricezione di trap SNMP come eventi WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a53de147b7c2fd4f96c4029d759378d2ee64a65fb5a48e1b7b1348383803b8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817467"
---
# <a name="receiving-snmp-traps-as-wmi-events"></a>Ricezione di trap SNMP come eventi WMI

WMI esegue automaticamente il mapping delle trap SNMP agli eventi WMI. Il sistema inserisce i dati contenuti nella trap nelle proprietà corrispondenti di un'istanza di evento WMI per l'accesso da parte del computer host WMI.

> [!Note]  
> Per altre informazioni sull'installazione del provider, vedere [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).

 

La ricezione di un trap SNMP è quasi identica alla ricezione di eventi da qualsiasi altro provider WMI. Tuttavia, il filtro eventi SNMP ha diverse classi univoche di cui tenere conto prima di eseguire la registrazione per gli eventi. Inoltre, il provider di eventi richiede l'uso esclusivo dello \\ spazio dei nomi smir.

Le classi più comuni con cui eseguire la registrazione [sono SnmpNotification](snmpnotification.md) e [SnmpExtendedNotification.](snmpextendednotification.md) Gli utenti che hanno intenzione di usare le notifiche degli eventi per aggiornare i valori nei dispositivi SNMP monitorati devono registrarsi per gli eventi SnmpExtendedNotification. Le informazioni degli eventi SnmpNotification non sono riutilizzabili.

Nella tabella seguente sono elencate le informazioni sulla configurazione del computer per la ricezione di trap SNMP come eventi WMI.



| Attività                                                                               | Descrizione                                                                        |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Scelta tra provider di eventi SNMP](choosing-between-snmp-event-providers.md) | WMI include due provider di eventi SNMP.                                             |
| [Ricezione di eventi SNMP](receiving-snmp-events.md)                                 | I provider di eventi SNMP supportano tre tipi di trap SNMPv1 e notifiche SNMPv2. |



 

L'esempio seguente configura un computer per monitorare l'evento **SnmpLinkUpNotification** da un hub gestito.


```VB
Set objLocator = CreateObject("wbemscripting.swbemlocator")
Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")

set objwbemEventsource = _ 
    objServices.ExecNotificationQuery _
   ("SELECT * FROM SnmpLinkUpNotification")

set objWbemObject = objwbemEventsource.NextEvent()

wscript.echo "Received " & objWbemObject.path_.class

for each prop in objWbemObject.properties_
    wscript.echo prop.name & " -- " & prop.value
next
```



 

 



