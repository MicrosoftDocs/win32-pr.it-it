---
description: Il \_ metodo delle sottoclassi dell'oggetto SWbemObject restituisce un oggetto SWbemObjectSet.
ms.assetid: c17e5d4a-016f-42ae-bc11-e21a44772ce5
ms.tgt_platform: multiple
title: Metodo SWbemObject.Subclasses_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Subclasses_
- ISWbemObject.Subclasses_
- ISWbemObject.Subclasses_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: efae27b26235cbf1c298c7b45de69e1cf49c8570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309813"
---
# <a name="swbemobjectsubclasses_-method"></a><span data-ttu-id="e5a7e-103">SWbemObject. subclasss ( \_ metodo)</span><span class="sxs-lookup"><span data-stu-id="e5a7e-103">SWbemObject.Subclasses\_ method</span></span>

<span data-ttu-id="e5a7e-104">Il metodo delle **sottoclassi \_** dell'oggetto [**SWbemObject**](swbemobject.md) restituisce un oggetto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="e5a7e-104">The **Subclasses\_** method of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="e5a7e-105">Questo oggetto è una raccolta di sottoclassi dell'oggetto corrente, che deve essere una classe.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-105">This object is a collection of subclasses of the current object, which must be a class.</span></span> <span data-ttu-id="e5a7e-106">Gli elementi nella raccolta restituita possono essere ottenuti utilizzando metodi di raccolta standard.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-106">Items in the returned collection can be obtained using standard collection methods.</span></span> <span data-ttu-id="e5a7e-107">Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="e5a7e-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="e5a7e-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e5a7e-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e5a7e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5a7e-109">Syntax</span></span>


```VB
objWbemObjectSet = .Subclasses_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e5a7e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5a7e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5a7e-111">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e5a7e-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e5a7e-112">Integer che determina il modo in cui la chiamata esegue l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-112">Integer that determines how detailed the call enumerates.</span></span> <span data-ttu-id="e5a7e-113">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="e5a7e-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="e5a7e-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="e5a7e-115">Forza l'enumerazione ricorsiva in tutte le sottoclassi derivate dalla classe padre specificata.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-115">Forces recursive enumeration into all subclasses derived from the specified parent class.</span></span> <span data-ttu-id="e5a7e-116">La classe padre non viene restituita nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-116">The parent class itself is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="e5a7e-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="e5a7e-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="e5a7e-118">Valore predefinito per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-118">Default value for this parameter.</span></span> <span data-ttu-id="e5a7e-119">Impone all'enumerazione di includere solo le sottoclassi immediate della classe padre specificata.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-119">It forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="e5a7e-120"><span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>WbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="e5a7e-120"><span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*WbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="e5a7e-121">Causa la restituzione immediata della chiamata</span><span class="sxs-lookup"><span data-stu-id="e5a7e-121">Causes the call to return immediately</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="e5a7e-122"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="e5a7e-122"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="e5a7e-123">Causa il blocco della chiamata fino al completamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-123">Causes this call to block until the call has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="e5a7e-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="e5a7e-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="e5a7e-125">Fa in modo che WMI restituisca i dati di modifica della classe insieme alla definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-125">Causes WMI to return class amendment data along with the base class definition.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e5a7e-126">*objwbemNamedValueSet* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e5a7e-126">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e5a7e-127">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-127">Typically, this is undefined.</span></span> <span data-ttu-id="e5a7e-128">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-128">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="e5a7e-129">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-129">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5a7e-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5a7e-130">Return value</span></span>

<span data-ttu-id="e5a7e-131">Se la chiamata ha esito positivo, viene restituito un oggetto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="e5a7e-131">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e5a7e-132">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="e5a7e-132">Error codes</span></span>

<span data-ttu-id="e5a7e-133">Dopo il completamento del metodo delle **sottoclassi \_** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-133">After the completion of the **Subclasses\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="e5a7e-134">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="e5a7e-134">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="e5a7e-135">L'utente corrente non dispone delle autorizzazioni necessarie per visualizzare una o più classi restituite dalla chiamata.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-135">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="e5a7e-136">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="e5a7e-136">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="e5a7e-137">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-137">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="e5a7e-138">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="e5a7e-138">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="e5a7e-139">La classe specificata non esiste.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-139">Specified class did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="e5a7e-140">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="e5a7e-140">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="e5a7e-141">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-141">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="e5a7e-142">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="e5a7e-142">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="e5a7e-143">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-143">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5a7e-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5a7e-144">Remarks</span></span>

<span data-ttu-id="e5a7e-145">Non è un errore per la raccolta restituita avere zero elementi se non sono presenti sottoclassi dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-145">It is not an error for the returned collection to have zero elements if there are no subclasses of the current object.</span></span> <span data-ttu-id="e5a7e-146">Il metodo delle **sottoclassi \_** funziona solo per gli oggetti classe.</span><span class="sxs-lookup"><span data-stu-id="e5a7e-146">The **Subclasses\_** method only works for class objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5a7e-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5a7e-147">Requirements</span></span>



| <span data-ttu-id="e5a7e-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5a7e-148">Requirement</span></span> | <span data-ttu-id="e5a7e-149">Valore</span><span class="sxs-lookup"><span data-stu-id="e5a7e-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5a7e-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5a7e-150">Minimum supported client</span></span><br/> | <span data-ttu-id="e5a7e-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5a7e-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e5a7e-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5a7e-152">Minimum supported server</span></span><br/> | <span data-ttu-id="e5a7e-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5a7e-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e5a7e-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5a7e-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5a7e-155"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5a7e-155"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5a7e-156">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e5a7e-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="e5a7e-157"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e5a7e-157"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e5a7e-158">DLL</span><span class="sxs-lookup"><span data-stu-id="e5a7e-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5a7e-159"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5a7e-159"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e5a7e-160">CLSID</span><span class="sxs-lookup"><span data-stu-id="e5a7e-160">CLSID</span></span><br/>                    | <span data-ttu-id="e5a7e-161">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="e5a7e-161">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="e5a7e-162">IID</span><span class="sxs-lookup"><span data-stu-id="e5a7e-162">IID</span></span><br/>                      | <span data-ttu-id="e5a7e-163">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="e5a7e-163">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="e5a7e-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5a7e-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5a7e-165">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="e5a7e-165">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="e5a7e-166">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="e5a7e-166">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




