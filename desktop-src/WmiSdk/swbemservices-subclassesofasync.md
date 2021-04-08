---
description: Restituisce una raccolta di sottoclassi per una classe specificata.
ms.assetid: a9d16ee9-992e-4ce5-9c03-0a2c9958588c
ms.tgt_platform: multiple
title: Metodo SWbemServices. SubclassesOfAsync (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.SubclassesOfAsync
- ISWbemServices.SubclassesOfAsync
- ISWbemServices.SubclassesOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d8d325c96ea1a292d8ac3afc76bfea619fe5a143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967849"
---
# <a name="swbemservicessubclassesofasync-method"></a><span data-ttu-id="614e2-103">SWbemServices. SubclassesOfAsync, metodo</span><span class="sxs-lookup"><span data-stu-id="614e2-103">SWbemServices.SubclassesOfAsync method</span></span>

<span data-ttu-id="614e2-104">Il metodo **SubclassesOfAsync** dell'oggetto [**SWbemServices**](swbemservices.md) restituisce una raccolta di sottoclassi per una classe specificata.</span><span class="sxs-lookup"><span data-stu-id="614e2-104">The **SubclassesOfAsync** method of the [**SWbemServices**](swbemservices.md) object returns a collection of subclasses for a specified class.</span></span> <span data-ttu-id="614e2-105">Usare questo metodo solo per gli oggetti classe.</span><span class="sxs-lookup"><span data-stu-id="614e2-105">Only use this method for class objects.</span></span>

<span data-ttu-id="614e2-106">Questo metodo viene chiamato in modalità asincrona.</span><span class="sxs-lookup"><span data-stu-id="614e2-106">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="614e2-107">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="614e2-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="614e2-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="614e2-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="614e2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="614e2-109">Syntax</span></span>


```VB
SWbemServices.SubclassesOfAsync( _
  ByVal ObjWbemSink, _
  [ ByVal strSuperclass ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="614e2-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="614e2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="614e2-111">*ObjWbemSink*</span><span class="sxs-lookup"><span data-stu-id="614e2-111">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="614e2-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="614e2-112">Required.</span></span> <span data-ttu-id="614e2-113">Sink di oggetto che riceve le sottoclassi in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="614e2-113">Object sink that receives the subclasses asynchronously.</span></span> <span data-ttu-id="614e2-114">Creare un oggetto [**SWbemSink**](swbemsink.md) per ricevere gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="614e2-114">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="614e2-115">*strSuperclass* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="614e2-115">*strSuperclass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="614e2-116">Specifica un nome di classe padre.</span><span class="sxs-lookup"><span data-stu-id="614e2-116">Specifies a parent class name.</span></span> <span data-ttu-id="614e2-117">Nell'enumeratore vengono restituite solo le classi sottoclassi di questa classe.</span><span class="sxs-lookup"><span data-stu-id="614e2-117">Only the classes that are subclasses of this class are returned in the enumerator.</span></span> <span data-ttu-id="614e2-118">Se questo parametro è vuoto e se *iFlags* è **wbemQueryFlagShallow**, vengono restituite solo le classi di livello superiore, ovvero le classi prive di classe padre.</span><span class="sxs-lookup"><span data-stu-id="614e2-118">If this parameter is blank, and if *iFlags* is **wbemQueryFlagShallow**, only the top-level classes are returned (that is, classes that have no parent class).</span></span> <span data-ttu-id="614e2-119">Se questo parametro è vuoto e se *iFlags* è **wbemQueryFlagDeep**, vengono restituite tutte le classi all'interno dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="614e2-119">If this parameter is blank, and if *iFlags* is **wbemQueryFlagDeep**, all classes within the namespace are returned.</span></span>

</dd> <dt>

<span data-ttu-id="614e2-120">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="614e2-120">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="614e2-121">Determina la profondità dell'enumerazione della chiamata.</span><span class="sxs-lookup"><span data-stu-id="614e2-121">Determines the depth of the call enumeration.</span></span> <span data-ttu-id="614e2-122">Il valore predefinito per questo parametro è **wbemQueryFlagDeep**.</span><span class="sxs-lookup"><span data-stu-id="614e2-122">The default value for this parameter is **wbemQueryFlagDeep**.</span></span> <span data-ttu-id="614e2-123">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="614e2-123">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="614e2-124"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="614e2-124"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="614e2-125">Impone all'enumerazione di includere solo le sottoclassi immediate della classe padre specificata.</span><span class="sxs-lookup"><span data-stu-id="614e2-125">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="614e2-126"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="614e2-126"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="614e2-127">Valore predefinito per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="614e2-127">Default for this parameter.</span></span> <span data-ttu-id="614e2-128">Questo valore forza l'enumerazione ricorsiva in tutte le sottoclassi derivate dalla classe padre specificata.</span><span class="sxs-lookup"><span data-stu-id="614e2-128">This value forces recursive enumeration into all subclasses that are derived from the specified parent class.</span></span> <span data-ttu-id="614e2-129">La classe padre non viene restituita nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="614e2-129">The parent class is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="614e2-130"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="614e2-130"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="614e2-131">Fa in modo che le chiamate asincrone inviino gli aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="614e2-131">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="614e2-132"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="614e2-132"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="614e2-133">Impedisce alle chiamate asincrone di inviare aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="614e2-133">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="614e2-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="614e2-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="614e2-135">Causa la restituzione dei dati di modifica della classe da parte di WMI con la definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="614e2-135">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="614e2-136">Per ulteriori informazioni, vedere la pagina relativa alla [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="614e2-136">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="614e2-137">*objwbemNamedValueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="614e2-137">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="614e2-138">In genere, questo parametro non è definito.</span><span class="sxs-lookup"><span data-stu-id="614e2-138">Typically, this parameter is undefined.</span></span> <span data-ttu-id="614e2-139">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="614e2-139">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="614e2-140">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="614e2-140">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="614e2-141">*objWbemAsyncContext* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="614e2-141">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="614e2-142">Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink di oggetto per identificare l'origine della chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="614e2-142">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="614e2-143">Utilizzare questo parametro per effettuare più chiamate asincrone utilizzando lo stesso sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="614e2-143">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="614e2-144">Per usare questo parametro, creare un oggetto **SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona che si sta effettuando.</span><span class="sxs-lookup"><span data-stu-id="614e2-144">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="614e2-145">Questo oggetto **SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta tramite il metodo [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="614e2-145">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="614e2-146">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="614e2-146">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="614e2-147">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="614e2-147">Return value</span></span>

<span data-ttu-id="614e2-148">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="614e2-148">This method does not return a value.</span></span> <span data-ttu-id="614e2-149">In caso di esito positivo, il sink riceve un evento [**OnObjectReady**](swbemsink-onobjectready.md) per ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="614e2-149">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="614e2-150">Dopo l'ultima istanza, il sink di oggetto riceve un evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="614e2-150">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="614e2-151">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="614e2-151">Error codes</span></span>

<span data-ttu-id="614e2-152">Dopo il completamento del metodo **SubclassesOfAsync** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="614e2-152">After the completion of the **SubclassesOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="614e2-153">Una raccolta restituita con zero elementi non è un errore.</span><span class="sxs-lookup"><span data-stu-id="614e2-153">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="614e2-154">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="614e2-154">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="614e2-155">L'utente corrente non dispone dell'autorizzazione per visualizzare una o più classi restituite dalla chiamata.</span><span class="sxs-lookup"><span data-stu-id="614e2-155">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="614e2-156">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="614e2-156">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="614e2-157">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="614e2-157">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="614e2-158">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="614e2-158">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="614e2-159">La classe specificata non esiste.</span><span class="sxs-lookup"><span data-stu-id="614e2-159">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="614e2-160">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="614e2-160">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="614e2-161">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="614e2-161">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="614e2-162">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="614e2-162">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="614e2-163">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="614e2-163">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="614e2-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="614e2-164">Remarks</span></span>

<span data-ttu-id="614e2-165">Questa chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="614e2-165">This call returns immediately.</span></span> <span data-ttu-id="614e2-166">Gli oggetti e lo stato richiesti vengono restituiti al chiamante tramite callback recapitati al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="614e2-166">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="614e2-167">Per elaborare ogni oggetto all'arrivo, creare un *objWbemSink*. Subroutine dell'evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="614e2-167">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="614e2-168">Dopo la restituzione di tutti gli oggetti, è possibile eseguire l'elaborazione finale nell'implementazione di *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="614e2-168">After all the objects are returned, you can perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="614e2-169">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="614e2-169">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="614e2-170">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="614e2-170">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="614e2-171">Per eliminare i rischi, vedere [impostazione della sicurezza per una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="614e2-171">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="614e2-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="614e2-172">Requirements</span></span>



| <span data-ttu-id="614e2-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="614e2-173">Requirement</span></span> | <span data-ttu-id="614e2-174">Valore</span><span class="sxs-lookup"><span data-stu-id="614e2-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="614e2-175">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="614e2-175">Minimum supported client</span></span><br/> | <span data-ttu-id="614e2-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="614e2-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="614e2-177">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="614e2-177">Minimum supported server</span></span><br/> | <span data-ttu-id="614e2-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="614e2-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="614e2-179">Intestazione</span><span class="sxs-lookup"><span data-stu-id="614e2-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="614e2-180"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="614e2-180"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="614e2-181">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="614e2-181">Type library</span></span><br/>             | <dl> <span data-ttu-id="614e2-182"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="614e2-182"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="614e2-183">DLL</span><span class="sxs-lookup"><span data-stu-id="614e2-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="614e2-184"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="614e2-184"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="614e2-185">CLSID</span><span class="sxs-lookup"><span data-stu-id="614e2-185">CLSID</span></span><br/>                    | <span data-ttu-id="614e2-186">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="614e2-186">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="614e2-187">IID</span><span class="sxs-lookup"><span data-stu-id="614e2-187">IID</span></span><br/>                      | <span data-ttu-id="614e2-188">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="614e2-188">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="614e2-189">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="614e2-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="614e2-190">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="614e2-190">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="614e2-191">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="614e2-191">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

