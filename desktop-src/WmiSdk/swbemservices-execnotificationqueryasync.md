---
description: Esegue una query per la ricezione di eventi.
ms.assetid: 0b0e8313-4ffd-4d4a-8965-d2c6743e7573
ms.tgt_platform: multiple
title: Metodo SWbemServices.ExecNotificationQueryAsync (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8e2ecddf290d83583b3108620b8b4bb23be7c957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309779"
---
# <a name="swbemservicesexecnotificationqueryasync-method"></a><span data-ttu-id="4cb39-103">Metodo cNotificationQueryAsync SWbemServices.Exe</span><span class="sxs-lookup"><span data-stu-id="4cb39-103">SWbemServices.ExecNotificationQueryAsync method</span></span>

<span data-ttu-id="4cb39-104">Il metodo **ExecNotificationQueryAsync** dell'oggetto [**SWbemServices**](swbemservices.md) esegue una query per la ricezione di eventi.</span><span class="sxs-lookup"><span data-stu-id="4cb39-104">The **ExecNotificationQueryAsync** method of the [**SWbemServices**](swbemservices.md) object executes a query to receive events.</span></span> <span data-ttu-id="4cb39-105">Questa chiamata restituisce immediatamente un risultato e i risultati e lo stato vengono restituiti al chiamante tramite gli eventi recapitati al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="4cb39-105">This call returns immediately and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span>

<span data-ttu-id="4cb39-106">Gli eventi specificati nella query possono essere eventi Strumentazione gestione Windows (WMI) intrinseci, ad esempio [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md), o eventi estrinseci, ad esempio [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) o [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span><span class="sxs-lookup"><span data-stu-id="4cb39-106">The events that are specified in the query can be intrinsic Windows Management Instrumentation (WMI) events, such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md), or extrinsic events, such as [**Win32\_IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) or [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span> <span data-ttu-id="4cb39-107">Per ulteriori informazioni, vedere [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="4cb39-107">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="4cb39-108">Il metodo viene chiamato in modalità asincrona.</span><span class="sxs-lookup"><span data-stu-id="4cb39-108">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="4cb39-109">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="4cb39-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="4cb39-110">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="4cb39-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4cb39-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4cb39-111">Syntax</span></span>


```VB
SWbemServices.ExecNotificationQueryAsync( _
  ByVal objWbemSink, _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4cb39-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="4cb39-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cb39-113">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="4cb39-113">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="4cb39-114">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="4cb39-114">Required.</span></span> <span data-ttu-id="4cb39-115">Sink di oggetto che riceve la notifica degli eventi in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="4cb39-115">Object sink that receives the notification of events asynchronously.</span></span> <span data-ttu-id="4cb39-116">Creare un oggetto [**SWbemSink**](swbemsink.md) per ricevere gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="4cb39-116">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="4cb39-117">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="4cb39-117">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="4cb39-118">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="4cb39-118">Required.</span></span> <span data-ttu-id="4cb39-119">Stringa che contiene il testo della query correlata agli eventi.</span><span class="sxs-lookup"><span data-stu-id="4cb39-119">String that contains the text of the event-related query.</span></span> <span data-ttu-id="4cb39-120">Questo parametro non può essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="4cb39-120">This parameter cannot be blank.</span></span> <span data-ttu-id="4cb39-121">Per ulteriori informazioni sulla creazione di stringhe di query WMI, vedere [esecuzione di query con WQL](querying-with-wql.md) e informazioni di riferimento su [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="4cb39-121">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="4cb39-122">*strQueryLanguage* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="4cb39-122">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb39-123">Stringa che contiene il linguaggio di query da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="4cb39-123">String that contains the query language to be used.</span></span> <span data-ttu-id="4cb39-124">Se specificato, questo valore deve essere "WQL".</span><span class="sxs-lookup"><span data-stu-id="4cb39-124">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="4cb39-125">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="4cb39-125">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb39-126">Integer che determina il comportamento della query.</span><span class="sxs-lookup"><span data-stu-id="4cb39-126">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="4cb39-127">Questo parametro può essere impostato sui valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4cb39-127">This parameter can be set to the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="4cb39-128"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="4cb39-128"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="4cb39-129">Fa in modo che le chiamate asincrone inviino gli aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4cb39-129">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="4cb39-130"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="4cb39-130"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="4cb39-131">Impedisce alle chiamate asincrone di inviare aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4cb39-131">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4cb39-132">*objwbemNamedValueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="4cb39-132">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb39-133">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="4cb39-133">Typically, this is undefined.</span></span> <span data-ttu-id="4cb39-134">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che servizi la richiesta.</span><span class="sxs-lookup"><span data-stu-id="4cb39-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="4cb39-135">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="4cb39-135">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="4cb39-136">*objWbemAsyncContext* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="4cb39-136">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb39-137">Si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink di oggetto per identificare l'origine della chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="4cb39-137">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="4cb39-138">Utilizzare questo parametro per effettuare più chiamate asincrone utilizzando lo stesso sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="4cb39-138">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="4cb39-139">Per usare questo parametro, creare un oggetto **SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona che si sta effettuando.</span><span class="sxs-lookup"><span data-stu-id="4cb39-139">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="4cb39-140">L'oggetto **SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta tramite il metodo [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="4cb39-140">The **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="4cb39-141">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="4cb39-141">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cb39-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4cb39-142">Return value</span></span>

<span data-ttu-id="4cb39-143">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="4cb39-143">This method does not return a value.</span></span> <span data-ttu-id="4cb39-144">In caso di esito positivo, il sink riceve un evento [**OnObjectReady**](swbemsink-onobjectready.md) per ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="4cb39-144">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="4cb39-145">Dopo l'ultima istanza, il sink di oggetto riceve un evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="4cb39-145">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4cb39-146">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="4cb39-146">Error codes</span></span>

<span data-ttu-id="4cb39-147">Dopo il completamento del metodo **ExecNotificationQueryAsync** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore indicati nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="4cb39-147">After the completion of the **ExecNotificationQueryAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes identified in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="4cb39-148">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="4cb39-148">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="4cb39-149">L'utente corrente non è autorizzato a visualizzare il set di risultati.</span><span class="sxs-lookup"><span data-stu-id="4cb39-149">Current user is not authorized to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="4cb39-150">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="4cb39-150">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="4cb39-151">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="4cb39-151">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="4cb39-152">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="4cb39-152">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="4cb39-153">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="4cb39-153">Invalid parameter is specified.</span></span>

</dd> <dt>

<span data-ttu-id="4cb39-154">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="4cb39-154">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="4cb39-155">Sintassi di query non valida.</span><span class="sxs-lookup"><span data-stu-id="4cb39-155">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4cb39-156">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="4cb39-156">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="4cb39-157">Il linguaggio di query richiesto non è supportato.</span><span class="sxs-lookup"><span data-stu-id="4cb39-157">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4cb39-158">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="4cb39-158">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="4cb39-159">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="4cb39-159">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4cb39-160">Commenti</span><span class="sxs-lookup"><span data-stu-id="4cb39-160">Remarks</span></span>

<span data-ttu-id="4cb39-161">Il metodo **ExecNotificationQueryAsync** restituisce gli oggetti del tipo di evento generati dagli eventi futuri.</span><span class="sxs-lookup"><span data-stu-id="4cb39-161">The **ExecNotificationQueryAsync** method returns event type objects that future events generate.</span></span> <span data-ttu-id="4cb39-162">Gli oggetti evento che **ExecNotificationQueryAsync** le richieste possono essere intrinseci (ad esempio, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) o estrinseci (ad esempio, [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) o eventi SNMP).</span><span class="sxs-lookup"><span data-stu-id="4cb39-162">The event objects that **ExecNotificationQueryAsync** requests can be intrinsic (for example, [**\_\_InstanceCreationEvent**](--instancecreationevent.md)), or extrinsic (for example, [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) or SNMP events).</span></span> <span data-ttu-id="4cb39-163">Per ulteriori informazioni, vedere [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="4cb39-163">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="4cb39-164">La chiamata a **ExecNotificationQueryAsync** restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="4cb39-164">The call to **ExecNotificationQueryAsync** returns immediately.</span></span> <span data-ttu-id="4cb39-165">Gli oggetti e lo stato richiesti vengono restituiti al chiamante tramite callback recapitati al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="4cb39-165">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="4cb39-166">Per elaborare ogni oggetto quando viene restituito, creare un *objWbemSink*. Subroutine dell'evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="4cb39-166">To process each object when it is returned, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="4cb39-167">Dopo la restituzione di tutti gli oggetti, eseguire l'elaborazione finale per implementare *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="4cb39-167">After all the objects are returned, perform the final processing to implement the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="4cb39-168">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="4cb39-168">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="4cb39-169">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="4cb39-169">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="4cb39-170">Per eliminare i rischi, vedere [impostazione della sicurezza per una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="4cb39-170">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="4cb39-171">Esistono limiti al numero di parole chiave **and** e **or** che possono essere utilizzate nelle query WQL.</span><span class="sxs-lookup"><span data-stu-id="4cb39-171">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="4cb39-172">Un numero elevato di parole chiave WQL utilizzate in una query complessa può causare la restituzione da parte di WMI del codice **errore Asan** **E della \_ \_ \_ violazione della quota** .</span><span class="sxs-lookup"><span data-stu-id="4cb39-172">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code asan **HRESULT** value.</span></span> <span data-ttu-id="4cb39-173">Il limite di parole chiave WQL dipende dalla complessità della query.</span><span class="sxs-lookup"><span data-stu-id="4cb39-173">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="4cb39-174">Esempio</span><span class="sxs-lookup"><span data-stu-id="4cb39-174">Examples</span></span>

<span data-ttu-id="4cb39-175">Nell'esempio di codice VBScript riportato di seguito viene illustrato uno script in attesa di una notifica degli eventi WMI che indica che un processo è stato terminato.</span><span class="sxs-lookup"><span data-stu-id="4cb39-175">The following VBScript code example shows a script that is waiting for a WMI event notification that indicates that a process has terminated.</span></span> <span data-ttu-id="4cb39-176">È in attesa di un evento intrinseco WMI, un'istanza della classe di evento [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md).</span><span class="sxs-lookup"><span data-stu-id="4cb39-176">It is waiting for a WMI intrinsic event, an instance of the event class [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md).</span></span> <span data-ttu-id="4cb39-177">**\_ \_ InstanceDeletionEvent** deve rappresentare l'eliminazione di un'istanza del [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="4cb39-177">The **\_\_InstanceDeletionEvent** must represent the deletion of an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span> <span data-ttu-id="4cb39-178">Per ulteriori informazioni sugli eventi intrinseci WMI, vedere [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="4cb39-178">For more information about WMI intrinsic events, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="4cb39-179">Lo script seguente viene eseguito a tempo indefinito fino a quando il computer non viene riavviato, WMI viene arrestato o lo script viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="4cb39-179">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="4cb39-180">Per arrestare manualmente lo script, utilizzare Gestione attività per arrestare il processo.</span><span class="sxs-lookup"><span data-stu-id="4cb39-180">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="4cb39-181">Per arrestarla a livello di codice, usare il metodo [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) nella \_ classe del processo Win32.</span><span class="sxs-lookup"><span data-stu-id="4cb39-181">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, "SELECT * FROM __InstanceCreationEvent WITHIN 1 " _
                                               & "WHERE TargetInstance ISA 'Win32_Process'"

WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo "Event occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="requirements"></a><span data-ttu-id="4cb39-182">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4cb39-182">Requirements</span></span>



| <span data-ttu-id="4cb39-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cb39-183">Requirement</span></span> | <span data-ttu-id="4cb39-184">Valore</span><span class="sxs-lookup"><span data-stu-id="4cb39-184">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cb39-185">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4cb39-185">Minimum supported client</span></span><br/> | <span data-ttu-id="4cb39-186">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4cb39-186">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4cb39-187">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4cb39-187">Minimum supported server</span></span><br/> | <span data-ttu-id="4cb39-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4cb39-188">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4cb39-189">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4cb39-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cb39-190"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cb39-190"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4cb39-191">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4cb39-191">Type library</span></span><br/>             | <dl> <span data-ttu-id="4cb39-192"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4cb39-192"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4cb39-193">DLL</span><span class="sxs-lookup"><span data-stu-id="4cb39-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cb39-194"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cb39-194"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4cb39-195">CLSID</span><span class="sxs-lookup"><span data-stu-id="4cb39-195">CLSID</span></span><br/>                    | <span data-ttu-id="4cb39-196">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="4cb39-196">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="4cb39-197">IID</span><span class="sxs-lookup"><span data-stu-id="4cb39-197">IID</span></span><br/>                      | <span data-ttu-id="4cb39-198">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="4cb39-198">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="4cb39-199">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4cb39-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cb39-200">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="4cb39-200">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="4cb39-201">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="4cb39-201">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
</dt> <dt>

[<span data-ttu-id="4cb39-202">**SWbemServices.ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="4cb39-202">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)
</dt> <dt>

[<span data-ttu-id="4cb39-203">Registrazione per eventi registro di sistema</span><span class="sxs-lookup"><span data-stu-id="4cb39-203">Registering for System Registry Events</span></span>](registering-for-system-registry-events.md)
</dt> <dt>

[<span data-ttu-id="4cb39-204">Determinazione del tipo di evento da ricevere</span><span class="sxs-lookup"><span data-stu-id="4cb39-204">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="4cb39-205">Chiamata a un metodo</span><span class="sxs-lookup"><span data-stu-id="4cb39-205">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="4cb39-206">Impostazione della sicurezza per una chiamata asincrona</span><span class="sxs-lookup"><span data-stu-id="4cb39-206">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
</dt> </dl>

 

