---
description: L'oggetto SWbemEventSource recupera gli eventi da una query di eventi in combinazione con SWbemServices.ExecNotificationQuery.
ms.assetid: 7efd5e6a-4311-4d20-8b05-e9208eec098a
ms.tgt_platform: multiple
title: Oggetto SWbemEventSource (Wbemdisp.h)
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
ms.openlocfilehash: e38dab258ebccacb24cf92b7445752102b297ab1207b99e40355c30fde99113d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992141"
---
# <a name="swbemeventsource-object"></a>Oggetto SWbemEventSource

**L'oggetto SWbemEventSource** recupera gli eventi da una query di eventi in combinazione con [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md). Si ottiene un **oggetto SWbemEventSource** se si effettua una chiamata a **SWbemServices.ExecNotificationQuery** per eseguire una query di evento. È quindi possibile usare il [**metodo NextEvent**](swbemeventsource-nextevent.md) per recuperare gli eventi non appena arrivano. Questo oggetto non può essere creato dalla chiamata [createObject](/previous-versions//xzysf6hc(v=vs.85)) vbscript.

## <a name="members"></a>Membri

**L'oggetto SWbemEventSource** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto SWbemEventSource** dispone di questi metodi.



| Metodo                                          | Descrizione                                                                                                                                  |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**NextEvent**](swbemeventsource-nextevent.md) | Usato per recuperare un evento in combinazione con [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto SWbemEventSource** ha queste proprietà.



| Proprietà                                                    | Tipo di accesso          | Descrizione                                              |
|:------------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Sicurezza\_**](swbemeventsource-security-.md)<br/> | Sola lettura<br/> | Consente di leggere o modificare le impostazioni di sicurezza.<br/> |



 

## <a name="examples"></a>Esempio

Questo script usa i metodi della **classe SWbemEventSource** e [**della classe SWbemServices**](swbemservices.md) insieme a una query WQL per gli eventi dell'applicazione. Per altre informazioni sulla notifica degli eventi WMI e sulle query, vedere Monitoring [Events](monitoring-events.md), [Running a Script Based on an Event](running-a-script-based-on-an-event.md)e Receiving Asynchronous Event [Notifications](receiving-asynchronous-event-notifications.md).


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
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemEventSource<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemEventSource<br/>                                                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Scripting di oggetti API](scripting-api-objects.md)
</dt> </dl>

 

