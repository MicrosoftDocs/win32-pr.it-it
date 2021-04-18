---
description: Restituisce una raccolta di oggetti (classi o istanze) chiamati endpoint associati a un oggetto specificato.
ms.assetid: a78e6701-6779-4a02-b811-23b2da4f4167
ms.tgt_platform: multiple
title: Metodo SWbemServices. AssociatorsOf (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0208ef23158d71a5174fcb6759acba1d64bd09a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313165"
---
# <a name="swbemservicesassociatorsof-method"></a><span data-ttu-id="1496a-103">SWbemServices. AssociatorsOf, metodo</span><span class="sxs-lookup"><span data-stu-id="1496a-103">SWbemServices.AssociatorsOf method</span></span>

<span data-ttu-id="1496a-104">Il metodo **AssociatorsOf** dell'oggetto [**SWbemServices**](swbemservices.md) restituisce una raccolta di oggetti (classi o istanze) chiamati endpoint associati a un oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="1496a-104">The **AssociatorsOf** method of the [**SWbemServices**](swbemservices.md) object returns a collection of objects (classes or instances) called endpoints that are associated with a specified object.</span></span> <span data-ttu-id="1496a-105">Questo metodo esegue la stessa funzione eseguita dagli ASSOCIATOri della query WQL.</span><span class="sxs-lookup"><span data-stu-id="1496a-105">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="1496a-106">Per impostazione predefinita, questo metodo viene chiamato in modalità semisincrono.</span><span class="sxs-lookup"><span data-stu-id="1496a-106">This method is called in the semisynchronous mode by default.</span></span> <span data-ttu-id="1496a-107">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="1496a-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="1496a-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="1496a-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1496a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1496a-109">Syntax</span></span>


```VB
objWbemObjectSet = .AssociatorsOf( _
  ByVal strObjectPath, _
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



## <a name="parameters"></a><span data-ttu-id="1496a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="1496a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1496a-111">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="1496a-111">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="1496a-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1496a-112">Required.</span></span> <span data-ttu-id="1496a-113">Stringa che contiene il percorso dell'oggetto della classe o dell'istanza di origine.</span><span class="sxs-lookup"><span data-stu-id="1496a-113">String that contains the object path of the source class or instance.</span></span> <span data-ttu-id="1496a-114">Per ulteriori informazioni, vedere [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="1496a-114">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="1496a-115">*strAssocClass* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="1496a-115">*strAssocClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1496a-116">Stringa che contiene una classe di associazione.</span><span class="sxs-lookup"><span data-stu-id="1496a-116">String that contains an association class.</span></span> <span data-ttu-id="1496a-117">Se specificato, questo parametro indica che gli endpoint restituiti devono essere associati all'origine tramite la classe di associazione specificata o una classe derivata da questa classe di associazione.</span><span class="sxs-lookup"><span data-stu-id="1496a-117">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class that is derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="1496a-118">*strResultClass* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="1496a-118">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1496a-119">Stringa che contiene un nome di classe.</span><span class="sxs-lookup"><span data-stu-id="1496a-119">String that contains a class name.</span></span> <span data-ttu-id="1496a-120">Se specificato, questo parametro facoltativo indica che gli endpoint restituiti devono appartenere o essere derivati dalla classe specificata in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="1496a-120">If specified, this optional parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1496a-121">*strResultRole* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="1496a-121">*strResultRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1496a-122">Stringa che contiene un nome di proprietà.</span><span class="sxs-lookup"><span data-stu-id="1496a-122">String that contains a property name.</span></span> <span data-ttu-id="1496a-123">Se specificato, questo parametro indica che gli endpoint restituiti devono riprodurre un particolare ruolo nella propria associazione con l'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="1496a-123">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="1496a-124">Il ruolo è definito dal nome di una proprietà specificata (che deve essere una proprietà di riferimento) di un'associazione.</span><span class="sxs-lookup"><span data-stu-id="1496a-124">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="1496a-125">*strRole* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="1496a-125">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1496a-126">Stringa che contiene un nome di proprietà.</span><span class="sxs-lookup"><span data-stu-id="1496a-126">String that contains a property name.</span></span> <span data-ttu-id="1496a-127">Se specificato, questo parametro indica che gli endpoint restituiti devono partecipare a un'associazione con l'oggetto di origine in cui l'oggetto di origine svolge un particolare ruolo.</span><span class="sxs-lookup"><span data-stu-id="1496a-127">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="1496a-128">Il ruolo è definito dal nome di una proprietà specificata (che deve essere una proprietà di riferimento) di un'associazione.</span><span class="sxs-lookup"><span data-stu-id="1496a-128">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="1496a-129">*bClassesOnly* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="1496a-129">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1496a-130">Valore booleano che indica se deve essere restituito un elenco di nomi di classe anziché le istanze effettive delle classi.</span><span class="sxs-lookup"><span data-stu-id="1496a-130">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="1496a-131">Queste sono le classi a cui appartengono le istanze dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="1496a-131">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="1496a-132">Il valore predefinito per questo parametro è **false**.</span><span class="sxs-lookup"><span data-stu-id="1496a-132">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1496a-133">*bSchemaOnly* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="1496a-133">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1496a-134">Valore booleano che indica se la query viene applicata allo schema anziché ai dati.</span><span class="sxs-lookup"><span data-stu-id="1496a-134">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="1496a-135">Il valore predefinito per questo parametro è **false**.</span><span class="sxs-lookup"><span data-stu-id="1496a-135">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="1496a-136">Può essere impostato su **true** solo se il parametro *strObjectPath* specifica il percorso dell'oggetto di una classe.</span><span class="sxs-lookup"><span data-stu-id="1496a-136">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="1496a-137">Se impostato su **true**, il set di endpoint restituiti rappresenta le classi associate adeguatamente alla classe di origine nello schema.</span><span class="sxs-lookup"><span data-stu-id="1496a-137">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="1496a-138">*strRequiredAssocQualifier* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="1496a-138">*strRequiredAssocQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1496a-139">Stringa che contiene un nome di qualificatore.</span><span class="sxs-lookup"><span data-stu-id="1496a-139">String that contains a qualifier name.</span></span> <span data-ttu-id="1496a-140">Se specificato, questo parametro indica che gli endpoint restituiti devono essere associati all'oggetto di origine tramite una classe di associazione che include il qualificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="1496a-140">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="1496a-141">*strRequiredQualifier* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="1496a-141">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1496a-142">Stringa che contiene un nome di qualificatore.</span><span class="sxs-lookup"><span data-stu-id="1496a-142">String that contains a qualifier name.</span></span> <span data-ttu-id="1496a-143">Se specificato, questo parametro indica che gli endpoint restituiti devono includere il qualificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="1496a-143">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="1496a-144">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="1496a-144">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1496a-145">Integer che specifica flag aggiuntivi per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="1496a-145">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="1496a-146">Il valore predefinito per questo parametro è **wbemFlagReturnImmediately**, che chiama il metodo in modalità semisincrono.</span><span class="sxs-lookup"><span data-stu-id="1496a-146">The default value for this parameter is **wbemFlagReturnImmediately**, which calls the method in the semisynchronous mode.</span></span> <span data-ttu-id="1496a-147">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1496a-147">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="1496a-148"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="1496a-148"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="1496a-149">Causa la restituzione di un enumeratore di sola trasmissione.</span><span class="sxs-lookup"><span data-stu-id="1496a-149">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="1496a-150">Gli enumeratori di solo avanzamento sono in genere molto più veloci e utilizzano meno memoria rispetto agli enumeratori convenzionali, ma non consentono chiamate a [**SWbemObject \_ . Clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="1496a-150">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="1496a-151"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="1496a-151"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="1496a-152">Causa la conservazione dei puntatori agli oggetti dell'enumerazione da parte di WMI finché il client non rilascia l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="1496a-152">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="1496a-153"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="1496a-153"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="1496a-154">Causa la restituzione immediata della chiamata.</span><span class="sxs-lookup"><span data-stu-id="1496a-154">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="1496a-155"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="1496a-155"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="1496a-156">Causa il blocco della chiamata fino al completamento della query.</span><span class="sxs-lookup"><span data-stu-id="1496a-156">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="1496a-157">Questo flag chiama il metodo in modalità sincrona.</span><span class="sxs-lookup"><span data-stu-id="1496a-157">This flag calls the method in synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="1496a-158"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="1496a-158"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="1496a-159">Fa in modo che WMI restituisca i dati di modifica della classe insieme alla definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="1496a-159">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="1496a-160">Per ulteriori informazioni, vedere la pagina relativa alla [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="1496a-160">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1496a-161">*objwbemNamedValueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="1496a-161">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1496a-162">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="1496a-162">Typically, this is undefined.</span></span> <span data-ttu-id="1496a-163">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="1496a-163">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="1496a-164">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="1496a-164">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1496a-165">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1496a-165">Return value</span></span>

<span data-ttu-id="1496a-166">Se la chiamata ha esito positivo, viene restituito un oggetto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="1496a-166">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1496a-167">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="1496a-167">Error codes</span></span>

<span data-ttu-id="1496a-168">Dopo il completamento del metodo **AssociatorsOf** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="1496a-168">After the completion of the **AssociatorsOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="1496a-169">Una raccolta restituita con zero elementi non è un errore.</span><span class="sxs-lookup"><span data-stu-id="1496a-169">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="1496a-170">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="1496a-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="1496a-171">L'utente corrente non dispone dell'autorizzazione per visualizzare una o più classi restituite dalla chiamata.</span><span class="sxs-lookup"><span data-stu-id="1496a-171">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="1496a-172">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="1496a-172">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="1496a-173">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="1496a-173">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="1496a-174">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="1496a-174">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="1496a-175">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="1496a-175">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="1496a-176">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="1496a-176">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="1496a-177">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="1496a-177">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1496a-178">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="1496a-178">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="1496a-179">L'elemento richiesto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="1496a-179">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1496a-180">Commenti</span><span class="sxs-lookup"><span data-stu-id="1496a-180">Remarks</span></span>

<span data-ttu-id="1496a-181">Il metodo recupera le istanze di risorse gestite associate a una risorsa specificata tramite una o più classi di associazione.</span><span class="sxs-lookup"><span data-stu-id="1496a-181">The method retrieves the instances of managed resources that are associated with a specified resource through one or more association classes.</span></span> <span data-ttu-id="1496a-182">Si specifica il percorso dell'oggetto per l'endpoint di origine e AssociatorsOf restituisce le risorse gestite sull'endpoint opposto.</span><span class="sxs-lookup"><span data-stu-id="1496a-182">You provide the object path for the originating endpoint, and AssociatorsOf returns the managed resources at the opposite endpoint.</span></span> <span data-ttu-id="1496a-183">Il metodo AssociatorsOf esegue la stessa funzione eseguita dagli ASSOCIATOri della query WQL.</span><span class="sxs-lookup"><span data-stu-id="1496a-183">The AssociatorsOf method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="1496a-184">Per ulteriori informazioni sugli ASSOCIAtori della query WQL, le istanze di origine e gli endpoint, vedere [associatirs of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="1496a-184">For more information about the ASSOCIATORS OF WQL query, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1496a-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1496a-185">Requirements</span></span>



| <span data-ttu-id="1496a-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="1496a-186">Requirement</span></span> | <span data-ttu-id="1496a-187">Valore</span><span class="sxs-lookup"><span data-stu-id="1496a-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1496a-188">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1496a-188">Minimum supported client</span></span><br/> | <span data-ttu-id="1496a-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1496a-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1496a-190">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1496a-190">Minimum supported server</span></span><br/> | <span data-ttu-id="1496a-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1496a-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1496a-192">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1496a-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="1496a-193"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1496a-193"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1496a-194">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="1496a-194">Type library</span></span><br/>             | <dl> <span data-ttu-id="1496a-195"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1496a-195"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1496a-196">DLL</span><span class="sxs-lookup"><span data-stu-id="1496a-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1496a-197"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1496a-197"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1496a-198">CLSID</span><span class="sxs-lookup"><span data-stu-id="1496a-198">CLSID</span></span><br/>                    | <span data-ttu-id="1496a-199">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="1496a-199">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="1496a-200">IID</span><span class="sxs-lookup"><span data-stu-id="1496a-200">IID</span></span><br/>                      | <span data-ttu-id="1496a-201">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="1496a-201">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="1496a-202">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1496a-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1496a-203">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="1496a-203">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="1496a-204">**SWbemObject. Associator\_**</span><span class="sxs-lookup"><span data-stu-id="1496a-204">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="1496a-205">**SWbemObject. AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="1496a-205">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)
</dt> <dt>

[<span data-ttu-id="1496a-206">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="1496a-206">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
</dt> <dt>

[<span data-ttu-id="1496a-207">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="1496a-207">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="1496a-208">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="1496a-208">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




