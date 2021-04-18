---
description: L'oggetto SWbemEventSource recupera gli eventi da una query di eventi insieme a SWbemServices.ExecNotificationQuery.
ms.assetid: 7efd5e6a-4311-4d20-8b05-e9208eec098a
ms.tgt_platform: multiple
title: Oggetto SWbemEventSource (wbemdisp. h)
ms.topic: reference
ms.date: 09/25/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource
- ISWbemEventSource
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8da55a7b6722c263fe9a3fb0af7a8db07d672e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309850"
---
# <a name="swbemeventsource-object"></a>Oggetto SWbemEventSource

L'oggetto **SWbemEventSource** recupera gli eventi da una query di eventi insieme a [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md). Si ottiene un oggetto **SWbemEventSource** se si effettua una chiamata a **SWbemServices.ExecNotificationQuery** per creare una query di eventi. È quindi possibile usare il metodo [**NextEvent**](swbemeventsource-nextevent.md) per recuperare gli eventi man mano che arrivano. Questo oggetto non può essere creato dalla chiamata [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) di VBScript.

## <a name="members"></a>Membri

L'oggetto **SWbemEventSource** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **SWbemEventSource** dispone di questi metodi.



| Metodo                                          | Descrizione                                                                                                                                  |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**NextEvent**](swbemeventsource-nextevent.md) | Utilizzato per recuperare un evento in combinazione con [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **SWbemEventSource** dispone di queste proprietà.



| Proprietà                                                    | Tipo di accesso          | Descrizione                                              |
|:------------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Sicurezza\_**](swbemeventsource-security-.md)<br/> | Sola lettura<br/> | Utilizzato per leggere o modificare le impostazioni di sicurezza.<br/> |



 

## <a name="examples"></a>Esempio

Questo script usa i metodi della classe **SWbemEventSource** e la classe [**SWbemServices**](swbemservices.md) insieme a una query WQL per gli eventi dell'applicazione. Per ulteriori informazioni sulla notifica degli eventi WMI e sulle query, vedere [eventi di monitoraggio](monitoring-events.md), [esecuzione di uno script basato su un evento](running-a-script-based-on-an-event.md)e [ricezione di notifiche di eventi asincroni](receiving-asynchronous-event-notifications.md).


```VB
' Connect to WMI, obtaining an SWbemServices object
set svc = _
CreateObject("Wbemscripting.SWbemLocator")._
   ConnectServer(,"root\cimv2")

' Obtain an SWbemEventSource object from the 
' SWbemServices.ExecNotificationQuery method to specify the 
' event source as "Application" events in a Win32_NTLogEvent
set evtsrc = svc.ExecNotificationQuery("SELECT * " _
   & "FROM __InstanceCreationEvent " _
   & "WHERE TargetInstance ISA 'Win32_NTLogEvent'" _
   & "AND TargetInstance.Logfile ='Application'")

' Wait for an event by executing the NextEvent method on the 
' SWbemEventSource object.
while (num < 5)
    set inst = evtsrc.NextEvent(-1)
    Wscript.echo inst.TargetInstance.Logfile
    num = num + 1
wend
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMEVENTSOURCE CLSID<br/>                                                      |
| IID<br/>                      | \_ISWBEMEVENTSOURCE IID<br/>                                                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> </dl>

 

