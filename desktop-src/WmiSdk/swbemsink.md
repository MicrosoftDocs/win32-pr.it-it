---
description: L'oggetto SWbemSink viene implementato dalle applicazioni client per ricevere i risultati delle operazioni asincrone e delle notifiche degli eventi.
ms.assetid: a90777ef-fa26-4bfb-b196-c083a0c92a29
ms.tgt_platform: multiple
title: Oggetto SWbemSink (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink
- ISWbemSinkEvents
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b8007b7387a09e31f49dbc833f657bc959ee11e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309762"
---
# <a name="swbemsink-object"></a>Oggetto SWbemSink

L'oggetto **SWbemSink** viene implementato dalle applicazioni client per ricevere i risultati delle operazioni asincrone e delle notifiche degli eventi. Per eseguire una chiamata asincrona, è necessario creare un'istanza di un oggetto **SWbemSink** e passarla come parametro *ObjWbemSink* . Gli eventi nell'implementazione di **SWbemSink** vengono attivati quando vengono restituiti lo stato o i risultati o quando la chiamata è completa. La chiamata **CreateObject** di VBScript crea questo oggetto.

## <a name="members"></a>Membri

L'oggetto **SWbemSink** dispone di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'oggetto **SWbemSink** dispone di questi metodi.



| Metodo                             | Descrizione                                                                        |
|:-----------------------------------|:-----------------------------------------------------------------------------------|
| [**Annulla**](swbemsink-cancel.md) | Annulla tutte le operazioni asincrone associate a questo sink.<br/> |



 

## <a name="remarks"></a>Commenti

Un callback asincrono consente a un utente non autenticato di fornire dati al sink. Questo comporta rischi per la sicurezza per gli script e le applicazioni. Per eliminare i rischi, usare la comunicazione semisincrono o la comunicazione sincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

### <a name="events"></a>Eventi

È possibile implementare subroutine da chiamare quando vengono attivati gli eventi. Se, ad esempio, si desidera elaborare ogni oggetto restituito da una chiamata di query asincrona, ad esempio [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), creare una subroutine utilizzando il sink specificato nella chiamata asincrona, come illustrato nell'esempio seguente.


```VB
Sub SinkName_OnObjectReady(objObject, objAsyncContext)
```



Usare la tabella seguente come riferimento per identificare gli eventi e le descrizioni dei trigger.



| Event                                            | Descrizione                                                             |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [**OnCompleted**](swbemsink-oncompleted.md)     | Attivato al completamento di un'operazione asincrona.                   |
| [**OnObjectPut**](swbemsink-onobjectput.md)     | Attivato quando un'operazione Put asincrona è completata.               |
| [**OnObjectReady**](swbemsink-onobjectready.md) | Attivato quando è disponibile un oggetto fornito da una chiamata asincrona. |
| [**OnProgress**](swbemsink-onprogress.md)       | Attivato per fornire lo stato di un'operazione asincrona.            |



 

**Recupero asincrono delle statistiche del registro eventi**

WMI supporta sia gli script asincroni sia quelli parzialmente sincroni. Quando si recuperano gli eventi dai registri eventi, gli script asincroni spesso recuperano questi dati molto più velocemente.

In uno script asincrono viene eseguita una query e il controllo viene restituito immediatamente allo script. La query continua a essere elaborata in un thread separato mentre lo script inizia a agire immediatamente sulle informazioni restituite. Gli script asincroni sono basati su eventi: ogni volta che viene recuperato un record evento, viene generato l'evento OnObjectReady. Al termine della query, l'evento OnCompleted viene attivato e lo script può continuare in base al fatto che sono stati restituiti tutti i record disponibili.

In uno script semi-sincrono, al contrario, viene eseguita una query e lo script Accoda una grande quantità di informazioni recuperate prima di agire su di essa. Per molti oggetti, l'elaborazione semi-sincrona è adeguata; ad esempio, quando si esegue una query su un'unità disco per le relative proprietà, potrebbe essere presente solo un secondo diviso tra il momento in cui viene eseguita la query e l'ora in cui vengono restituite le informazioni e su cui si agisce. Ciò è dovuto in gran parte al fatto che la quantità di informazioni restituite è relativamente piccola.

Quando si esegue una query su un registro eventi, tuttavia, l'intervallo tra il momento in cui viene eseguita la query e il momento in cui uno script semisincrono può terminare la restituzione e agire sulle informazioni può richiedere ore. A questo proposito, lo script potrebbe esaurire la memoria e non riuscirà da solo prima del completamento.

Per i registri eventi con un numero elevato di record, la differenza nel tempo di elaborazione può essere considerevole. In un computer di test basato su Windows 2000 con record 2.000 nel registro eventi, una query semi-sincrona che recupera tutti gli eventi e li visualizza in una finestra di comando richiede 10 minuti 45 secondi. Una query asincrona che ha eseguito la stessa operazione ha richiesto un minuto di 54 secondi.

## <a name="examples"></a>Esempio

Il codice VBScript seguente esegue una query asincrona dei registri eventi per tutti i record.


```VB
Const POPUP_DURATION = 10
Const OK_BUTTON = 0
Set objWSHShell = Wscript.CreateObject("Wscript.Shell")
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objSink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
objWMIService.InstancesOfAsync objSink, "Win32_NTLogEvent"
errReturn = objWshShell.Popup("Retrieving events", POPUP_DURATION, _
"Event Retrieval", OK_BUTTON)
Sub SINK_OnCompleted(iHResult, objErrorObject, objAsyncContext)
 WScript.Echo "Asynchronous operation is done."
End Sub
Sub SINK_OnObjectReady(objEvent, objAsyncContext)
 Wscript.Echo "Category: " & objEvent.Category
 Wscript.Echo "Computer Name: " & objEvent.ComputerName
 Wscript.Echo "Event Code: " & objEvent.EventCode
 Wscript.Echo "Message: " & objEvent.Message
 Wscript.Echo "Record Number: " & objEvent.RecordNumber
 Wscript.Echo "Source Name: " & objEvent.SourceName
 Wscript.Echo "Time Written: " & objEvent.TimeWritten
 Wscript.Echo "Event Type: " & objEvent.Type
 Wscript.Echo "User: " & objEvent.User
End Sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSINK CLSID<br/> \_SWBEMSINKEVENTS CLSID<br/>                           |
| IID<br/>                      | \_ISWBEMSINK IID<br/> \_ISWBEMSINKEVENTS IID<br/>                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> </dl>

 

 




