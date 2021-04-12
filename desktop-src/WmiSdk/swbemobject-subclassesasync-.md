---
description: Il \_ Metodo SubclassesAsync di SWbemObject fornisce in modo asincrono le sottoclassi dell'oggetto corrente, che deve essere una classe.
ms.assetid: 14d4a609-3aa4-49bd-bea4-6a71bc24d9dd
ms.tgt_platform: multiple
title: Metodo SWbemObject.SubclassesAsync_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SubclassesAsync_
- ISWbemObject.SubclassesAsync_
- ISWbemObject.SubclassesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6e922953e9f25aae2e47ea572678790b1228a581
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233803"
---
# <a name="swbemobjectsubclassesasync_-method"></a><span data-ttu-id="45cea-103">SWbemObject. SubclassesAsync, \_ Metodo</span><span class="sxs-lookup"><span data-stu-id="45cea-103">SWbemObject.SubclassesAsync\_ method</span></span>

<span data-ttu-id="45cea-104">Il **metodo \_ SubclassesAsync** di [**SWbemObject**](swbemobject.md) fornisce in modo asincrono le sottoclassi dell'oggetto corrente, che deve essere una classe.</span><span class="sxs-lookup"><span data-stu-id="45cea-104">The **SubclassesAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously supplies the subclasses of the current object, which must be a class.</span></span>

<span data-ttu-id="45cea-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="45cea-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="45cea-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45cea-106">Syntax</span></span>


```VB
SWbemObject.SubclassesAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="45cea-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="45cea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45cea-108">*objWbemSink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45cea-108">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45cea-109">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="45cea-109">Required.</span></span> <span data-ttu-id="45cea-110">Sink di oggetto che riceve gli oggetti in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="45cea-110">Object sink that receives the objects asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="45cea-111">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="45cea-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="45cea-112">Determina la modalità di enumerazione della chiamata.</span><span class="sxs-lookup"><span data-stu-id="45cea-112">Determines how detailed the call enumerates.</span></span> <span data-ttu-id="45cea-113">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="45cea-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="45cea-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="45cea-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="45cea-115">Forza l'enumerazione ricorsiva in tutte le sottoclassi derivate dalla classe padre specificata.</span><span class="sxs-lookup"><span data-stu-id="45cea-115">Forces recursive enumeration into all subclasses derived from the specified parent class.</span></span> <span data-ttu-id="45cea-116">La classe padre non viene restituita nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="45cea-116">The parent class itself is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="45cea-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="45cea-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="45cea-118">Valore predefinito per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="45cea-118">Default for this parameter.</span></span> <span data-ttu-id="45cea-119">Impone all'enumerazione di includere solo le sottoclassi immediate della classe padre specificata.</span><span class="sxs-lookup"><span data-stu-id="45cea-119">It forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="45cea-120"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="45cea-120"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="45cea-121">Fa in modo che le chiamate asincrone inviino gli aggiornamenti di stato al gestore eventi [**SWbemSink. OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="45cea-121">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="45cea-122"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="45cea-122"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="45cea-123">Impedisce alle chiamate asincrone di inviare aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="45cea-123">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="45cea-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="45cea-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="45cea-125">Causa la restituzione dei dati di modifica della classe da parte di WMI con la definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="45cea-125">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="45cea-126">Per ulteriori informazioni sui qualificatori modificati, vedere [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="45cea-126">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="45cea-127">*objWbemNamedValueSet* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="45cea-127">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="45cea-128">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="45cea-128">Typically, this is undefined.</span></span> <span data-ttu-id="45cea-129">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="45cea-129">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="45cea-130">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="45cea-130">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="45cea-131">*objWbemAsyncContext* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="45cea-131">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="45cea-132">Si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink di oggetto per identificare l'origine della chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="45cea-132">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="45cea-133">Utilizzare questo parametro quando si effettuano più chiamate asincrone utilizzando lo stesso sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="45cea-133">Use this parameter when you make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="45cea-134">Per usare questo parametro, creare un oggetto **SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona che si sta effettuando.</span><span class="sxs-lookup"><span data-stu-id="45cea-134">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="45cea-135">Questo oggetto **SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta tramite il metodo [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="45cea-135">This **SWbemNamedValueSet** object is returned to the object sink, and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="45cea-136">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="45cea-136">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45cea-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45cea-137">Return value</span></span>

<span data-ttu-id="45cea-138">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="45cea-138">This method does not return a value.</span></span> <span data-ttu-id="45cea-139">In caso di esito positivo, il sink riceve un evento [**OnObjectReady**](swbemsink-onobjectready.md) per ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="45cea-139">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event for each instance.</span></span> <span data-ttu-id="45cea-140">Dopo l'ultima istanza, il sink di oggetto riceve un evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="45cea-140">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="45cea-141">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="45cea-141">Error codes</span></span>

<span data-ttu-id="45cea-142">Dopo il completamento del metodo **SubclassesAsync \_** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="45cea-142">After the completion of the **SubclassesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="45cea-143">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="45cea-143">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="45cea-144">L'utente corrente non dispone delle autorizzazioni necessarie per visualizzare una o più classi restituite dalla chiamata.</span><span class="sxs-lookup"><span data-stu-id="45cea-144">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="45cea-145">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="45cea-145">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="45cea-146">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="45cea-146">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="45cea-147">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="45cea-147">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="45cea-148">La classe specificata non esiste.</span><span class="sxs-lookup"><span data-stu-id="45cea-148">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="45cea-149">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="45cea-149">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="45cea-150">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="45cea-150">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="45cea-151">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="45cea-151">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="45cea-152">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="45cea-152">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45cea-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="45cea-153">Remarks</span></span>

<span data-ttu-id="45cea-154">Questa chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="45cea-154">This call returns immediately.</span></span> <span data-ttu-id="45cea-155">Gli oggetti e lo stato richiesti vengono restituiti al chiamante tramite callback recapitati al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="45cea-155">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="45cea-156">Per elaborare ogni oggetto all'arrivo, creare un *objWbemSink*. Subroutine dell'evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="45cea-156">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="45cea-157">Dopo la restituzione di tutti gli oggetti, è possibile eseguire l'elaborazione finale nell'implementazione di *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="45cea-157">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="45cea-158">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="45cea-158">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="45cea-159">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="45cea-159">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="45cea-160">Per eliminare i rischi, usare la comunicazione semisincrono o la comunicazione sincrona.</span><span class="sxs-lookup"><span data-stu-id="45cea-160">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="45cea-161">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="45cea-161">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="45cea-162">È consigliabile che gli script verifichino l'origine della chiamata usando un parametro *objWbemAsyncContext* .</span><span class="sxs-lookup"><span data-stu-id="45cea-162">It is recommended that scripts verify the source of the call by using an *objWbemAsyncContext* parameter.</span></span>

<span data-ttu-id="45cea-163">Non è un errore per la raccolta restituita avere zero elementi se non sono presenti sottoclassi dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="45cea-163">It is not an error for the returned collection to have zero elements if there are no subclasses of the current object.</span></span> <span data-ttu-id="45cea-164">Il **metodo \_ SubclassesAsync** funziona solo per gli oggetti classe.</span><span class="sxs-lookup"><span data-stu-id="45cea-164">The **SubclassesAsync\_** method only works for class objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="45cea-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45cea-165">Requirements</span></span>



| <span data-ttu-id="45cea-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="45cea-166">Requirement</span></span> | <span data-ttu-id="45cea-167">Valore</span><span class="sxs-lookup"><span data-stu-id="45cea-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45cea-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45cea-168">Minimum supported client</span></span><br/> | <span data-ttu-id="45cea-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45cea-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="45cea-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45cea-170">Minimum supported server</span></span><br/> | <span data-ttu-id="45cea-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45cea-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="45cea-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45cea-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="45cea-173"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="45cea-173"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="45cea-174">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="45cea-174">Type library</span></span><br/>             | <dl> <span data-ttu-id="45cea-175"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="45cea-175"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="45cea-176">DLL</span><span class="sxs-lookup"><span data-stu-id="45cea-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45cea-177"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45cea-177"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="45cea-178">CLSID</span><span class="sxs-lookup"><span data-stu-id="45cea-178">CLSID</span></span><br/>                    | <span data-ttu-id="45cea-179">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="45cea-179">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="45cea-180">IID</span><span class="sxs-lookup"><span data-stu-id="45cea-180">IID</span></span><br/>                      | <span data-ttu-id="45cea-181">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="45cea-181">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="45cea-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45cea-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45cea-183">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="45cea-183">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="45cea-184">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="45cea-184">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> <dt>

[<span data-ttu-id="45cea-185">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="45cea-185">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> </dl>

 

