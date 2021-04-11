---
description: Restituisce una raccolta di tutte le classi di associazione o di istanze che fanno riferimento a una classe di origine o a un'istanza specifica.
ms.assetid: 33425b1c-13f5-4c3d-8f8a-2922f3e95264
ms.tgt_platform: multiple
title: Metodo SWbemServices. ReferencesTo (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 73addea189815d1594d0963fbdd6e20c562b3be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131914"
---
# <a name="swbemservicesreferencesto-method"></a><span data-ttu-id="b2848-103">SWbemServices. ReferencesTo, metodo</span><span class="sxs-lookup"><span data-stu-id="b2848-103">SWbemServices.ReferencesTo method</span></span>

<span data-ttu-id="b2848-104">Il metodo **ReferencesTo** dell'oggetto [**SWbemServices**](swbemservices.md) restituisce una raccolta di tutte le classi di associazione o di istanze che fanno riferimento a una classe di origine o a un'istanza specifica.</span><span class="sxs-lookup"><span data-stu-id="b2848-104">The **ReferencesTo** method of the [**SWbemServices**](swbemservices.md) object returns a collection of all association classes or instances that refer to a specific source class or instance.</span></span> <span data-ttu-id="b2848-105">Questo metodo esegue la stessa funzione eseguita dai [riferimenti della](references-of-statement.md) query WQL.</span><span class="sxs-lookup"><span data-stu-id="b2848-105">This method performs the same function that the [REFERENCES OF](references-of-statement.md) WQL query performs.</span></span>

<span data-ttu-id="b2848-106">Questo metodo viene chiamato in modalità semisincrono.</span><span class="sxs-lookup"><span data-stu-id="b2848-106">This method is called in the semisynchronous mode.</span></span> <span data-ttu-id="b2848-107">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b2848-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="b2848-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b2848-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b2848-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2848-109">Syntax</span></span>


```VB
objWbemObjectSet = .ReferencesTo( _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b2848-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2848-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2848-111">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="b2848-111">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="b2848-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b2848-112">Required.</span></span> <span data-ttu-id="b2848-113">Stringa che contiene il percorso dell'oggetto dell'origine per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="b2848-113">String that contains the object path of the source for this method.</span></span> <span data-ttu-id="b2848-114">Per ulteriori informazioni, vedere [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="b2848-114">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2848-115">*strResultClass* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="b2848-115">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2848-116">Stringa che contiene un nome di classe.</span><span class="sxs-lookup"><span data-stu-id="b2848-116">String that contains a class name.</span></span> <span data-ttu-id="b2848-117">Se specificato, questo parametro indica che gli oggetti di associazione restituiti devono appartenere o essere derivati dalla classe specificata in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b2848-117">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class that is specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b2848-118">*strRole* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="b2848-118">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2848-119">Stringa che contiene un nome di proprietà.</span><span class="sxs-lookup"><span data-stu-id="b2848-119">String that contains a property name.</span></span> <span data-ttu-id="b2848-120">Se specificato, questo parametro indica che gli oggetti di associazione restituiti devono essere limitati a quelli in cui l'oggetto di origine gioca un ruolo specifico.</span><span class="sxs-lookup"><span data-stu-id="b2848-120">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="b2848-121">Il ruolo è definito dal nome di una proprietà specificata (che deve essere una proprietà di riferimento) di un'associazione.</span><span class="sxs-lookup"><span data-stu-id="b2848-121">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="b2848-122">*bClassesOnly* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="b2848-122">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2848-123">Valore booleano che indica se deve essere restituito un elenco di nomi di classe anziché le istanze effettive delle classi.</span><span class="sxs-lookup"><span data-stu-id="b2848-123">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="b2848-124">Queste sono le classi a cui appartengono gli oggetti Association.</span><span class="sxs-lookup"><span data-stu-id="b2848-124">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="b2848-125">Il valore predefinito per questo parametro è **false**.</span><span class="sxs-lookup"><span data-stu-id="b2848-125">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b2848-126">*bSchemaOnly* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="b2848-126">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2848-127">Valore booleano che indica se la query viene applicata o meno allo schema anziché ai dati.</span><span class="sxs-lookup"><span data-stu-id="b2848-127">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="b2848-128">Il valore predefinito per questo parametro è **false**.</span><span class="sxs-lookup"><span data-stu-id="b2848-128">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="b2848-129">Può essere impostato su **true** solo se il parametro *strObjectPath* specifica il percorso dell'oggetto di una classe.</span><span class="sxs-lookup"><span data-stu-id="b2848-129">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="b2848-130">Se è impostato su **true**, il set di endpoint restituiti rappresenta le classi associate adeguatamente alla classe di origine nello schema.</span><span class="sxs-lookup"><span data-stu-id="b2848-130">When set to **TRUE**, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="b2848-131">*strRequiredQualifier* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="b2848-131">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2848-132">Stringa che contiene un nome di qualificatore.</span><span class="sxs-lookup"><span data-stu-id="b2848-132">String that contains a qualifier name.</span></span> <span data-ttu-id="b2848-133">Se specificato, questo parametro indica che gli oggetti Association restituiti devono includere il qualificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="b2848-133">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="b2848-134">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="b2848-134">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2848-135">Integer che specifica flag aggiuntivi per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="b2848-135">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="b2848-136">Il valore predefinito per questo parametro è **wbemFlagReturnImmediately**, che indica alla chiamata di restituire immediatamente invece di attendere il completamento della query.</span><span class="sxs-lookup"><span data-stu-id="b2848-136">The default for this parameter is **wbemFlagReturnImmediately**, which directs the call to return immediately rather than wait until the query has completed.</span></span> <span data-ttu-id="b2848-137">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b2848-137">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="b2848-138"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="b2848-138"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="b2848-139">Causa la restituzione di un enumeratore di sola trasmissione.</span><span class="sxs-lookup"><span data-stu-id="b2848-139">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="b2848-140">Gli enumeratori di solo avanzamento sono in genere molto più veloci e utilizzano meno memoria rispetto agli enumeratori convenzionali, ma non consentono chiamate a [**SWbemObject \_ . Clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="b2848-140">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="b2848-141"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b2848-141"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b2848-142">Fa in modo che Strumentazione gestione Windows (WMI) mantenga i puntatori agli oggetti dell'enumerazione finché il client non rilascia l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="b2848-142">Causes Windows Management Instrumentation (WMI) to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="b2848-143"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="b2848-143"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="b2848-144">Causa la restituzione immediata della chiamata.</span><span class="sxs-lookup"><span data-stu-id="b2848-144">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="b2848-145"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b2848-145"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b2848-146">Causa il blocco della chiamata fino al completamento della query.</span><span class="sxs-lookup"><span data-stu-id="b2848-146">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="b2848-147">Questo flag chiama il metodo in modalità sincrona.</span><span class="sxs-lookup"><span data-stu-id="b2848-147">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="b2848-148"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="b2848-148"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="b2848-149">Fa in modo che WMI restituisca i dati di modifica della classe insieme alla definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="b2848-149">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="b2848-150">Per ulteriori informazioni, vedere la pagina relativa alla [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="b2848-150">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b2848-151">*objWbemNamedValueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="b2848-151">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2848-152">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="b2848-152">Typically, this is undefined.</span></span> <span data-ttu-id="b2848-153">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="b2848-153">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="b2848-154">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="b2848-154">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2848-155">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2848-155">Return value</span></span>

<span data-ttu-id="b2848-156">Se il metodo ha esito positivo, il metodo restituisce un oggetto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="b2848-156">If the method is successful, the method returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b2848-157">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="b2848-157">Error codes</span></span>

<span data-ttu-id="b2848-158">Dopo il completamento del metodo **ReferencesTo** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="b2848-158">After the completion of the **ReferencesTo** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="b2848-159">Una raccolta restituita con zero elementi non è un errore.</span><span class="sxs-lookup"><span data-stu-id="b2848-159">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="b2848-160">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="b2848-160">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="b2848-161">L'utente corrente non dispone dell'autorizzazione per visualizzare una o più classi restituite dalla chiamata.</span><span class="sxs-lookup"><span data-stu-id="b2848-161">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="b2848-162">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b2848-162">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b2848-163">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="b2848-163">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b2848-164">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="b2848-164">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="b2848-165">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="b2848-165">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="b2848-166">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b2848-166">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b2848-167">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="b2848-167">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b2848-168">**wbemFlagUseAmendedQualifiers** -131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="b2848-168">**wbemFlagUseAmendedQualifiers** - 131072 (0x20000)</span></span>
</dt> <dd>

<span data-ttu-id="b2848-169">Causa la restituzione dei dati di modifica della classe da parte di WMI con la definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="b2848-169">Causes WMI to return class amendment data with the base class definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2848-170">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2848-170">Remarks</span></span>

<span data-ttu-id="b2848-171">Per ulteriori informazioni sui riferimenti della query WQL associata, delle istanze di origine e degli oggetti di associazione, vedere associazioners [of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b2848-171">For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2848-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2848-172">Requirements</span></span>



| <span data-ttu-id="b2848-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2848-173">Requirement</span></span> | <span data-ttu-id="b2848-174">Valore</span><span class="sxs-lookup"><span data-stu-id="b2848-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2848-175">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2848-175">Minimum supported client</span></span><br/> | <span data-ttu-id="b2848-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2848-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b2848-177">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2848-177">Minimum supported server</span></span><br/> | <span data-ttu-id="b2848-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2848-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b2848-179">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2848-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2848-180"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2848-180"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b2848-181">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="b2848-181">Type library</span></span><br/>             | <dl> <span data-ttu-id="b2848-182"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b2848-182"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b2848-183">DLL</span><span class="sxs-lookup"><span data-stu-id="b2848-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2848-184"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2848-184"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b2848-185">CLSID</span><span class="sxs-lookup"><span data-stu-id="b2848-185">CLSID</span></span><br/>                    | <span data-ttu-id="b2848-186">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="b2848-186">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="b2848-187">IID</span><span class="sxs-lookup"><span data-stu-id="b2848-187">IID</span></span><br/>                      | <span data-ttu-id="b2848-188">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="b2848-188">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="b2848-189">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2848-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2848-190">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="b2848-190">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="b2848-191">**SWbemObject. Associator\_**</span><span class="sxs-lookup"><span data-stu-id="b2848-191">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="b2848-192">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="b2848-192">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="b2848-193">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="b2848-193">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> </dl>

 

 




