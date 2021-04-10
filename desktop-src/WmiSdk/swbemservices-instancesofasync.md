---
description: Recupera le istanze di una classe specificata in base ai criteri specificati dall'utente.
ms.assetid: 631cd749-9a39-4606-9a38-0b4bb5b4b2cd
ms.tgt_platform: multiple
title: Metodo SWbemServices. InstancesOfAsync (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c518cb38a0ecb221f4fcb0d0e7f9ce6dfc226ba9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880402"
---
# <a name="swbemservicesinstancesofasync-method"></a><span data-ttu-id="d68d0-103">SWbemServices. InstancesOfAsync, metodo</span><span class="sxs-lookup"><span data-stu-id="d68d0-103">SWbemServices.InstancesOfAsync method</span></span>

<span data-ttu-id="d68d0-104">Il metodo **InstancesOfAsync** dell'oggetto [**SWbemServices**](swbemservices.md) recupera le istanze di una classe specificata in base ai criteri specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="d68d0-104">The **InstancesOfAsync** method of the [**SWbemServices**](swbemservices.md) object retrieves instances of a specified class according to user-specified criteria.</span></span>

<span data-ttu-id="d68d0-105">Il metodo viene chiamato in modalità asincrona.</span><span class="sxs-lookup"><span data-stu-id="d68d0-105">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="d68d0-106">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="d68d0-106">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="d68d0-107">Per la spiegazione della sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d68d0-107">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d68d0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d68d0-108">Syntax</span></span>


```VB
SWbemServices.InstancesOfAsync( _
  ByVal ObjWbemSink, _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d68d0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d68d0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d68d0-110">*ObjWbemSink*</span><span class="sxs-lookup"><span data-stu-id="d68d0-110">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="d68d0-111">Sink di oggetto che riceve le istanze in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="d68d0-111">Object sink that receives the instances asynchronously.</span></span> <span data-ttu-id="d68d0-112">Creare un oggetto [**SWbemSink**](swbemsink.md) per ricevere gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="d68d0-112">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="d68d0-113">*strClass*</span><span class="sxs-lookup"><span data-stu-id="d68d0-113">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="d68d0-114">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d68d0-114">Required.</span></span> <span data-ttu-id="d68d0-115">Stringa che contiene il nome della classe per le istanze desiderate.</span><span class="sxs-lookup"><span data-stu-id="d68d0-115">String that contains the name of the class for the instances that you want.</span></span> <span data-ttu-id="d68d0-116">Questo parametro non può essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="d68d0-116">This parameter cannot be blank.</span></span>

</dd> <dt>

<span data-ttu-id="d68d0-117">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d68d0-117">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d68d0-118">Determina la profondità dell'enumerazione delle chiamate e indica se la chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="d68d0-118">Determines the depth of the call enumeration, and whether or not the call returns immediately.</span></span> <span data-ttu-id="d68d0-119">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d68d0-119">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="d68d0-120"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="d68d0-120"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="d68d0-121">Impone all'enumerazione di includere solo le sottoclassi immediate della classe padre specificata.</span><span class="sxs-lookup"><span data-stu-id="d68d0-121">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="d68d0-122"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="d68d0-122"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d68d0-123">Valore predefinito per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d68d0-123">Default for this parameter.</span></span> <span data-ttu-id="d68d0-124">Questo valore impone all'enumerazione di includere tutte le classi nella gerarchia.</span><span class="sxs-lookup"><span data-stu-id="d68d0-124">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="d68d0-125"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="d68d0-125"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="d68d0-126">Fa in modo che le chiamate asincrone inviino gli aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d68d0-126">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="d68d0-127"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="d68d0-127"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d68d0-128">Impedisce alle chiamate asincrone di inviare aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d68d0-128">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="d68d0-129"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="d68d0-129"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="d68d0-130">Causa la restituzione dei dati di modifica della classe da parte di WMI con la definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="d68d0-130">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="d68d0-131">Per ulteriori informazioni, vedere la pagina relativa alla [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="d68d0-131">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d68d0-132">*objWbemNamedValueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d68d0-132">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d68d0-133">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="d68d0-133">Typically, this is undefined.</span></span> <span data-ttu-id="d68d0-134">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="d68d0-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="d68d0-135">Un provider che supporta o richiede informazioni sul contesto deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="d68d0-135">A provider that supports or requires context information information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="d68d0-136">*objWbemAsyncContext* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d68d0-136">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d68d0-137">Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink di oggetto per identificare l'origine della chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="d68d0-137">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="d68d0-138">Utilizzare questo parametro se si eseguono più chiamate asincrone utilizzando lo stesso sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="d68d0-138">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="d68d0-139">Per usare questo parametro, creare un oggetto **SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona che si sta effettuando.</span><span class="sxs-lookup"><span data-stu-id="d68d0-139">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="d68d0-140">Questo oggetto **SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta tramite il metodo [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="d68d0-140">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d68d0-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d68d0-141">Return value</span></span>

<span data-ttu-id="d68d0-142">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d68d0-142">This method does not return a value.</span></span> <span data-ttu-id="d68d0-143">In caso di esito positivo, il sink riceve un evento [**OnObjectReady**](swbemsink-onobjectready.md) per ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="d68d0-143">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="d68d0-144">Dopo l'ultima istanza, il sink di oggetto riceve un evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="d68d0-144">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d68d0-145">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d68d0-145">Error codes</span></span>

<span data-ttu-id="d68d0-146">Al termine del metodo **InstancesOfAsync** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="d68d0-146">Upon the completion of the **InstancesOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d68d0-147">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="d68d0-147">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="d68d0-148">L'utente corrente non dispone dell'autorizzazione per visualizzare le istanze della classe specificata.</span><span class="sxs-lookup"><span data-stu-id="d68d0-148">Current user does not have the permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="d68d0-149">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d68d0-149">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d68d0-150">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="d68d0-150">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d68d0-151">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="d68d0-151">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="d68d0-152">La classe specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="d68d0-152">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d68d0-153">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d68d0-153">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d68d0-154">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="d68d0-154">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d68d0-155">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d68d0-155">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d68d0-156">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d68d0-156">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d68d0-157">Commenti</span><span class="sxs-lookup"><span data-stu-id="d68d0-157">Remarks</span></span>

<span data-ttu-id="d68d0-158">Questa chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="d68d0-158">This call returns immediately.</span></span> <span data-ttu-id="d68d0-159">Gli oggetti e lo stato richiesti vengono restituiti al chiamante tramite callback recapitati al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="d68d0-159">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="d68d0-160">Per elaborare ogni oggetto quando restituisce, creare un *objWbemSink*. Subroutine dell'evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="d68d0-160">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="d68d0-161">Dopo la restituzione di tutti gli oggetti, è possibile eseguire l'elaborazione finale nell'implementazione di *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="d68d0-161">After all the objects are returned, you can perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="d68d0-162">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="d68d0-162">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="d68d0-163">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d68d0-163">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="d68d0-164">Per eliminare i rischi, vedere [impostazione della sicurezza per una chiamata asincrona](setting-security-on-an-asynchronous-call.md)</span><span class="sxs-lookup"><span data-stu-id="d68d0-164">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md)</span></span>

<span data-ttu-id="d68d0-165">Il metodo **InstancesOfAsync** funziona solo per gli oggetti classe.</span><span class="sxs-lookup"><span data-stu-id="d68d0-165">The **InstancesOfAsync** method only works for class objects.</span></span> <span data-ttu-id="d68d0-166">Non si tratta di un errore per l'enumeratore restituito con zero (0) elementi.</span><span class="sxs-lookup"><span data-stu-id="d68d0-166">It is not an error for the returned enumerator to have zero (0) elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="d68d0-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d68d0-167">Requirements</span></span>



| <span data-ttu-id="d68d0-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="d68d0-168">Requirement</span></span> | <span data-ttu-id="d68d0-169">Valore</span><span class="sxs-lookup"><span data-stu-id="d68d0-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d68d0-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d68d0-170">Minimum supported client</span></span><br/> | <span data-ttu-id="d68d0-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d68d0-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d68d0-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d68d0-172">Minimum supported server</span></span><br/> | <span data-ttu-id="d68d0-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d68d0-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d68d0-174">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d68d0-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="d68d0-175"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d68d0-175"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d68d0-176">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d68d0-176">Type library</span></span><br/>             | <dl> <span data-ttu-id="d68d0-177"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d68d0-177"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d68d0-178">DLL</span><span class="sxs-lookup"><span data-stu-id="d68d0-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d68d0-179"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d68d0-179"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d68d0-180">CLSID</span><span class="sxs-lookup"><span data-stu-id="d68d0-180">CLSID</span></span><br/>                    | <span data-ttu-id="d68d0-181">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="d68d0-181">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="d68d0-182">IID</span><span class="sxs-lookup"><span data-stu-id="d68d0-182">IID</span></span><br/>                      | <span data-ttu-id="d68d0-183">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="d68d0-183">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="d68d0-184">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d68d0-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d68d0-185">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="d68d0-185">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="d68d0-186">Chiamata a un metodo</span><span class="sxs-lookup"><span data-stu-id="d68d0-186">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

