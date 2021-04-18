---
description: Esegue una query per la ricezione di eventi. La chiamata restituisce immediatamente un risultato.
ms.assetid: 3e1bb428-5395-4e90-9713-6d96242fef4e
ms.tgt_platform: multiple
title: Metodo SWbemServices.ExecNotificationQuery (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 44279d16e180d776dc4433c6d5246eab2419fca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313164"
---
# <a name="swbemservicesexecnotificationquery-method"></a><span data-ttu-id="ffc28-104">Metodo cNotificationQuery SWbemServices.Exe</span><span class="sxs-lookup"><span data-stu-id="ffc28-104">SWbemServices.ExecNotificationQuery method</span></span>

<span data-ttu-id="ffc28-105">Il metodo **ExecNotificationQuery** dell'oggetto [**SWbemServices**](swbemservices.md) esegue una query per la ricezione di eventi.</span><span class="sxs-lookup"><span data-stu-id="ffc28-105">The **ExecNotificationQuery** method of the [**SWbemServices**](swbemservices.md) object executes a query to receive events.</span></span> <span data-ttu-id="ffc28-106">La chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="ffc28-106">The call returns immediately.</span></span> <span data-ttu-id="ffc28-107">L'utente può eseguire il polling dell'enumeratore restituito per gli eventi man mano che arrivano.</span><span class="sxs-lookup"><span data-stu-id="ffc28-107">The user can poll the returned enumerator for events as they arrive.</span></span>

<span data-ttu-id="ffc28-108">Il metodo viene chiamato in modalità semisincrono.</span><span class="sxs-lookup"><span data-stu-id="ffc28-108">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="ffc28-109">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="ffc28-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="ffc28-110">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ffc28-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ffc28-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ffc28-111">Syntax</span></span>


```VB
objwbemEventsource = .ExecNotificationQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ffc28-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="ffc28-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffc28-113">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="ffc28-113">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="ffc28-114">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ffc28-114">Required.</span></span> <span data-ttu-id="ffc28-115">Stringa che contiene il testo della query correlata agli eventi.</span><span class="sxs-lookup"><span data-stu-id="ffc28-115">String that contains the text of the event-related query.</span></span> <span data-ttu-id="ffc28-116">Questo parametro non può essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="ffc28-116">This parameter cannot be blank.</span></span> <span data-ttu-id="ffc28-117">Per ulteriori informazioni sulla creazione di stringhe di query WMI, vedere [esecuzione di query con WQL](querying-with-wql.md) e informazioni di riferimento su [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="ffc28-117">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="ffc28-118">*strQueryLanguage* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="ffc28-118">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffc28-119">Stringa che contiene il linguaggio di query da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="ffc28-119">String that contains the query language to be used.</span></span> <span data-ttu-id="ffc28-120">Se specificato, questo valore deve essere "WQL".</span><span class="sxs-lookup"><span data-stu-id="ffc28-120">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="ffc28-121">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="ffc28-121">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffc28-122">Si tratta di un numero intero che determina il comportamento della query.</span><span class="sxs-lookup"><span data-stu-id="ffc28-122">This is an integer that determines the behavior of the query.</span></span> <span data-ttu-id="ffc28-123">Il valore predefinito è **wbemFlagReturnImmediately**  +  **wbemFlagForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="ffc28-123">The default value is **wbemFlagReturnImmediately** + **wbemFlagForwardOnly**.</span></span> <span data-ttu-id="ffc28-124">Se si specifica questo parametro, questo parametro deve essere impostato sia su **wbemFlagReturnImmediately** che su **wbemFlagForwardOnly** oppure la chiamata ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ffc28-124">If you specify this parameter, this parameter must be set to both **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** or the call fails.</span></span> <span data-ttu-id="ffc28-125">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ffc28-125">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="ffc28-126"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="ffc28-126"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="ffc28-127">Causa la restituzione di un enumeratore di sola trasmissione.</span><span class="sxs-lookup"><span data-stu-id="ffc28-127">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="ffc28-128">Gli enumeratori di solo avanzamento sono in genere molto più veloci e utilizzano meno memoria rispetto agli enumeratori convenzionali, ma non consentono chiamate a [**SWbemObject \_ . Clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="ffc28-128">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="ffc28-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="ffc28-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="ffc28-130">Causa la restituzione immediata della chiamata.</span><span class="sxs-lookup"><span data-stu-id="ffc28-130">Causes the call to return immediately.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ffc28-131">*objWbemNamedValueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="ffc28-131">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffc28-132">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="ffc28-132">Typically, this is undefined.</span></span> <span data-ttu-id="ffc28-133">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ffc28-133">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="ffc28-134">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="ffc28-134">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffc28-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ffc28-135">Return value</span></span>

<span data-ttu-id="ffc28-136">Se non si verificano errori, questo metodo restituisce un oggetto [**SWbemEventSource**](swbemeventsource.md) .</span><span class="sxs-lookup"><span data-stu-id="ffc28-136">If no error occurs, this method returns an [**SWbemEventSource**](swbemeventsource.md) object.</span></span> <span data-ttu-id="ffc28-137">È possibile chiamare il metodo [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) per recuperare gli eventi man mano che arrivano.</span><span class="sxs-lookup"><span data-stu-id="ffc28-137">You can call the [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) method to retrieve events as they arrive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ffc28-138">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ffc28-138">Error codes</span></span>

<span data-ttu-id="ffc28-139">Dopo il completamento del metodo **ExecNotificationQuery** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="ffc28-139">After the completion of the **ExecNotificationQuery** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="ffc28-140">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="ffc28-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="ffc28-141">L'utente corrente non è autorizzato a visualizzare il set di risultati.</span><span class="sxs-lookup"><span data-stu-id="ffc28-141">Current user is not authorized to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="ffc28-142">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="ffc28-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ffc28-143">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="ffc28-143">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="ffc28-144">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="ffc28-144">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="ffc28-145">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="ffc28-145">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="ffc28-146">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="ffc28-146">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="ffc28-147">Sintassi di query non valida.</span><span class="sxs-lookup"><span data-stu-id="ffc28-147">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ffc28-148">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="ffc28-148">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="ffc28-149">Il linguaggio della query richiesta non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ffc28-149">The requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ffc28-150">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="ffc28-150">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="ffc28-151">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ffc28-151">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ffc28-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="ffc28-152">Remarks</span></span>

<span data-ttu-id="ffc28-153">A differenza del metodo [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) , **ExecNotificationQuery** restituisce gli oggetti del tipo di evento generati da eventi futuri anziché da oggetti esistenti.</span><span class="sxs-lookup"><span data-stu-id="ffc28-153">Unlike the [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) method, **ExecNotificationQuery** returns event type objects that are generated by future events rather than existing objects.</span></span> <span data-ttu-id="ffc28-154">Gli oggetti evento che **ExecNotificationQuery** le richieste possono essere intrinseci, ad esempio [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md), o estrinseci, ad esempio eventi del provider del registro di sistema come gli eventi [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) o SNMP.</span><span class="sxs-lookup"><span data-stu-id="ffc28-154">The event objects that **ExecNotificationQuery** requests can either be intrinsic (such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md)) or extrinsic (such as registry provider events like [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) or SNMP events).</span></span> <span data-ttu-id="ffc28-155">Per ulteriori informazioni, vedere [determinazione del tipo di evento per la ricezione e la ricezione di notifiche degli](determining-the-type-of-event-to-receive.md) [eventi](receiving-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="ffc28-155">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md) and [Receiving Event Notifications](receiving-event-notifications.md).</span></span>

<span data-ttu-id="ffc28-156">Esistono limiti al numero di parole chiave **and** e **or** che possono essere utilizzate nelle query WQL.</span><span class="sxs-lookup"><span data-stu-id="ffc28-156">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="ffc28-157">Un numero elevato di parole chiave WQL utilizzate in una query complessa può causare la restituzione del codice di errore di **\_ \_ \_ violazione della quota E di WBEM** come valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ffc28-157">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="ffc28-158">Il limite di parole chiave WQL dipende dalla complessità della query.</span><span class="sxs-lookup"><span data-stu-id="ffc28-158">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="ffc28-159">Esempio</span><span class="sxs-lookup"><span data-stu-id="ffc28-159">Examples</span></span>

<span data-ttu-id="ffc28-160">Nell'esempio di codice VBScript seguente vengono monitorate le modifiche apportate ai volumi in un computer locale.</span><span class="sxs-lookup"><span data-stu-id="ffc28-160">The following VBScript code example monitors changes to volumes on a local computer.</span></span> <span data-ttu-id="ffc28-161">Si noti che [**Win32 \_ VolumeChangeEvent**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) è un evento estrinseco definito da un provider e non da un evento intrinseco WMI definito.</span><span class="sxs-lookup"><span data-stu-id="ffc28-161">Note that [**Win32\_VolumeChangeEvent**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) is an extrinsic event that is defined by a provider not an intrinsic WMI-defined event.</span></span> <span data-ttu-id="ffc28-162">Per ulteriori informazioni, vedere [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="ffc28-162">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>


```VB
Set colMonitoredEvents = _
   GetObject("Winmgmts:").ExecNotificationQuery_
      ("Select * from Win32_VolumeChangeEvent")

Do While i = 0
   Set strLatestEvent = colMonitoredEvents.NextEvent
   Wscript.Echo strLatestEvent.DriveName & "Time Created = " _
      & strLatestEvent.Time_Created

    Select Case strLatestEvent.EventType 
       Case 1        
            WScript.Echo "EventType = Configuration Changed"
       Case 2
            WScript.Echo "EventType = Device Arrival"
       Case 3
            WScript.Echo "EventType = Device Removal"
       Case 4
            WScript.Echo "EventType = Docking"

       Case Else
            WScript.Echo "Unrecognized EventType"
       End Select
Loop
```



<span data-ttu-id="ffc28-163">Nell'esempio di codice VBScript riportato di seguito viene monitorata l'eliminazione del processo.</span><span class="sxs-lookup"><span data-stu-id="ffc28-163">The following VBScript code example monitors process deletion.</span></span> <span data-ttu-id="ffc28-164">Se si elimina un processo in Gestione attività o si chiude un'applicazione, lo script Visualizza un messaggio.</span><span class="sxs-lookup"><span data-stu-id="ffc28-164">If you delete a process in Task Manager or close an application, then the script displays a message.</span></span> <span data-ttu-id="ffc28-165">Si noti che questo script esegue una query su un evento intrinseco definito da WMI- [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md).</span><span class="sxs-lookup"><span data-stu-id="ffc28-165">Note that this script queries an intrinsic event that is defined by WMI - [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md).</span></span>


```VB
Set objWMIService = GetObject( _
    "Winmgmts:{impersonationLevel=impersonate}" )
Set colMonitoredProcesses = _
    objWMIService.ExecNotificationQuery( _
    "SELECT * FROM __InstanceDeletionEvent WITHIN 10 WHERE " _
    & "TargetInstance ISA 'Win32_Process'")
i = 0
Do While i < 11
    Set strLatestProcess = colMonitoredProcesses.NextEvent
    WScript.Echo strLatestProcess.TargetInstance.Name
    WScript.Sleep 10000
    i= i + 1
Loop
```



## <a name="requirements"></a><span data-ttu-id="ffc28-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ffc28-166">Requirements</span></span>



| <span data-ttu-id="ffc28-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffc28-167">Requirement</span></span> | <span data-ttu-id="ffc28-168">Valore</span><span class="sxs-lookup"><span data-stu-id="ffc28-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffc28-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffc28-169">Minimum supported client</span></span><br/> | <span data-ttu-id="ffc28-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ffc28-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ffc28-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffc28-171">Minimum supported server</span></span><br/> | <span data-ttu-id="ffc28-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffc28-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ffc28-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ffc28-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffc28-174"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffc28-174"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ffc28-175">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ffc28-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="ffc28-176"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ffc28-176"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ffc28-177">DLL</span><span class="sxs-lookup"><span data-stu-id="ffc28-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffc28-178"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffc28-178"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ffc28-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="ffc28-179">CLSID</span></span><br/>                    | <span data-ttu-id="ffc28-180">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="ffc28-180">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="ffc28-181">IID</span><span class="sxs-lookup"><span data-stu-id="ffc28-181">IID</span></span><br/>                      | <span data-ttu-id="ffc28-182">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="ffc28-182">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="ffc28-183">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffc28-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffc28-184">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="ffc28-184">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="ffc28-185">**SWbemEventSource. NextEvent**</span><span class="sxs-lookup"><span data-stu-id="ffc28-185">**SWbemEventSource.NextEvent**</span></span>](swbemeventsource-nextevent.md)
</dt> <dt>

[<span data-ttu-id="ffc28-186">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="ffc28-186">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
</dt> <dt>

[<span data-ttu-id="ffc28-187">Ricezione di un evento WMI</span><span class="sxs-lookup"><span data-stu-id="ffc28-187">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)
</dt> <dt>

[<span data-ttu-id="ffc28-188">Esecuzione di query con WQL</span><span class="sxs-lookup"><span data-stu-id="ffc28-188">Querying with WQL</span></span>](querying-with-wql.md)
</dt> <dt>

[<span data-ttu-id="ffc28-189">WQL (SQL per WMI)</span><span class="sxs-lookup"><span data-stu-id="ffc28-189">WQL (SQL for WMI)</span></span>](wql-sql-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="ffc28-190">Determinazione del tipo di evento da ricevere</span><span class="sxs-lookup"><span data-stu-id="ffc28-190">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

