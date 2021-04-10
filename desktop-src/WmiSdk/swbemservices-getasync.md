---
description: Recupera un oggetto, ovvero una definizione di classe o un'istanza, in base al percorso dell'oggetto.
ms.assetid: 8da46851-52b8-4b5a-8c9d-1d492f57f4b6
ms.tgt_platform: multiple
title: Metodo SWbemServices. GetAsync (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.GetAsync
- ISWbemServices.GetAsync
- ISWbemServices.GetAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 451f13bde9458e7d57ec393f42b92a4092c99924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880405"
---
# <a name="swbemservicesgetasync-method"></a><span data-ttu-id="c428b-103">SWbemServices. GetAsync, metodo</span><span class="sxs-lookup"><span data-stu-id="c428b-103">SWbemServices.GetAsync method</span></span>

<span data-ttu-id="c428b-104">Il metodo **GetAsync** dell'oggetto [**SWbemServices**](swbemservices.md) recupera un oggetto, ovvero una definizione di classe o un'istanza, in base al percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c428b-104">The **GetAsync** method of the [**SWbemServices**](swbemservices.md) object retrieves an object, that is a class definition or an instance, based on the object path.</span></span>

<span data-ttu-id="c428b-105">Questo metodo recupera solo gli oggetti dallo spazio dei nomi associato all'oggetto [**SWbemServices**](swbemservices.md) corrente.</span><span class="sxs-lookup"><span data-stu-id="c428b-105">This method retrieves only objects from the namespace that is associated with the current [**SWbemServices**](swbemservices.md) object.</span></span>

<span data-ttu-id="c428b-106">Questo metodo viene chiamato in modalità asincrona.</span><span class="sxs-lookup"><span data-stu-id="c428b-106">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="c428b-107">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="c428b-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="c428b-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c428b-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c428b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c428b-109">Syntax</span></span>


```VB
SWbemServices.GetAsync( _
  ByVal objWbemSink, _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c428b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c428b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c428b-111">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="c428b-111">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="c428b-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c428b-112">Required.</span></span> <span data-ttu-id="c428b-113">Sink di oggetto che ottiene gli oggetti in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="c428b-113">Object sink that gets objects asynchronously.</span></span> <span data-ttu-id="c428b-114">Creare un oggetto [**SWbemSink**](swbemsink.md) per ricevere gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="c428b-114">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="c428b-115">*strObjectPath* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="c428b-115">*strObjectPath* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c428b-116">Percorso dell'oggetto che si desidera recuperare.</span><span class="sxs-lookup"><span data-stu-id="c428b-116">Path of the object that you want to retrieve.</span></span> <span data-ttu-id="c428b-117">Se questo valore è vuoto, l'oggetto vuoto restituito può diventare una nuova classe.</span><span class="sxs-lookup"><span data-stu-id="c428b-117">If this value is empty, the empty object that is returned can become a new class.</span></span> <span data-ttu-id="c428b-118">Per ulteriori informazioni, vedere [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="c428b-118">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="c428b-119">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="c428b-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c428b-120">Integer che determina il comportamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="c428b-120">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="c428b-121">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c428b-121">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="c428b-122"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="c428b-122"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="c428b-123">Fa in modo che le chiamate asincrone inviino gli aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c428b-123">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="c428b-124"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="c428b-124"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c428b-125">Impedisce alle chiamate asincrone di inviare aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c428b-125">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="c428b-126"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="c428b-126"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="c428b-127">Causa la restituzione dei dati di modifica della classe da parte di WMI con la definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="c428b-127">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="c428b-128">Per ulteriori informazioni, vedere la pagina relativa alla [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="c428b-128">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c428b-129">*objwbemNamedValueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="c428b-129">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c428b-130">In genere, questo valore non è definito.</span><span class="sxs-lookup"><span data-stu-id="c428b-130">Typically, this value is undefined.</span></span> <span data-ttu-id="c428b-131">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="c428b-131">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="c428b-132">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="c428b-132">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="c428b-133">*objWbemAsyncContext* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="c428b-133">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c428b-134">Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink di oggetto per identificare l'origine della chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="c428b-134">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="c428b-135">Utilizzare questo parametro se si eseguono più chiamate asincrone utilizzando lo stesso sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="c428b-135">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="c428b-136">Per usare questo parametro, creare un oggetto **SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona che si sta effettuando.</span><span class="sxs-lookup"><span data-stu-id="c428b-136">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="c428b-137">Questo oggetto **SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta tramite il metodo [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="c428b-137">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="c428b-138">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="c428b-138">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c428b-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c428b-139">Return value</span></span>

<span data-ttu-id="c428b-140">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c428b-140">This method does not return a value.</span></span> <span data-ttu-id="c428b-141">Se l'esito è positivo, il sink riceve un evento [**OnObjectReady**](swbemsink-onobjectready.md) quando l'oggetto è disponibile.</span><span class="sxs-lookup"><span data-stu-id="c428b-141">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event when the object is available.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c428b-142">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c428b-142">Error codes</span></span>

<span data-ttu-id="c428b-143">Dopo il completamento del metodo **GetAsync** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="c428b-143">After the completion of the **GetAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="c428b-144">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="c428b-144">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="c428b-145">L'utente corrente non dispone dell'autorizzazione per accedere all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c428b-145">Current user does not have the permission to access the object.</span></span>

</dd> <dt>

<span data-ttu-id="c428b-146">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="c428b-146">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c428b-147">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="c428b-147">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="c428b-148">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="c428b-148">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="c428b-149">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="c428b-149">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c428b-150">**wbemErrInvalidObjectPath** -2147749946 (0x8004103A)</span><span class="sxs-lookup"><span data-stu-id="c428b-150">**wbemErrInvalidObjectPath** - 2147749946 (0x8004103A)</span></span>
</dt> <dd>

<span data-ttu-id="c428b-151">Il percorso specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="c428b-151">Specified path was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c428b-152">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="c428b-152">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="c428b-153">Impossibile trovare l'oggetto richiesto.</span><span class="sxs-lookup"><span data-stu-id="c428b-153">Requested object could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="c428b-154">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="c428b-154">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="c428b-155">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="c428b-155">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c428b-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="c428b-156">Remarks</span></span>

<span data-ttu-id="c428b-157">Questa chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="c428b-157">This call returns immediately.</span></span> <span data-ttu-id="c428b-158">L'oggetto richiesto e lo stato vengono restituiti al chiamante tramite un callback recapitato al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="c428b-158">The requested object and status are returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="c428b-159">Per elaborare l'oggetto quando restituisce, creare un *objWbemSink*. [**OnObjectReady**](swbemsink-onobjectready.md)o *objWbemSink*. Sottoroutine di evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="c428b-159">To process the object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md), or an *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event subroutine.</span></span>

<span data-ttu-id="c428b-160">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="c428b-160">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="c428b-161">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c428b-161">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="c428b-162">Per eliminare i rischi, utilizzare semisincrono o la comunicazione sincrona.</span><span class="sxs-lookup"><span data-stu-id="c428b-162">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="c428b-163">Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="c428b-163">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c428b-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c428b-164">Requirements</span></span>



| <span data-ttu-id="c428b-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="c428b-165">Requirement</span></span> | <span data-ttu-id="c428b-166">Valore</span><span class="sxs-lookup"><span data-stu-id="c428b-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c428b-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c428b-167">Minimum supported client</span></span><br/> | <span data-ttu-id="c428b-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c428b-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c428b-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c428b-169">Minimum supported server</span></span><br/> | <span data-ttu-id="c428b-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c428b-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c428b-171">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c428b-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="c428b-172"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c428b-172"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c428b-173">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c428b-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="c428b-174"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c428b-174"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c428b-175">DLL</span><span class="sxs-lookup"><span data-stu-id="c428b-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c428b-176"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c428b-176"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c428b-177">CLSID</span><span class="sxs-lookup"><span data-stu-id="c428b-177">CLSID</span></span><br/>                    | <span data-ttu-id="c428b-178">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="c428b-178">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="c428b-179">IID</span><span class="sxs-lookup"><span data-stu-id="c428b-179">IID</span></span><br/>                      | <span data-ttu-id="c428b-180">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="c428b-180">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="c428b-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c428b-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c428b-182">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="c428b-182">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="c428b-183">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="c428b-183">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

