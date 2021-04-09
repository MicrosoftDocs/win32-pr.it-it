---
description: Il \_ Metodo InstancesAsync di SWbemObject fornisce in modo asincrono le istanze dell'oggetto classe corrente. Questo metodo implementa una semplice query. Query più complesse possono richiedere l'uso di SWbemServices.ExecQuery.
ms.assetid: d10fcbbf-6110-4152-8201-db43dc7a3c14
ms.tgt_platform: multiple
title: Metodo SWbemObject.InstancesAsync_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.InstancesAsync_
- ISWbemObject.InstancesAsync_
- ISWbemObject.InstancesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 800e28184593e339f739fb52d488803666f552c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880425"
---
# <a name="swbemobjectinstancesasync_-method"></a><span data-ttu-id="127fc-105">SWbemObject. InstancesAsync, \_ Metodo</span><span class="sxs-lookup"><span data-stu-id="127fc-105">SWbemObject.InstancesAsync\_ method</span></span>

<span data-ttu-id="127fc-106">Il **metodo \_ InstancesAsync** di [**SWbemObject**](swbemobject.md) fornisce in modo asincrono le istanze dell'oggetto classe corrente.</span><span class="sxs-lookup"><span data-stu-id="127fc-106">The **InstancesAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously supplies the instances of the current class object.</span></span> <span data-ttu-id="127fc-107">Questo metodo implementa una semplice query.</span><span class="sxs-lookup"><span data-stu-id="127fc-107">This method implements a simple query.</span></span> <span data-ttu-id="127fc-108">Query più complesse possono richiedere l'uso di [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="127fc-108">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="127fc-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="127fc-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="127fc-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="127fc-110">Syntax</span></span>


```VB
SWbemObject.InstancesAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="127fc-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="127fc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="127fc-112">*objWbemSink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="127fc-112">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="127fc-113">Sink di oggetto che restituisce le istanze di.</span><span class="sxs-lookup"><span data-stu-id="127fc-113">Object sink that returns the instances.</span></span>

</dd> <dt>

<span data-ttu-id="127fc-114">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="127fc-114">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="127fc-115">Integer che determina il comportamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="127fc-115">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="127fc-116">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="127fc-116">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="127fc-117"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="127fc-117"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="127fc-118">Fa in modo che le chiamate asincrone inviino gli aggiornamenti di stato al gestore eventi [**SWbemSink. OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="127fc-118">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="127fc-119"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="127fc-119"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="127fc-120">Impedisce alle chiamate asincrone di inviare aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="127fc-120">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="127fc-121"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="127fc-121"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="127fc-122">Fa in modo che WMI restituisca la classe localizzata e le descrizioni di proprietà.</span><span class="sxs-lookup"><span data-stu-id="127fc-122">Causes WMI to return the localized class and property descriptions.</span></span> <span data-ttu-id="127fc-123">Per ulteriori informazioni, vedere la pagina relativa alla [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="127fc-123">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="127fc-124">*objwbemNamedValueSet* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="127fc-124">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="127fc-125">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="127fc-125">Typically, this is undefined.</span></span> <span data-ttu-id="127fc-126">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="127fc-126">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="127fc-127">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="127fc-127">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="127fc-128">*objWbemAsyncContext* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="127fc-128">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="127fc-129">Si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink di oggetto per identificare l'origine della chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="127fc-129">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="127fc-130">Utilizzare questo parametro se si eseguono più chiamate asincrone utilizzando lo stesso sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="127fc-130">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="127fc-131">Per usare questo parametro, creare un oggetto **SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona che si sta effettuando.</span><span class="sxs-lookup"><span data-stu-id="127fc-131">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="127fc-132">Questo oggetto **SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta tramite il metodo [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="127fc-132">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="127fc-133">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="127fc-133">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="127fc-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="127fc-134">Return value</span></span>

<span data-ttu-id="127fc-135">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="127fc-135">This method does not return a value.</span></span> <span data-ttu-id="127fc-136">In caso di esito positivo, il sink riceve un evento [**OnObjectReady**](swbemsink-onobjectready.md) per ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="127fc-136">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="127fc-137">Dopo l'ultima istanza, il sink di oggetto riceverà un evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="127fc-137">After the last instance, the object sink will receive an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="127fc-138">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="127fc-138">Error codes</span></span>

<span data-ttu-id="127fc-139">Dopo il completamento del metodo **InstancesAsync \_** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="127fc-139">After the completion of the **InstancesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="127fc-140">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="127fc-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="127fc-141">L'utente corrente non dispone delle autorizzazioni necessarie per visualizzare le istanze della classe specificata.</span><span class="sxs-lookup"><span data-stu-id="127fc-141">Current user does not have permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="127fc-142">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="127fc-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="127fc-143">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="127fc-143">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="127fc-144">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="127fc-144">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="127fc-145">La classe specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="127fc-145">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="127fc-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="127fc-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="127fc-147">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="127fc-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="127fc-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="127fc-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="127fc-149">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="127fc-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="127fc-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="127fc-150">Remarks</span></span>

<span data-ttu-id="127fc-151">Questa chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="127fc-151">This call returns immediately.</span></span> <span data-ttu-id="127fc-152">Gli oggetti e lo stato richiesti vengono restituiti al chiamante tramite callback recapitati al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="127fc-152">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="127fc-153">Per elaborare ogni oggetto all'arrivo, creare un *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="127fc-153">To process each object when it arrives, create an *objWbemSink*.</span></span> <span data-ttu-id="127fc-154">Subroutine dell'evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="127fc-154">[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="127fc-155">Dopo la restituzione di tutti gli oggetti, è possibile eseguire l'elaborazione finale nell'implementazione di *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="127fc-155">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.</span></span> <span data-ttu-id="127fc-156">Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="127fc-156">[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="127fc-157">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="127fc-157">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="127fc-158">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="127fc-158">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="127fc-159">Per eliminare i rischi, usare la comunicazione semisincrono o la comunicazione sincrona.</span><span class="sxs-lookup"><span data-stu-id="127fc-159">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="127fc-160">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="127fc-160">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="127fc-161">Il **metodo \_ InstancesAsync** funziona solo per gli oggetti classe.</span><span class="sxs-lookup"><span data-stu-id="127fc-161">The **InstancesAsync\_** method only works for class objects.</span></span> <span data-ttu-id="127fc-162">Non si tratta di un errore per la raccolta restituita con zero (0) elementi.</span><span class="sxs-lookup"><span data-stu-id="127fc-162">It is not an error for the returned collection to have zero (0) elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="127fc-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="127fc-163">Requirements</span></span>



| <span data-ttu-id="127fc-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="127fc-164">Requirement</span></span> | <span data-ttu-id="127fc-165">Valore</span><span class="sxs-lookup"><span data-stu-id="127fc-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="127fc-166">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="127fc-166">Minimum supported client</span></span><br/> | <span data-ttu-id="127fc-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="127fc-167">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="127fc-168">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="127fc-168">Minimum supported server</span></span><br/> | <span data-ttu-id="127fc-169">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="127fc-169">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="127fc-170">Intestazione</span><span class="sxs-lookup"><span data-stu-id="127fc-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="127fc-171"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="127fc-171"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="127fc-172">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="127fc-172">Type library</span></span><br/>             | <dl> <span data-ttu-id="127fc-173"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="127fc-173"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="127fc-174">DLL</span><span class="sxs-lookup"><span data-stu-id="127fc-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="127fc-175"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="127fc-175"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="127fc-176">CLSID</span><span class="sxs-lookup"><span data-stu-id="127fc-176">CLSID</span></span><br/>                    | <span data-ttu-id="127fc-177">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="127fc-177">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="127fc-178">IID</span><span class="sxs-lookup"><span data-stu-id="127fc-178">IID</span></span><br/>                      | <span data-ttu-id="127fc-179">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="127fc-179">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="127fc-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="127fc-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="127fc-181">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="127fc-181">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="127fc-182">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="127fc-182">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

