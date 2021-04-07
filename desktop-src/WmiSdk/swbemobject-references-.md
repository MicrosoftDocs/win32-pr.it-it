---
description: Il metodo References \_ dell'oggetto SWbemObject restituisce una raccolta di tutte le classi di associazione o di istanze che fanno riferimento all'oggetto corrente.
ms.assetid: ba02da47-0bb2-40e1-af50-1c42b4be2abd
ms.tgt_platform: multiple
title: Metodo SWbemObject.References_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.References_
- ISWbemObject.References_
- ISWbemObject.References_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3349ff104a5f0730ee99735a230d265fffd1333f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885230"
---
# <a name="swbemobjectreferences_-method"></a><span data-ttu-id="5b0fd-103">Metodo SWbemObject. References \_</span><span class="sxs-lookup"><span data-stu-id="5b0fd-103">SWbemObject.References\_ method</span></span>

<span data-ttu-id="5b0fd-104">Il **metodo \_ References** dell'oggetto [**SWbemObject**](swbemobject.md) restituisce una raccolta di tutte le classi di associazione o di istanze che fanno riferimento all'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-104">The **References\_** method of the [**SWbemObject**](swbemobject.md) object returns a collection of all association classes or instances that refer to the current object.</span></span>

<span data-ttu-id="5b0fd-105">Questo metodo esegue la stessa funzione dei [riferimenti della](references-of-statement.md) query WQL.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-105">This method performs the same function as the [REFERENCES OF](references-of-statement.md) WQL query.</span></span>

<span data-ttu-id="5b0fd-106">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5b0fd-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b0fd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b0fd-107">Syntax</span></span>


```VB
objWbemObjectSet = .References_( _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5b0fd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b0fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b0fd-109">*strResultClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5b0fd-109">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0fd-110">Stringa che contiene un nome di classe.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-110">String that contains a class name.</span></span> <span data-ttu-id="5b0fd-111">Se specificato, questo parametro indica che gli oggetti di associazione restituiti devono appartenere o essere derivati dalla classe specificata in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-111">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5b0fd-112">*strRole* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5b0fd-112">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0fd-113">Stringa che contiene un nome di proprietà.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-113">String that contains a property name.</span></span> <span data-ttu-id="5b0fd-114">Se specificato, questo parametro indica che gli oggetti di associazione restituiti devono essere limitati a quelli in cui l'oggetto di origine gioca un ruolo specifico.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-114">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="5b0fd-115">Il ruolo è definito dal nome di una proprietà specificata (che deve essere una proprietà di riferimento) di un'associazione.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-115">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="5b0fd-116">*bClassesOnly* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5b0fd-116">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0fd-117">Valore booleano che indica se deve essere restituito un elenco di nomi di classe anziché le istanze effettive delle classi.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-117">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="5b0fd-118">Queste sono le classi a cui appartengono gli oggetti Association.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-118">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="5b0fd-119">Il valore predefinito per questo parametro è **false**.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-119">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="5b0fd-120">*bSchemaOnly* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5b0fd-120">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0fd-121">Valore booleano che indica se la query viene applicata o meno allo schema anziché ai dati.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-121">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="5b0fd-122">Il valore predefinito per questo parametro è **false**.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-122">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="5b0fd-123">Può essere impostato su **true** solo se l'oggetto su cui viene richiamato questo metodo è una classe.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-123">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="5b0fd-124">Se è impostato su **true**, il set di endpoint restituiti rappresenta le classi associate adeguatamente alla classe di origine nello schema.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-124">When set to **TRUE**, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="5b0fd-125">*strRequiredQualifier* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5b0fd-125">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0fd-126">Stringa che contiene un nome di qualificatore.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-126">String that contains a qualifier name.</span></span> <span data-ttu-id="5b0fd-127">Se specificato, questo parametro indica che gli oggetti Association restituiti devono includere il qualificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-127">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="5b0fd-128">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5b0fd-128">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0fd-129">Integer che specifica flag aggiuntivi per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-129">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="5b0fd-130">Il valore predefinito per questo parametro è **wbemFlagReturnImmediately**, che indica alla chiamata di restituire immediatamente invece di attendere il completamento della query.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-130">The default for this parameter is **wbemFlagReturnImmediately**, which directs the call to return immediately rather than wait until the query has completed.</span></span> <span data-ttu-id="5b0fd-131">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-131">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="5b0fd-132"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="5b0fd-132"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="5b0fd-133">Causa la restituzione di un enumeratore di sola trasmissione.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-133">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="5b0fd-134">Gli enumeratori di solo avanzamento sono in genere molto più veloci e utilizzano meno memoria rispetto agli enumeratori convenzionali, ma non consentono chiamate a [**SWbemObject \_ . Clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="5b0fd-134">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="5b0fd-135"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="5b0fd-135"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="5b0fd-136">Fa in modo che Strumentazione gestione Windows (WMI) mantenga i puntatori agli oggetti dell'enumerazione finché il client non rilascia l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-136">Causes Windows Management Instrumentation (WMI) to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="5b0fd-137"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="5b0fd-137"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="5b0fd-138">Causa la restituzione immediata della chiamata.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-138">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="5b0fd-139"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="5b0fd-139"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="5b0fd-140">Causa il blocco della chiamata fino al completamento della query.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-140">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="5b0fd-141"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="5b0fd-141"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="5b0fd-142">Causa la restituzione dei dati di modifica della classe da parte di WMI con la definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-142">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="5b0fd-143">Per ulteriori informazioni sui qualificatori modificati, vedere [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="5b0fd-143">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5b0fd-144">*objwbemNamedValueSet* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5b0fd-144">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0fd-145">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-145">Typically, this is undefined.</span></span> <span data-ttu-id="5b0fd-146">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-146">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="5b0fd-147">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-147">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b0fd-148">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b0fd-148">Return value</span></span>

<span data-ttu-id="5b0fd-149">Se la chiamata ha esito positivo, viene restituito un oggetto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="5b0fd-149">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5b0fd-150">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="5b0fd-150">Error codes</span></span>

<span data-ttu-id="5b0fd-151">Dopo il completamento del metodo **References \_** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-151">After the completion of the **References\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="5b0fd-152">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="5b0fd-152">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="5b0fd-153">L'utente corrente non dispone delle autorizzazioni necessarie per visualizzare una o più classi restituite dalla chiamata.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-153">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="5b0fd-154">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="5b0fd-154">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="5b0fd-155">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-155">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="5b0fd-156">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="5b0fd-156">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="5b0fd-157">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-157">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="5b0fd-158">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="5b0fd-158">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="5b0fd-159">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-159">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b0fd-160">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b0fd-160">Remarks</span></span>

<span data-ttu-id="5b0fd-161">Per ulteriori informazioni sui riferimenti della query WQL associata, delle istanze di origine e degli oggetti di associazione, vedere associazioners [of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="5b0fd-161">For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b0fd-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b0fd-162">Requirements</span></span>



| <span data-ttu-id="5b0fd-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b0fd-163">Requirement</span></span> | <span data-ttu-id="5b0fd-164">Valore</span><span class="sxs-lookup"><span data-stu-id="5b0fd-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b0fd-165">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b0fd-165">Minimum supported client</span></span><br/> | <span data-ttu-id="5b0fd-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b0fd-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5b0fd-167">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b0fd-167">Minimum supported server</span></span><br/> | <span data-ttu-id="5b0fd-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b0fd-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5b0fd-169">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b0fd-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b0fd-170"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b0fd-170"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b0fd-171">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="5b0fd-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="5b0fd-172"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5b0fd-172"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5b0fd-173">DLL</span><span class="sxs-lookup"><span data-stu-id="5b0fd-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b0fd-174"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b0fd-174"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5b0fd-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="5b0fd-175">CLSID</span></span><br/>                    | <span data-ttu-id="5b0fd-176">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="5b0fd-176">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="5b0fd-177">IID</span><span class="sxs-lookup"><span data-stu-id="5b0fd-177">IID</span></span><br/>                      | <span data-ttu-id="5b0fd-178">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="5b0fd-178">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="5b0fd-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b0fd-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b0fd-180">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="5b0fd-180">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="5b0fd-181">**SWbemObject. Associator\_**</span><span class="sxs-lookup"><span data-stu-id="5b0fd-181">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="5b0fd-182">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="5b0fd-182">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="5b0fd-183">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="5b0fd-183">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




