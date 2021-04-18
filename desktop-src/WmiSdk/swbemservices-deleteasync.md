---
description: Elimina la classe o l'istanza specificata nel percorso dell'oggetto.
ms.assetid: f5ed170e-d002-4dd9-b8b6-b764a7a41a27
ms.tgt_platform: multiple
title: Metodo SWbemServices. DeleteAsync (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: adc8811c11f67b9fc92628740bd15df2086948d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309781"
---
# <a name="swbemservicesdeleteasync-method"></a><span data-ttu-id="d2f55-103">SWbemServices. DeleteAsync, metodo</span><span class="sxs-lookup"><span data-stu-id="d2f55-103">SWbemServices.DeleteAsync method</span></span>

<span data-ttu-id="d2f55-104">Il metodo **DeleteAsync** dell'oggetto [**SWbemServices**](swbemservices.md) Elimina la classe o l'istanza specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d2f55-104">The **DeleteAsync** method of the [**SWbemServices**](swbemservices.md) object deletes the class or instance specified in the object path.</span></span> <span data-ttu-id="d2f55-105">La chiamata a **DeleteAsync** restituisce immediatamente un risultato e i risultati e lo stato vengono restituiti al chiamante tramite gli eventi recapitati al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="d2f55-105">The call to **DeleteAsync** returns immediately and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="d2f55-106">Per ulteriori informazioni sulla creazione di un sink, vedere [ricezione di un evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="d2f55-106">For more information about creating a sink, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span> <span data-ttu-id="d2f55-107">È possibile eliminare solo gli oggetti nello spazio dei nomi a cui si è connessi.</span><span class="sxs-lookup"><span data-stu-id="d2f55-107">You can only delete objects in the namespace to which you are connected.</span></span>

<span data-ttu-id="d2f55-108">Se un provider dinamico fornisce la classe o l'istanza, a volte non è possibile eliminare questo oggetto a meno che il provider non supporti l'eliminazione di classi o istanze.</span><span class="sxs-lookup"><span data-stu-id="d2f55-108">If a dynamic provider supplies the class or instance, sometimes it is not possible to delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="d2f55-109">Il metodo viene chiamato in modalità asincrona.</span><span class="sxs-lookup"><span data-stu-id="d2f55-109">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="d2f55-110">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="d2f55-110">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="d2f55-111">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d2f55-111">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d2f55-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2f55-112">Syntax</span></span>


```VB
SWbemServices.DeleteAsync( _
  [ ByVal ObjWbemSink ], _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d2f55-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2f55-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2f55-114">*ObjWbemSink* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d2f55-114">*ObjWbemSink* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2f55-115">Sink di oggetto che riceve i risultati dell'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="d2f55-115">Object sink that receives the results of the deletion.</span></span> <span data-ttu-id="d2f55-116">Creare un oggetto [**SWbemSink**](swbemsink.md) per ricevere gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="d2f55-116">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="d2f55-117">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="d2f55-117">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="d2f55-118">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d2f55-118">Required.</span></span> <span data-ttu-id="d2f55-119">Stringa che contiene il percorso dell'oggetto che si desidera eliminare.</span><span class="sxs-lookup"><span data-stu-id="d2f55-119">String that contains the object path to the object that you want to delete.</span></span> <span data-ttu-id="d2f55-120">Per ulteriori informazioni, vedere [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="d2f55-120">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2f55-121">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d2f55-121">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2f55-122">Determina se vengono restituiti gli aggiornamenti di stato.</span><span class="sxs-lookup"><span data-stu-id="d2f55-122">Determines if status updates are returned.</span></span> <span data-ttu-id="d2f55-123">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d2f55-123">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="d2f55-124"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="d2f55-124"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="d2f55-125">Fa in modo che le chiamate asincrone inviino gli aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d2f55-125">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="d2f55-126"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="d2f55-126"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d2f55-127">Impedisce alle chiamate asincrone di inviare aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d2f55-127">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d2f55-128">*objWbemNamedValueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d2f55-128">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2f55-129">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="d2f55-129">Typically, this is undefined.</span></span> <span data-ttu-id="d2f55-130">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="d2f55-130">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="d2f55-131">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="d2f55-131">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="d2f55-132">*objWbemAsyncContext* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d2f55-132">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2f55-133">Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink di oggetto per identificare l'origine della chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="d2f55-133">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="d2f55-134">Utilizzare questo parametro se si eseguono più chiamate asincrone utilizzando lo stesso sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="d2f55-134">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="d2f55-135">Per usare questo parametro, creare un oggetto **SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona che si sta effettuando.</span><span class="sxs-lookup"><span data-stu-id="d2f55-135">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="d2f55-136">Questo oggetto **SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta tramite il metodo [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="d2f55-136">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="d2f55-137">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="d2f55-137">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2f55-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2f55-138">Return value</span></span>

<span data-ttu-id="d2f55-139">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d2f55-139">This method does not return a value.</span></span> <span data-ttu-id="d2f55-140">Se la chiamata ha esito positivo, il sink di oggetto riceve la notifica dell'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="d2f55-140">If the call is successful, the object sink receives notification of the deletion.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d2f55-141">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d2f55-141">Error codes</span></span>

<span data-ttu-id="d2f55-142">Dopo il completamento del metodo **DeleteAsync** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="d2f55-142">After the completion of the **DeleteAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d2f55-143">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d2f55-143">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d2f55-144">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="d2f55-144">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d2f55-145">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d2f55-145">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d2f55-146">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="d2f55-146">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="d2f55-147">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d2f55-147">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d2f55-148">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d2f55-148">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d2f55-149">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="d2f55-149">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="d2f55-150">Si è verificato un errore di rete, che impedisce il normale funzionamento.</span><span class="sxs-lookup"><span data-stu-id="d2f55-150">Networking error occurred, preventing normal operation.</span></span>

</dd> <dt>

<span data-ttu-id="d2f55-151">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="d2f55-151">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="d2f55-152">Il nome utente o la password corrente o specificata non sono validi o sono autorizzati a eseguire la connessione.</span><span class="sxs-lookup"><span data-stu-id="d2f55-152">Current or specified user name and password are not valid or authorized to make the connection.</span></span>

</dd> <dt>

<span data-ttu-id="d2f55-153">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="d2f55-153">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="d2f55-154">L'elemento richiesto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="d2f55-154">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2f55-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2f55-155">Remarks</span></span>

<span data-ttu-id="d2f55-156">Questa chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="d2f55-156">This call returns immediately.</span></span> <span data-ttu-id="d2f55-157">Lo stato dell'operazione di eliminazione viene restituito al chiamante tramite un callback recapitato al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="d2f55-157">The status of the delete operation is returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="d2f55-158">È possibile eseguire l'elaborazione finale nell'implementazione di *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="d2f55-158">You can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="d2f55-159">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="d2f55-159">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="d2f55-160">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d2f55-160">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="d2f55-161">Per eliminare i rischi, vedere [impostazione della sicurezza per una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="d2f55-161">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2f55-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2f55-162">Requirements</span></span>



| <span data-ttu-id="d2f55-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2f55-163">Requirement</span></span> | <span data-ttu-id="d2f55-164">Valore</span><span class="sxs-lookup"><span data-stu-id="d2f55-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2f55-165">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2f55-165">Minimum supported client</span></span><br/> | <span data-ttu-id="d2f55-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2f55-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d2f55-167">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2f55-167">Minimum supported server</span></span><br/> | <span data-ttu-id="d2f55-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2f55-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d2f55-169">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2f55-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2f55-170"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2f55-170"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2f55-171">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d2f55-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="d2f55-172"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d2f55-172"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d2f55-173">DLL</span><span class="sxs-lookup"><span data-stu-id="d2f55-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2f55-174"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2f55-174"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d2f55-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="d2f55-175">CLSID</span></span><br/>                    | <span data-ttu-id="d2f55-176">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="d2f55-176">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="d2f55-177">IID</span><span class="sxs-lookup"><span data-stu-id="d2f55-177">IID</span></span><br/>                      | <span data-ttu-id="d2f55-178">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="d2f55-178">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="d2f55-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2f55-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2f55-180">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="d2f55-180">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="d2f55-181">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="d2f55-181">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> </dl>

 

