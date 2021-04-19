---
description: Il metodo instances \_ dell'oggetto SWbemObject crea un enumeratore che restituisce le istanze dell'oggetto classe corrente. Questo metodo implementa una semplice query. Query più complesse possono richiedere l'uso di SWbemServices.ExecQuery.
ms.assetid: 30402d7d-f7cb-43b5-96b5-a8a76144e32d
ms.tgt_platform: multiple
title: Metodo SWbemObject.Instances_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Instances_
- ISWbemObject.Instances_
- ISWbemObject.Instances_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c573c1e94cd473d22483c7b6a2c801c3e6bcb9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318173"
---
# <a name="swbemobjectinstances_-method"></a><span data-ttu-id="c5e7f-105">Metodo SWbemObject. instances \_</span><span class="sxs-lookup"><span data-stu-id="c5e7f-105">SWbemObject.Instances\_ method</span></span>

<span data-ttu-id="c5e7f-106">Il **metodo \_ instances** dell'oggetto [**SWbemObject**](swbemobject.md) crea un enumeratore che restituisce le istanze dell'oggetto classe corrente.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-106">The **Instances\_** method of the [**SWbemObject**](swbemobject.md) object creates an enumerator that returns the instances of the current class object.</span></span> <span data-ttu-id="c5e7f-107">Questo metodo implementa una semplice query.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-107">This method implements a simple query.</span></span> <span data-ttu-id="c5e7f-108">Query più complesse possono richiedere l'uso di [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="c5e7f-108">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="c5e7f-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c5e7f-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c5e7f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5e7f-110">Syntax</span></span>


```VB
objWbemObjectSet = .Instances_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c5e7f-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5e7f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5e7f-112">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c5e7f-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c5e7f-113">Integer che determina il comportamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-113">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="c5e7f-114">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-114">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="c5e7f-115"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="c5e7f-115"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="c5e7f-116">Causa la restituzione di un enumeratore di sola trasmissione.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-116">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="c5e7f-117">Gli enumeratori di solo avanzamento sono in genere molto più veloci e utilizzano meno memoria rispetto agli enumeratori convenzionali, ma non consentono chiamate a [**SWbemObject \_ . Clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="c5e7f-117">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="c5e7f-118"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="c5e7f-118"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c5e7f-119">Causa la conservazione dei puntatori agli oggetti dell'enumerazione da parte di WMI finché il client non rilascia l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-119">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="c5e7f-120"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="c5e7f-120"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="c5e7f-121">Valore predefinito per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-121">Default value for this parameter.</span></span> <span data-ttu-id="c5e7f-122">Questo flag causa la restituzione immediata della chiamata.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-122">This flag causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="c5e7f-123"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="c5e7f-123"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* ( 0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c5e7f-124">Causa il blocco della chiamata fino al completamento della query.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-124">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="c5e7f-125"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="c5e7f-125"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="c5e7f-126">Impone all'enumerazione di includere solo le sottoclassi immediate della classe padre specificata.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-126">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="c5e7f-127"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="c5e7f-127"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c5e7f-128">Valore predefinito per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-128">Default for this parameter.</span></span> <span data-ttu-id="c5e7f-129">Questo valore impone all'enumerazione di includere tutte le classi nella gerarchia.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-129">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="c5e7f-130"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="c5e7f-130"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="c5e7f-131">Causa la restituzione dei dati di modifica della classe da parte di WMI con la definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-131">Causes WMI to return class amendment data with the base class definition.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c5e7f-132">*objwbemNamedValueSet* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c5e7f-132">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c5e7f-133">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-133">Typically, this is undefined.</span></span> <span data-ttu-id="c5e7f-134">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="c5e7f-135">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-135">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5e7f-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5e7f-136">Return value</span></span>

<span data-ttu-id="c5e7f-137">Se il metodo ha esito positivo, viene restituito un oggetto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="c5e7f-137">If the method is successful, an [**SWbemObjectSet**](swbemobjectset.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c5e7f-138">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c5e7f-138">Error codes</span></span>

<span data-ttu-id="c5e7f-139">Dopo il completamento del metodo **instances \_** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-139">After the completion of the **Instances\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="c5e7f-140">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="c5e7f-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="c5e7f-141">L'utente corrente non dispone delle autorizzazioni necessarie per visualizzare le istanze della classe specificata.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-141">Current user does not have permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="c5e7f-142">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="c5e7f-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c5e7f-143">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-143">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c5e7f-144">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="c5e7f-144">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="c5e7f-145">La classe specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-145">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c5e7f-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="c5e7f-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="c5e7f-147">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c5e7f-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="c5e7f-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="c5e7f-149">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5e7f-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5e7f-150">Remarks</span></span>

<span data-ttu-id="c5e7f-151">Il **metodo \_ instances** funziona solo per gli oggetti classe.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-151">The **Instances\_** method only works for class objects.</span></span> <span data-ttu-id="c5e7f-152">Non si tratta di un errore per la raccolta restituita con zero elementi.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-152">It is not an error for the returned collection to have zero elements.</span></span> <span data-ttu-id="c5e7f-153">Il comportamento predefinito per questo metodo è [*semisincrono*](gloss-s.md) a causa del valore *iFlags* predefinito **wbemFlagReturnImmediately**.</span><span class="sxs-lookup"><span data-stu-id="c5e7f-153">The default behavior for this method is [*semisynchronous*](gloss-s.md) because of the default *IFlags* value **wbemFlagReturnImmediately**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5e7f-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5e7f-154">Requirements</span></span>



| <span data-ttu-id="c5e7f-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5e7f-155">Requirement</span></span> | <span data-ttu-id="c5e7f-156">Valore</span><span class="sxs-lookup"><span data-stu-id="c5e7f-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5e7f-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5e7f-157">Minimum supported client</span></span><br/> | <span data-ttu-id="c5e7f-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5e7f-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c5e7f-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5e7f-159">Minimum supported server</span></span><br/> | <span data-ttu-id="c5e7f-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5e7f-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c5e7f-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5e7f-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5e7f-162"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5e7f-162"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5e7f-163">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c5e7f-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="c5e7f-164"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c5e7f-164"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c5e7f-165">DLL</span><span class="sxs-lookup"><span data-stu-id="c5e7f-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5e7f-166"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5e7f-166"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c5e7f-167">CLSID</span><span class="sxs-lookup"><span data-stu-id="c5e7f-167">CLSID</span></span><br/>                    | <span data-ttu-id="c5e7f-168">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="c5e7f-168">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="c5e7f-169">IID</span><span class="sxs-lookup"><span data-stu-id="c5e7f-169">IID</span></span><br/>                      | <span data-ttu-id="c5e7f-170">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="c5e7f-170">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="c5e7f-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5e7f-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5e7f-172">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="c5e7f-172">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="c5e7f-173">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="c5e7f-173">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




