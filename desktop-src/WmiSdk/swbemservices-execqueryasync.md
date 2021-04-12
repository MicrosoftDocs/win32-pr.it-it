---
description: Esegue una query per il recupero di oggetti.
ms.assetid: 50c7f62b-dd83-4117-b10e-acee1690ce8c
ms.tgt_platform: multiple
title: Metodo SWbemServices.ExecQueryAsync (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5564e53ef3ea185235e93bbbeb8e2a5fa001d67b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344701"
---
# <a name="swbemservicesexecqueryasync-method"></a><span data-ttu-id="48710-103">Metodo cQueryAsync SWbemServices.Exe</span><span class="sxs-lookup"><span data-stu-id="48710-103">SWbemServices.ExecQueryAsync method</span></span>

<span data-ttu-id="48710-104">Il metodo **ExecQueryAsync** dell'oggetto [**SWbemServices**](swbemservices.md) esegue una query per recuperare gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="48710-104">The **ExecQueryAsync** method of the [**SWbemServices**](swbemservices.md) object executes a query to retrieve objects.</span></span> <span data-ttu-id="48710-105">La chiamata a questo metodo restituisce immediatamente un risultato e i risultati e lo stato vengono restituiti al chiamante tramite gli eventi recapitati al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="48710-105">The call to this method returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="48710-106">Per gestire ogni oggetto restituito, creare un *objWbemSink*. Subroutine dell'evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="48710-106">To handle each returned object, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span>

<span data-ttu-id="48710-107">Il metodo viene chiamato in modalità asincrona.</span><span class="sxs-lookup"><span data-stu-id="48710-107">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="48710-108">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="48710-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="48710-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="48710-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="48710-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48710-110">Syntax</span></span>


```VB
objWbemObjectSet = .ExecQueryAsync( _
  [ ByVal objWbemSink ], _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="48710-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="48710-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48710-112">*objWbemSink* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="48710-112">*objWbemSink* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="48710-113">Sink di oggetto che esegue la query in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="48710-113">Object sink that executes the query asynchronously.</span></span> <span data-ttu-id="48710-114">Creare un oggetto [**SWbemSink**](swbemsink.md) per ricevere gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="48710-114">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="48710-115">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="48710-115">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="48710-116">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="48710-116">Required.</span></span> <span data-ttu-id="48710-117">Stringa che contiene il testo della query.</span><span class="sxs-lookup"><span data-stu-id="48710-117">String that contains the text of the query.</span></span> <span data-ttu-id="48710-118">Questo parametro non può essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="48710-118">This parameter cannot be blank.</span></span> <span data-ttu-id="48710-119">Per ulteriori informazioni sulla creazione di stringhe di query WMI, vedere [esecuzione di query con WQL](querying-with-wql.md) e informazioni di riferimento su [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="48710-119">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="48710-120">*strQueryLanguage* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="48710-120">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="48710-121">Stringa che contiene il linguaggio di query da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="48710-121">String that contains the query language to be used.</span></span> <span data-ttu-id="48710-122">Se specificato, il valore deve essere "WQL".</span><span class="sxs-lookup"><span data-stu-id="48710-122">If specified, the value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="48710-123">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="48710-123">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="48710-124">Integer che determina il comportamento della query.</span><span class="sxs-lookup"><span data-stu-id="48710-124">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="48710-125">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="48710-125">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="48710-126"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="48710-126"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="48710-127">Fa in modo che le chiamate asincrone inviino gli aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="48710-127">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="48710-128"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="48710-128"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="48710-129">Impedisce alle chiamate asincrone di inviare aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="48710-129">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span data-ttu-id="48710-130"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype \* \* \* \* (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="48710-130"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>\*\*\*\*wbemQueryFlagPrototype\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="48710-131">Utilizzato per un prototipo.</span><span class="sxs-lookup"><span data-stu-id="48710-131">Used for a prototype.</span></span> <span data-ttu-id="48710-132">Arresta la query e restituisce invece un oggetto simile a un oggetto risultato tipico.</span><span class="sxs-lookup"><span data-stu-id="48710-132">It stops the query from happening and instead, returns an object that looks like a typical result object.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="48710-133"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="48710-133"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="48710-134">Causa la restituzione dei dati di modifica della classe da parte di WMI con la definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="48710-134">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="48710-135">Per ulteriori informazioni, vedere la pagina relativa alla [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="48710-135">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="48710-136">*objwbemNamedValueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="48710-136">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="48710-137">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="48710-137">Typically, this is undefined.</span></span> <span data-ttu-id="48710-138">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che servizi la richiesta.</span><span class="sxs-lookup"><span data-stu-id="48710-138">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="48710-139">Un provider che supporta o richiede informazioni sul contesto deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="48710-139">A provider that supports or requires context information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="48710-140">*objWbemAsyncContext* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="48710-140">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="48710-141">Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink di oggetto per identificare l'origine della chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="48710-141">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="48710-142">Utilizzare questo parametro per effettuare più chiamate asincrone utilizzando lo stesso sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="48710-142">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="48710-143">Per usare questo parametro, creare un oggetto **SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona che si sta effettuando.</span><span class="sxs-lookup"><span data-stu-id="48710-143">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="48710-144">Questo oggetto **SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta tramite il metodo [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="48710-144">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="48710-145">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="48710-145">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48710-146">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="48710-146">Return value</span></span>

<span data-ttu-id="48710-147">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="48710-147">This method has no return values.</span></span> <span data-ttu-id="48710-148">In caso di esito positivo, il sink riceve un evento [**OnObjectReady**](swbemsink-onobjectready.md) per ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="48710-148">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="48710-149">Dopo l'ultima istanza, il sink di oggetto riceve un evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="48710-149">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="48710-150">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="48710-150">Error codes</span></span>

<span data-ttu-id="48710-151">Dopo il completamento del metodo **ExecQueryAsync** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="48710-151">After the completion of the **ExecQueryAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object can contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="48710-152">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="48710-152">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="48710-153">L'utente corrente non dispone dell'autorizzazione per visualizzare il set di risultati.</span><span class="sxs-lookup"><span data-stu-id="48710-153">Current user does not have the permission to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="48710-154">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="48710-154">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="48710-155">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="48710-155">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="48710-156">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="48710-156">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="48710-157">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="48710-157">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="48710-158">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="48710-158">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="48710-159">Sintassi di query non valida.</span><span class="sxs-lookup"><span data-stu-id="48710-159">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="48710-160">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="48710-160">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="48710-161">Il linguaggio di query richiesto non è supportato.</span><span class="sxs-lookup"><span data-stu-id="48710-161">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="48710-162">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="48710-162">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="48710-163">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="48710-163">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48710-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="48710-164">Remarks</span></span>

<span data-ttu-id="48710-165">Questa chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="48710-165">This call returns immediately.</span></span> <span data-ttu-id="48710-166">Gli oggetti e lo stato richiesti vengono restituiti al chiamante tramite callback recapitati al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="48710-166">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="48710-167">Per elaborare ogni oggetto quando restituisce, creare un *objWbemSink*. Subroutine dell'evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="48710-167">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="48710-168">Dopo la restituzione di tutti gli oggetti, eseguire l'elaborazione finale nell'implementazione di *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="48710-168">After all the objects are returned, perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="48710-169">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="48710-169">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="48710-170">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="48710-170">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="48710-171">Per eliminare i rischi, vedere [impostazione della sicurezza per una chiamata asincrona](setting-security-on-an-asynchronous-call.md)</span><span class="sxs-lookup"><span data-stu-id="48710-171">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md)</span></span>

<span data-ttu-id="48710-172">Il metodo **ExecQueryAsync** restituisce un set di risultati vuoto se non sono presenti oggetti corrispondenti ai criteri della query.</span><span class="sxs-lookup"><span data-stu-id="48710-172">The **ExecQueryAsync** method returns an empty result set when there are no objects to match the criteria in the query.</span></span> <span data-ttu-id="48710-173">Questo metodo restituisce le proprietà chiave se la proprietà [**Key**](standard-qualifiers.md) è richiesta nel parametro *strQuery* .</span><span class="sxs-lookup"><span data-stu-id="48710-173">This method returns key properties whether or not the [**Key**](standard-qualifiers.md) property is requested in the *strQuery* parameter.</span></span>

<span data-ttu-id="48710-174">Esistono limiti al numero di parole chiave **and** e **or** che possono essere utilizzate nelle query WQL.</span><span class="sxs-lookup"><span data-stu-id="48710-174">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="48710-175">Un numero elevato di parole chiave WQL utilizzate in una query complessa può causare la restituzione del \_ codice di errore di violazione della quota E di WBEM \_ \_ come valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="48710-175">Large numbers of WQL keywords used in a complex query can cause WMI to return the WBEM\_E\_QUOTA\_VIOLATION error code as an **HRESULT** value.</span></span> <span data-ttu-id="48710-176">Il limite di parole chiave WQL dipende dalla complessità della query.</span><span class="sxs-lookup"><span data-stu-id="48710-176">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="requirements"></a><span data-ttu-id="48710-177">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48710-177">Requirements</span></span>



| <span data-ttu-id="48710-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="48710-178">Requirement</span></span> | <span data-ttu-id="48710-179">Valore</span><span class="sxs-lookup"><span data-stu-id="48710-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48710-180">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48710-180">Minimum supported client</span></span><br/> | <span data-ttu-id="48710-181">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48710-181">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="48710-182">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48710-182">Minimum supported server</span></span><br/> | <span data-ttu-id="48710-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48710-183">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48710-184">Intestazione</span><span class="sxs-lookup"><span data-stu-id="48710-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="48710-185"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="48710-185"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="48710-186">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="48710-186">Type library</span></span><br/>             | <dl> <span data-ttu-id="48710-187"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="48710-187"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="48710-188">DLL</span><span class="sxs-lookup"><span data-stu-id="48710-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48710-189"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48710-189"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="48710-190">CLSID</span><span class="sxs-lookup"><span data-stu-id="48710-190">CLSID</span></span><br/>                    | <span data-ttu-id="48710-191">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="48710-191">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="48710-192">IID</span><span class="sxs-lookup"><span data-stu-id="48710-192">IID</span></span><br/>                      | <span data-ttu-id="48710-193">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="48710-193">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="48710-194">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48710-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48710-195">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="48710-195">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="48710-196">Chiamata a un metodo</span><span class="sxs-lookup"><span data-stu-id="48710-196">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="48710-197">**SWbemServices. Get**</span><span class="sxs-lookup"><span data-stu-id="48710-197">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> </dl>

 

