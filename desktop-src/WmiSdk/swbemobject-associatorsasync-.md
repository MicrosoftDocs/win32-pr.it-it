---
description: Il \_ Metodo AssociatorsAsync di SWbemObject ottiene oggetti (classi o istanze) associati all'oggetto corrente. Questi oggetti sono detti endpoint. Questo metodo esegue la stessa funzione eseguita dagli ASSOCIATOri della query WQL.
ms.assetid: c71e11cd-39a5-40d8-b279-f5ee9ff3ae04
ms.tgt_platform: multiple
title: Metodo SWbemObject.AssociatorsAsync_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fe7a592327b6952308e44ac054fb94e21aa6d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309830"
---
# <a name="swbemobjectassociatorsasync_-method"></a><span data-ttu-id="68582-105">SWbemObject. AssociatorsAsync, \_ Metodo</span><span class="sxs-lookup"><span data-stu-id="68582-105">SWbemObject.AssociatorsAsync\_ method</span></span>

<span data-ttu-id="68582-106">Il **metodo \_ AssociatorsAsync** di [**SWbemObject**](swbemobject.md) ottiene oggetti (classi o istanze) associati all'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="68582-106">The **AssociatorsAsync\_** method of [**SWbemObject**](swbemobject.md) obtains objects (classes or instances) that are associated with the current object.</span></span> <span data-ttu-id="68582-107">Questi oggetti sono detti endpoint.</span><span class="sxs-lookup"><span data-stu-id="68582-107">These objects are called endpoints.</span></span> <span data-ttu-id="68582-108">Questo metodo esegue la stessa funzione eseguita dagli ASSOCIATOri della query WQL.</span><span class="sxs-lookup"><span data-stu-id="68582-108">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="68582-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="68582-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="68582-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68582-110">Syntax</span></span>


```VB
SWbemObject.AssociatorsAsync_( _
  ByVal objWbemSink, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="68582-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="68582-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68582-112">*objWbemSink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68582-112">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68582-113">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="68582-113">Required.</span></span> <span data-ttu-id="68582-114">Sink di oggetto che riceve gli oggetti in modo asincrono come callback.</span><span class="sxs-lookup"><span data-stu-id="68582-114">Object sink that receives the objects asynchronously as a callback.</span></span>

</dd> <dt>

<span data-ttu-id="68582-115">*strAssocClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="68582-115">*strAssocClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68582-116">Stringa che contiene una classe di associazione.</span><span class="sxs-lookup"><span data-stu-id="68582-116">String that contains an association class.</span></span> <span data-ttu-id="68582-117">Se specificato, questo parametro indica che gli endpoint restituiti devono essere associati all'origine tramite la classe di associazione specificata o una classe derivata da questa classe di associazione.</span><span class="sxs-lookup"><span data-stu-id="68582-117">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="68582-118">*strResultClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="68582-118">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68582-119">Stringa che contiene un nome di classe.</span><span class="sxs-lookup"><span data-stu-id="68582-119">String that contains a class name.</span></span> <span data-ttu-id="68582-120">Se specificato, questo parametro indica che gli endpoint restituiti devono appartenere o essere derivati dalla classe specificata in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="68582-120">If specified, this parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="68582-121">*strResultRole* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="68582-121">*strResultRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68582-122">Stringa che contiene un nome di proprietà.</span><span class="sxs-lookup"><span data-stu-id="68582-122">String that contains a property name.</span></span> <span data-ttu-id="68582-123">Se specificato, questo parametro indica che gli endpoint restituiti devono riprodurre un particolare ruolo nella propria associazione con l'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="68582-123">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="68582-124">Il ruolo è definito dal nome di una proprietà specificata (che deve essere una proprietà di riferimento) di un'associazione.</span><span class="sxs-lookup"><span data-stu-id="68582-124">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="68582-125">*strRole* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="68582-125">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68582-126">Stringa che contiene un nome di proprietà.</span><span class="sxs-lookup"><span data-stu-id="68582-126">String that contains a property name.</span></span> <span data-ttu-id="68582-127">Se specificato, questo parametro indica che gli endpoint restituiti devono partecipare a un'associazione con l'oggetto di origine in cui l'oggetto di origine svolge un particolare ruolo.</span><span class="sxs-lookup"><span data-stu-id="68582-127">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="68582-128">Il ruolo è definito dal nome di una proprietà specificata (che deve essere una proprietà di riferimento) di un'associazione.</span><span class="sxs-lookup"><span data-stu-id="68582-128">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="68582-129">*bClassesOnly* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="68582-129">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68582-130">Valore booleano che indica se deve essere restituito un elenco di nomi di classe anziché le istanze effettive delle classi.</span><span class="sxs-lookup"><span data-stu-id="68582-130">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="68582-131">Queste sono le classi a cui appartengono le istanze dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="68582-131">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="68582-132">Il valore predefinito per questo parametro è **false**.</span><span class="sxs-lookup"><span data-stu-id="68582-132">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="68582-133">*bSchemaOnly* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="68582-133">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68582-134">Valore booleano che indica se la query viene applicata allo schema anziché ai dati.</span><span class="sxs-lookup"><span data-stu-id="68582-134">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="68582-135">Il valore predefinito per questo parametro è **false**.</span><span class="sxs-lookup"><span data-stu-id="68582-135">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="68582-136">Può essere impostato su **true** solo se l'oggetto su cui viene richiamato questo metodo è una classe.</span><span class="sxs-lookup"><span data-stu-id="68582-136">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="68582-137">Se impostato su **true**, il set di endpoint restituiti rappresenta le classi associate adeguatamente alla classe di origine nello schema.</span><span class="sxs-lookup"><span data-stu-id="68582-137">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="68582-138">*strRequiredAssocQualifier* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="68582-138">*strRequiredAssocQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68582-139">Stringa che contiene un nome di qualificatore.</span><span class="sxs-lookup"><span data-stu-id="68582-139">String that contains a qualifier name.</span></span> <span data-ttu-id="68582-140">Se specificato, questo parametro indica che gli endpoint restituiti devono essere associati all'oggetto di origine tramite una classe di associazione che include il qualificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="68582-140">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="68582-141">*strRequiredQualifier* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="68582-141">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68582-142">Stringa che contiene un nome di qualificatore.</span><span class="sxs-lookup"><span data-stu-id="68582-142">String that contains a qualifier name.</span></span> <span data-ttu-id="68582-143">Se specificato, questo parametro indica che gli endpoint restituiti devono includere il qualificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="68582-143">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="68582-144">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="68582-144">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68582-145">Integer che specifica flag aggiuntivi per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="68582-145">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="68582-146">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="68582-146">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="68582-147"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="68582-147"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="68582-148">Fa in modo che le chiamate asincrone inviino gli aggiornamenti di stato al gestore eventi [**SWbemSink. OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="68582-148">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="68582-149"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="68582-149"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="68582-150">Impedisce alle chiamate asincrone di inviare aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="68582-150">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="68582-151"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="68582-151"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="68582-152">Fa in modo che WMI restituisca la classe localizzata e le descrizioni di proprietà.</span><span class="sxs-lookup"><span data-stu-id="68582-152">Causes WMI to return the localized class and property descriptions.</span></span> <span data-ttu-id="68582-153">Per ulteriori informazioni, vedere la pagina relativa alla [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="68582-153">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="68582-154">*objwbemNamedValueSet* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="68582-154">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68582-155">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="68582-155">Typically, this is undefined.</span></span> <span data-ttu-id="68582-156">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="68582-156">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="68582-157">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="68582-157">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="68582-158">*objWbemAsyncContext* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="68582-158">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68582-159">Si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink di oggetto per identificare l'origine della chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="68582-159">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="68582-160">Utilizzare questo parametro se si eseguono più chiamate asincrone utilizzando lo stesso sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="68582-160">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="68582-161">Per usare questo parametro, creare un oggetto **SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona che si sta effettuando.</span><span class="sxs-lookup"><span data-stu-id="68582-161">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="68582-162">Questo oggetto **SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta tramite il metodo [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="68582-162">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="68582-163">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="68582-163">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68582-164">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68582-164">Return value</span></span>

<span data-ttu-id="68582-165">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="68582-165">This method does not return a value.</span></span> <span data-ttu-id="68582-166">In caso di esito positivo, il sink riceve un evento [**OnObjectReady**](swbemsink-onobjectready.md) per ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="68582-166">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="68582-167">Dopo l'ultima istanza, il sink di oggetto riceve un evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="68582-167">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="68582-168">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="68582-168">Error codes</span></span>

<span data-ttu-id="68582-169">Dopo il completamento del **metodo \_ AssociatorsAsync** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="68582-169">After completion of the **AssociatorsAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="68582-170">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="68582-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="68582-171">L'utente corrente non dispone delle autorizzazioni necessarie per visualizzare una o più classi restituite dalla chiamata.</span><span class="sxs-lookup"><span data-stu-id="68582-171">The current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="68582-172">**wbemErrFailed** -2147449889 (0x7FFF7C21)</span><span class="sxs-lookup"><span data-stu-id="68582-172">**wbemErrFailed** - 2147449889 (0x7FFF7C21)</span></span>
</dt> <dd>

<span data-ttu-id="68582-173">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="68582-173">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="68582-174">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="68582-174">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="68582-175">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="68582-175">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="68582-176">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="68582-176">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="68582-177">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="68582-177">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68582-178">Commenti</span><span class="sxs-lookup"><span data-stu-id="68582-178">Remarks</span></span>

<span data-ttu-id="68582-179">Questa chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="68582-179">This call returns immediately.</span></span> <span data-ttu-id="68582-180">Gli oggetti e lo stato richiesti vengono restituiti al chiamante tramite le chiamate recapitate al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="68582-180">The requested objects and status are returned to the caller through call-backs delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="68582-181">Per elaborare ogni oggetto all'arrivo, creare un *objWbemSink*. Subroutine dell'evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="68582-181">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="68582-182">Dopo la restituzione di tutti gli oggetti, è possibile eseguire l'elaborazione finale nell'implementazione di *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="68582-182">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="68582-183">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="68582-183">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="68582-184">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="68582-184">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="68582-185">Per eliminare i rischi, usare la comunicazione semisincrono o la comunicazione sincrona.</span><span class="sxs-lookup"><span data-stu-id="68582-185">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="68582-186">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="68582-186">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="68582-187">Per ulteriori informazioni sugli ASSOCIAtori delle query WQL associate, sulle istanze di origine e sugli endpoint, vedere [associazioners of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="68582-187">For more information about the ASSOCIATORS OF associated WQL queries, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68582-188">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68582-188">Requirements</span></span>



| <span data-ttu-id="68582-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="68582-189">Requirement</span></span> | <span data-ttu-id="68582-190">Valore</span><span class="sxs-lookup"><span data-stu-id="68582-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68582-191">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68582-191">Minimum supported client</span></span><br/> | <span data-ttu-id="68582-192">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68582-192">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68582-193">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68582-193">Minimum supported server</span></span><br/> | <span data-ttu-id="68582-194">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68582-194">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68582-195">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68582-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="68582-196"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="68582-196"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="68582-197">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="68582-197">Type library</span></span><br/>             | <dl> <span data-ttu-id="68582-198"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="68582-198"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="68582-199">DLL</span><span class="sxs-lookup"><span data-stu-id="68582-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68582-200"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68582-200"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="68582-201">CLSID</span><span class="sxs-lookup"><span data-stu-id="68582-201">CLSID</span></span><br/>                    | <span data-ttu-id="68582-202">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="68582-202">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="68582-203">IID</span><span class="sxs-lookup"><span data-stu-id="68582-203">IID</span></span><br/>                      | <span data-ttu-id="68582-204">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="68582-204">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="68582-205">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68582-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68582-206">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="68582-206">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="68582-207">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="68582-207">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
</dt> <dt>

[<span data-ttu-id="68582-208">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="68582-208">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="68582-209">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="68582-209">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

