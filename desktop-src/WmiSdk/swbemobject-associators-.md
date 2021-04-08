---
description: Il metodo ASSOCIATORS \_ dell'oggetto SWbemObject restituisce una raccolta di oggetti (classi o istanze) associati all'oggetto corrente.
ms.assetid: 79f01853-c649-4cbe-b2fa-cff38fb4b733
ms.tgt_platform: multiple
title: Metodo SWbemObject.Associators_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Associators_
- ISWbemObject.Associators_
- ISWbemObject.Associators_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1f9ff4536936661ece54b5bff29e500ce6e98d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968187"
---
# <a name="swbemobjectassociators_-method"></a><span data-ttu-id="06053-103">Metodo SWbemObject. Associator \_</span><span class="sxs-lookup"><span data-stu-id="06053-103">SWbemObject.Associators\_ method</span></span>

<span data-ttu-id="06053-104">Il metodo ASSOCIATORS dell'oggetto [**SWbemObject**](swbemobject.md) restituisce una raccolta di oggetti (classi o istanze) associati all'oggetto corrente. **\_**</span><span class="sxs-lookup"><span data-stu-id="06053-104">The **Associators\_** method of the [**SWbemObject**](swbemobject.md) object returns a collection of objects (classes or instances) that are associated with the current object.</span></span> <span data-ttu-id="06053-105">Questi oggetti restituiti sono detti endpoint.</span><span class="sxs-lookup"><span data-stu-id="06053-105">These returned objects are called endpoints.</span></span> <span data-ttu-id="06053-106">Questo metodo esegue la stessa funzione eseguita dagli ASSOCIATOri della query WQL.</span><span class="sxs-lookup"><span data-stu-id="06053-106">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="06053-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="06053-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="06053-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06053-108">Syntax</span></span>


```VB
objWbemObjectSet = .Associators_( _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="06053-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="06053-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06053-110">*strAssocClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="06053-110">*strAssocClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06053-111">Stringa che contiene una classe di associazione.</span><span class="sxs-lookup"><span data-stu-id="06053-111">String that contains an association class.</span></span> <span data-ttu-id="06053-112">Se specificato, questo parametro indica che gli endpoint restituiti devono essere associati all'origine tramite la classe di associazione specificata o una classe derivata da questa classe di associazione.</span><span class="sxs-lookup"><span data-stu-id="06053-112">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="06053-113">*strResultClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="06053-113">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06053-114">Stringa che contiene un nome di classe.</span><span class="sxs-lookup"><span data-stu-id="06053-114">String that contains a class name.</span></span> <span data-ttu-id="06053-115">Se specificato, questo parametro indica che gli endpoint restituiti devono appartenere o essere derivati dalla classe specificata in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="06053-115">If specified, this parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="06053-116">*strResultRole* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="06053-116">*strResultRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06053-117">Stringa che contiene un nome di proprietà.</span><span class="sxs-lookup"><span data-stu-id="06053-117">String that contains a property name.</span></span> <span data-ttu-id="06053-118">Se specificato, questo parametro indica che gli endpoint restituiti devono riprodurre un particolare ruolo nella propria associazione con l'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="06053-118">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="06053-119">Il ruolo è definito dal nome di una proprietà specificata (che deve essere una proprietà di riferimento) di un'associazione.</span><span class="sxs-lookup"><span data-stu-id="06053-119">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="06053-120">*strRole* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="06053-120">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06053-121">Stringa che contiene un nome di proprietà.</span><span class="sxs-lookup"><span data-stu-id="06053-121">String that contains a property name.</span></span> <span data-ttu-id="06053-122">Se specificato, questo parametro indica che gli endpoint restituiti devono partecipare a un'associazione con l'oggetto di origine in cui l'oggetto di origine svolge un particolare ruolo.</span><span class="sxs-lookup"><span data-stu-id="06053-122">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="06053-123">Il ruolo è definito dal nome di una proprietà specificata (che deve essere una proprietà di riferimento) di un'associazione.</span><span class="sxs-lookup"><span data-stu-id="06053-123">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="06053-124">*bClassesOnly* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="06053-124">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06053-125">Valore booleano che indica se deve essere restituito un elenco di nomi di classe anziché le istanze effettive delle classi.</span><span class="sxs-lookup"><span data-stu-id="06053-125">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="06053-126">Queste sono le classi a cui appartengono le istanze dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="06053-126">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="06053-127">Il valore predefinito per questo parametro è **false**.</span><span class="sxs-lookup"><span data-stu-id="06053-127">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="06053-128">*bSchemaOnly* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="06053-128">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06053-129">Si tratta di un valore booleano che indica se la query viene applicata allo schema anziché ai dati.</span><span class="sxs-lookup"><span data-stu-id="06053-129">This is a Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="06053-130">Il valore predefinito per questo parametro è **false**.</span><span class="sxs-lookup"><span data-stu-id="06053-130">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="06053-131">Può essere impostato su **true** solo se l'oggetto su cui viene richiamato questo metodo è una classe.</span><span class="sxs-lookup"><span data-stu-id="06053-131">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="06053-132">Se impostato su **true**, il set di endpoint restituiti rappresenta le classi associate adeguatamente alla classe di origine nello schema.</span><span class="sxs-lookup"><span data-stu-id="06053-132">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="06053-133">*strRequiredAssocQualifier* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="06053-133">*strRequiredAssocQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06053-134">Stringa che contiene un nome di qualificatore.</span><span class="sxs-lookup"><span data-stu-id="06053-134">String that contains a qualifier name.</span></span> <span data-ttu-id="06053-135">Questo parametro, se specificato, indica che gli endpoint restituiti devono essere associati all'oggetto di origine tramite una classe di associazione che include il qualificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="06053-135">This parameter, if specified, indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="06053-136">*strRequiredQualifier* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="06053-136">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06053-137">Stringa che contiene un nome di qualificatore.</span><span class="sxs-lookup"><span data-stu-id="06053-137">String that contains a qualifier name.</span></span> <span data-ttu-id="06053-138">Questo parametro, se specificato, indica che gli endpoint restituiti devono includere il qualificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="06053-138">This parameter, if specified, indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="06053-139">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="06053-139">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06053-140">Integer che specifica flag aggiuntivi per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="06053-140">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="06053-141">Il valore predefinito per questo parametro è **wbemFlagReturnImmediately**, che indica alla chiamata di restituire immediatamente invece di attendere il completamento della query.</span><span class="sxs-lookup"><span data-stu-id="06053-141">The default for this parameter is **wbemFlagReturnImmediately**, which directs the call to return immediately rather than wait until the query has completed.</span></span> <span data-ttu-id="06053-142">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="06053-142">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="06053-143"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="06053-143"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="06053-144">Causa la restituzione di un enumeratore di sola trasmissione.</span><span class="sxs-lookup"><span data-stu-id="06053-144">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="06053-145">Gli enumeratori di solo avanzamento sono in genere molto più veloci e utilizzano meno memoria rispetto agli enumeratori convenzionali, ma non consentono chiamate a [**SWbemObject \_ . Clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="06053-145">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="06053-146"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="06053-146"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="06053-147">Causa la conservazione dei puntatori agli oggetti dell'enumerazione da parte di WMI finché il client non rilascia l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="06053-147">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="06053-148"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="06053-148"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="06053-149">Causa la restituzione immediata della chiamata.</span><span class="sxs-lookup"><span data-stu-id="06053-149">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="06053-150"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="06053-150"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="06053-151">Causa il blocco della chiamata fino al completamento della query.</span><span class="sxs-lookup"><span data-stu-id="06053-151">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="06053-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="06053-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="06053-153">Causa la restituzione dei dati di modifica della classe da parte di WMI con la definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="06053-153">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="06053-154">L'inclusione di questo flag rende disponibile il testo qualificatore della descrizione localizzato per classi, proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="06053-154">Including this flag makes the localized description qualifier text available for classes, properties and methods.</span></span> <span data-ttu-id="06053-155">Per ulteriori informazioni sui qualificatori modificati, vedere [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="06053-155">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="06053-156">*objwbemNamedValueSet* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="06053-156">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06053-157">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="06053-157">Typically, this is undefined.</span></span> <span data-ttu-id="06053-158">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="06053-158">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="06053-159">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="06053-159">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06053-160">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06053-160">Return value</span></span>

<span data-ttu-id="06053-161">Se la chiamata ha esito positivo, viene restituito un oggetto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="06053-161">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="06053-162">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="06053-162">Error codes</span></span>

<span data-ttu-id="06053-163">Dopo il completamento del metodo **ASSOCIATORS \_** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="06053-163">After completion of the **Associators\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="06053-164">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="06053-164">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="06053-165">L'utente corrente non dispone delle autorizzazioni necessarie per visualizzare una o più classi restituite dalla chiamata.</span><span class="sxs-lookup"><span data-stu-id="06053-165">The current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="06053-166">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="06053-166">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="06053-167">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="06053-167">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="06053-168">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="06053-168">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="06053-169">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="06053-169">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="06053-170">**wbemErrOutOfMemory** -2147749894</span><span class="sxs-lookup"><span data-stu-id="06053-170">**wbemErrOutOfMemory** - 2147749894</span></span>
</dt> <dd>

<span data-ttu-id="06053-171">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="06053-171">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06053-172">Commenti</span><span class="sxs-lookup"><span data-stu-id="06053-172">Remarks</span></span>

<span data-ttu-id="06053-173">Per ulteriori informazioni sugli ASSOCIAtori della query WQL associata, sulle istanze di origine e sugli endpoint, vedere [associatirs of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="06053-173">For more information about the ASSOCIATORS OF associated WQL query, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="06053-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06053-174">Requirements</span></span>



| <span data-ttu-id="06053-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="06053-175">Requirement</span></span> | <span data-ttu-id="06053-176">Valore</span><span class="sxs-lookup"><span data-stu-id="06053-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06053-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06053-177">Minimum supported client</span></span><br/> | <span data-ttu-id="06053-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06053-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="06053-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06053-179">Minimum supported server</span></span><br/> | <span data-ttu-id="06053-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06053-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="06053-181">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06053-181">Header</span></span><br/>                   | <dl> <span data-ttu-id="06053-182"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="06053-182"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="06053-183">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="06053-183">Type library</span></span><br/>             | <dl> <span data-ttu-id="06053-184"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="06053-184"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="06053-185">DLL</span><span class="sxs-lookup"><span data-stu-id="06053-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06053-186"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06053-186"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="06053-187">CLSID</span><span class="sxs-lookup"><span data-stu-id="06053-187">CLSID</span></span><br/>                    | <span data-ttu-id="06053-188">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="06053-188">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="06053-189">IID</span><span class="sxs-lookup"><span data-stu-id="06053-189">IID</span></span><br/>                      | <span data-ttu-id="06053-190">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="06053-190">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="06053-191">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06053-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06053-192">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="06053-192">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="06053-193">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="06053-193">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="06053-194">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="06053-194">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="06053-195">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="06053-195">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




