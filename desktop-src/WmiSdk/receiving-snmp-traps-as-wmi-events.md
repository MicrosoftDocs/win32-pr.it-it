---
description: WMI esegue automaticamente il mapping di trap SNMP a eventi WMI. Il sistema inserisce i dati contenuti nella trap nelle proprietà corrispondenti di un'istanza di evento WMI per l'accesso da parte del computer host WMI.
ms.assetid: 549f58a9-9d3b-41b9-a374-ab83877f63a7
ms.tgt_platform: multiple
title: Ricezione di trap SNMP come eventi WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da24be8ea9a4882af0b961b1d0f6f0c3d442c70c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528507"
---
# <a name="receiving-snmp-traps-as-wmi-events"></a>Ricezione di trap SNMP come eventi WMI

WMI esegue automaticamente il mapping di trap SNMP a eventi WMI. Il sistema inserisce i dati contenuti nella trap nelle proprietà corrispondenti di un'istanza di evento WMI per l'accesso da parte del computer host WMI.

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

La ricezione di un trap SNMP è quasi identica alla ricezione di eventi da qualsiasi altro provider WMI. Tuttavia, il filtro eventi SNMP dispone di diverse classi univoche da tenere presenti prima di eseguire la registrazione per gli eventi. Il provider di eventi richiede inoltre l'utilizzo esclusivo dello \\ spazio dei nomi archivio SMIR.

Le classi più comuni con cui eseguire la registrazione sono [SnmpNotification](snmpnotification.md) e [SnmpExtendedNotification](snmpextendednotification.md). Gli utenti intenzionati a utilizzare le notifiche degli eventi per aggiornare i valori nei dispositivi SNMP monitorati devono registrarsi per gli eventi SnmpExtendedNotification. Le informazioni degli eventi SnmpNotification non sono riutilizzabili.

Nella tabella seguente sono elencate le informazioni sulla configurazione del computer per la ricezione di trap SNMP come eventi WMI.



| Attività                                                                               | Descrizione                                                                        |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Scelta tra i provider di eventi SNMP](choosing-between-snmp-event-providers.md) | WMI include due provider di eventi SNMP.                                             |
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



 

 



