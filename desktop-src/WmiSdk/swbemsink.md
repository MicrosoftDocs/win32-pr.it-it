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
# <a name="swbemsink-object"></a><span data-ttu-id="7a0e4-103">Oggetto SWbemSink</span><span class="sxs-lookup"><span data-stu-id="7a0e4-103">SWbemSink object</span></span>

<span data-ttu-id="7a0e4-104">L'oggetto **SWbemSink** viene implementato dalle applicazioni client per ricevere i risultati delle operazioni asincrone e delle notifiche degli eventi.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-104">The **SWbemSink** object is implemented by client applications to receive the results of asynchronous operations and event notifications.</span></span> <span data-ttu-id="7a0e4-105">Per eseguire una chiamata asincrona, è necessario creare un'istanza di un oggetto **SWbemSink** e passarla come parametro *ObjWbemSink* .</span><span class="sxs-lookup"><span data-stu-id="7a0e4-105">To make an asynchronous call, you must create an instance of an **SWbemSink** object and pass it as the *ObjWbemSink* parameter.</span></span> <span data-ttu-id="7a0e4-106">Gli eventi nell'implementazione di **SWbemSink** vengono attivati quando vengono restituiti lo stato o i risultati o quando la chiamata è completa.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-106">The events in your implementation of **SWbemSink** are triggered when status or results are returned, or when the call is complete.</span></span> <span data-ttu-id="7a0e4-107">La chiamata **CreateObject** di VBScript crea questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-107">The VBScript **CreateObject** call creates this object.</span></span>

## <a name="members"></a><span data-ttu-id="7a0e4-108">Membri</span><span class="sxs-lookup"><span data-stu-id="7a0e4-108">Members</span></span>

<span data-ttu-id="7a0e4-109">L'oggetto **SWbemSink** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7a0e4-109">The **SWbemSink** object has these types of members:</span></span>

-   [<span data-ttu-id="7a0e4-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="7a0e4-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7a0e4-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="7a0e4-111">Methods</span></span>

<span data-ttu-id="7a0e4-112">L'oggetto **SWbemSink** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-112">The **SWbemSink** object has these methods.</span></span>



| <span data-ttu-id="7a0e4-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="7a0e4-113">Method</span></span>                             | <span data-ttu-id="7a0e4-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a0e4-114">Description</span></span>                                                                        |
|:-----------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="7a0e4-115">**Annulla**</span><span class="sxs-lookup"><span data-stu-id="7a0e4-115">**Cancel**</span></span>](swbemsink-cancel.md) | <span data-ttu-id="7a0e4-116">Annulla tutte le operazioni asincrone associate a questo sink.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-116">Cancels all asynchronous operations that are associated with this sink.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7a0e4-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a0e4-117">Remarks</span></span>

<span data-ttu-id="7a0e4-118">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-118">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="7a0e4-119">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-119">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="7a0e4-120">Per eliminare i rischi, usare la comunicazione semisincrono o la comunicazione sincrona.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-120">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="7a0e4-121">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="7a0e4-121">For more information, see [Calling a Method](calling-a-method.md).</span></span>

### <a name="events"></a><span data-ttu-id="7a0e4-122">Eventi</span><span class="sxs-lookup"><span data-stu-id="7a0e4-122">Events</span></span>

<span data-ttu-id="7a0e4-123">È possibile implementare subroutine da chiamare quando vengono attivati gli eventi.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-123">You can implement subroutines to be called when events are triggered.</span></span> <span data-ttu-id="7a0e4-124">Se, ad esempio, si desidera elaborare ogni oggetto restituito da una chiamata di query asincrona, ad esempio [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), creare una subroutine utilizzando il sink specificato nella chiamata asincrona, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-124">For example, if you want to process each object that is returned by an asynchronous query call such as [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), create a subroutine using the sink that is specified in the asynchronous call, as shown in the following example.</span></span>


```VB
Sub SinkName_OnObjectReady(objObject, objAsyncContext)
```



<span data-ttu-id="7a0e4-125">Usare la tabella seguente come riferimento per identificare gli eventi e le descrizioni dei trigger.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-125">Use the following table as a reference to identify events and trigger descriptions.</span></span>



| <span data-ttu-id="7a0e4-126">Event</span><span class="sxs-lookup"><span data-stu-id="7a0e4-126">Event</span></span>                                            | <span data-ttu-id="7a0e4-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a0e4-127">Description</span></span>                                                             |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="7a0e4-128">**OnCompleted**</span><span class="sxs-lookup"><span data-stu-id="7a0e4-128">**OnCompleted**</span></span>](swbemsink-oncompleted.md)     | <span data-ttu-id="7a0e4-129">Attivato al completamento di un'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-129">Triggered when an asynchronous operation is complete.</span></span>                   |
| [<span data-ttu-id="7a0e4-130">**OnObjectPut**</span><span class="sxs-lookup"><span data-stu-id="7a0e4-130">**OnObjectPut**</span></span>](swbemsink-onobjectput.md)     | <span data-ttu-id="7a0e4-131">Attivato quando un'operazione Put asincrona è completata.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-131">Triggered when an asynchronous Put operation is complete.</span></span>               |
| [<span data-ttu-id="7a0e4-132">**OnObjectReady**</span><span class="sxs-lookup"><span data-stu-id="7a0e4-132">**OnObjectReady**</span></span>](swbemsink-onobjectready.md) | <span data-ttu-id="7a0e4-133">Attivato quando è disponibile un oggetto fornito da una chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-133">Triggered when an object provided by an asynchronous call is available.</span></span> |
| [<span data-ttu-id="7a0e4-134">**OnProgress**</span><span class="sxs-lookup"><span data-stu-id="7a0e4-134">**OnProgress**</span></span>](swbemsink-onprogress.md)       | <span data-ttu-id="7a0e4-135">Attivato per fornire lo stato di un'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-135">Triggered to provide the status of a asynchronous operation.</span></span>            |



 

<span data-ttu-id="7a0e4-136">**Recupero asincrono delle statistiche del registro eventi**</span><span class="sxs-lookup"><span data-stu-id="7a0e4-136">**Asynchronously Retrieving Event Log Statistics**</span></span>

<span data-ttu-id="7a0e4-137">WMI supporta sia gli script asincroni sia quelli parzialmente sincroni.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-137">WMI supports both asynchronous and semi-synchronous scripts.</span></span> <span data-ttu-id="7a0e4-138">Quando si recuperano gli eventi dai registri eventi, gli script asincroni spesso recuperano questi dati molto più velocemente.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-138">When retrieving events from the event logs, asynchronous scripts often retrieve this data much faster.</span></span>

<span data-ttu-id="7a0e4-139">In uno script asincrono viene eseguita una query e il controllo viene restituito immediatamente allo script.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-139">In an asynchronous script, a query is issued and control is immediately returned to the script.</span></span> <span data-ttu-id="7a0e4-140">La query continua a essere elaborata in un thread separato mentre lo script inizia a agire immediatamente sulle informazioni restituite.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-140">The query continues to process on a separate thread while the script begins to immediately act on the information that is returned.</span></span> <span data-ttu-id="7a0e4-141">Gli script asincroni sono basati su eventi: ogni volta che viene recuperato un record evento, viene generato l'evento OnObjectReady.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-141">Asynchronous scripts are event driven: each time an event record is retrieved, the OnObjectReady event is fired.</span></span> <span data-ttu-id="7a0e4-142">Al termine della query, l'evento OnCompleted viene attivato e lo script può continuare in base al fatto che sono stati restituiti tutti i record disponibili.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-142">When the query has completed, the OnCompleted event will fire, and the script can continue based on the fact that all the available records have been returned.</span></span>

<span data-ttu-id="7a0e4-143">In uno script semi-sincrono, al contrario, viene eseguita una query e lo script Accoda una grande quantità di informazioni recuperate prima di agire su di essa.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-143">In a semi-synchronous script, by contrast, a query is issued and the script then queues a large amount of retrieved information before acting upon it.</span></span> <span data-ttu-id="7a0e4-144">Per molti oggetti, l'elaborazione semi-sincrona è adeguata; ad esempio, quando si esegue una query su un'unità disco per le relative proprietà, potrebbe essere presente solo un secondo diviso tra il momento in cui viene eseguita la query e l'ora in cui vengono restituite le informazioni e su cui si agisce.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-144">For many objects, semi-synchronous processing is adequate; for example, when querying a disk drive for its properties, there might be only a split second between the time the query is issued and the time the information is returned and acted upon.</span></span> <span data-ttu-id="7a0e4-145">Ciò è dovuto in gran parte al fatto che la quantità di informazioni restituite è relativamente piccola.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-145">This is due in large part to the fact that the amount of information returned is relatively small.</span></span>

<span data-ttu-id="7a0e4-146">Quando si esegue una query su un registro eventi, tuttavia, l'intervallo tra il momento in cui viene eseguita la query e il momento in cui uno script semisincrono può terminare la restituzione e agire sulle informazioni può richiedere ore.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-146">When querying an event log, however, the interval between the time the query is issued and the time that a semi-synchronous script can finish returning and acting on the information can take hours.</span></span> <span data-ttu-id="7a0e4-147">A questo proposito, lo script potrebbe esaurire la memoria e non riuscirà da solo prima del completamento.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-147">On top of that, the script might run out of memory and fail on its own before completing.</span></span>

<span data-ttu-id="7a0e4-148">Per i registri eventi con un numero elevato di record, la differenza nel tempo di elaborazione può essere considerevole.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-148">For event logs with a large number of records, the difference in processing time can be considerable.</span></span> <span data-ttu-id="7a0e4-149">In un computer di test basato su Windows 2000 con record 2.000 nel registro eventi, una query semi-sincrona che recupera tutti gli eventi e li visualizza in una finestra di comando richiede 10 minuti 45 secondi.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-149">On a Windows 2000-based test computer with 2,000 records in the event log, a semi-synchronous query that retrieved all the events and displayed them in a command window took 10 minutes 45 seconds.</span></span> <span data-ttu-id="7a0e4-150">Una query asincrona che ha eseguito la stessa operazione ha richiesto un minuto di 54 secondi.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-150">An asynchronous query that performed the same operation took one minute 54 seconds.</span></span>

## <a name="examples"></a><span data-ttu-id="7a0e4-151">Esempio</span><span class="sxs-lookup"><span data-stu-id="7a0e4-151">Examples</span></span>

<span data-ttu-id="7a0e4-152">Il codice VBScript seguente esegue una query asincrona dei registri eventi per tutti i record.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-152">The following VBScript asynchronously queries the event logs for all records.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="7a0e4-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a0e4-153">Requirements</span></span>



| <span data-ttu-id="7a0e4-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a0e4-154">Requirement</span></span> | <span data-ttu-id="7a0e4-155">Valore</span><span class="sxs-lookup"><span data-stu-id="7a0e4-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a0e4-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a0e4-156">Minimum supported client</span></span><br/> | <span data-ttu-id="7a0e4-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a0e4-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7a0e4-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a0e4-158">Minimum supported server</span></span><br/> | <span data-ttu-id="7a0e4-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a0e4-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7a0e4-160">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a0e4-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a0e4-161"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a0e4-161"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7a0e4-162">IDL</span><span class="sxs-lookup"><span data-stu-id="7a0e4-162">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7a0e4-163"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7a0e4-163"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="7a0e4-164">DLL</span><span class="sxs-lookup"><span data-stu-id="7a0e4-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a0e4-165"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a0e4-165"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7a0e4-166">CLSID</span><span class="sxs-lookup"><span data-stu-id="7a0e4-166">CLSID</span></span><br/>                    | <span data-ttu-id="7a0e4-167">\_SWBEMSINK CLSID</span><span class="sxs-lookup"><span data-stu-id="7a0e4-167">CLSID\_SWbemSink</span></span><br/> <span data-ttu-id="7a0e4-168">\_SWBEMSINKEVENTS CLSID</span><span class="sxs-lookup"><span data-stu-id="7a0e4-168">CLSID\_SWbemSinkEvents</span></span><br/>                           |
| <span data-ttu-id="7a0e4-169">IID</span><span class="sxs-lookup"><span data-stu-id="7a0e4-169">IID</span></span><br/>                      | <span data-ttu-id="7a0e4-170">\_ISWBEMSINK IID</span><span class="sxs-lookup"><span data-stu-id="7a0e4-170">IID\_ISWbemSink</span></span><br/> <span data-ttu-id="7a0e4-171">\_ISWBEMSINKEVENTS IID</span><span class="sxs-lookup"><span data-stu-id="7a0e4-171">IID\_ISWbemSinkEvents</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="7a0e4-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a0e4-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a0e4-173">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="7a0e4-173">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




