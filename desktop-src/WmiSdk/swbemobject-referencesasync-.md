---
description: Il \_ Metodo ReferencesAsync di SWbemObject fornisce una raccolta di tutte le classi di associazione o di istanze che fanno riferimento all'oggetto corrente. Questo metodo esegue la stessa funzione eseguita dai riferimenti della query WQL.
ms.assetid: 44989726-3f68-453b-b9f5-e76fb0fbb152
ms.tgt_platform: multiple
title: Metodo SWbemObject.ReferencesAsync_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: aa4b85475a0dc9f736254c8f207469a52897b7ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309817"
---
# <a name="swbemobjectreferencesasync_-method"></a><span data-ttu-id="829c8-104">SWbemObject. ReferencesAsync, \_ Metodo</span><span class="sxs-lookup"><span data-stu-id="829c8-104">SWbemObject.ReferencesAsync\_ method</span></span>

<span data-ttu-id="829c8-105">Il **metodo \_ ReferencesAsync** di [**SWbemObject**](swbemobject.md) fornisce una raccolta di tutte le classi di associazione o di istanze che fanno riferimento all'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="829c8-105">The **ReferencesAsync\_** method of [**SWbemObject**](swbemobject.md) supplies a collection of all association classes or instances that refer to the current object.</span></span> <span data-ttu-id="829c8-106">Questo metodo esegue la stessa funzione eseguita dai [riferimenti della](references-of-statement.md) query WQL.</span><span class="sxs-lookup"><span data-stu-id="829c8-106">This method performs the same function that the WQL [REFERENCES OF](references-of-statement.md) query performs.</span></span>

<span data-ttu-id="829c8-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="829c8-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="829c8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="829c8-108">Syntax</span></span>


```VB
SWbemObject.ReferencesAsync_( _
  ByVal objWbemSink, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="829c8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="829c8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="829c8-110">*objWbemSink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="829c8-110">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="829c8-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="829c8-111">Required.</span></span> <span data-ttu-id="829c8-112">Sink di oggetto che riceve gli oggetti in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="829c8-112">Object sink that receives the objects asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="829c8-113">*strResultClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="829c8-113">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="829c8-114">Stringa che contiene un nome di classe.</span><span class="sxs-lookup"><span data-stu-id="829c8-114">String that contains a class name.</span></span> <span data-ttu-id="829c8-115">Se specificato, questo parametro indica che gli oggetti di associazione restituiti devono appartenere o essere derivati dalla classe specificata in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="829c8-115">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="829c8-116">*strRole* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="829c8-116">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="829c8-117">Stringa che contiene un nome di proprietà.</span><span class="sxs-lookup"><span data-stu-id="829c8-117">String that contains a property name.</span></span> <span data-ttu-id="829c8-118">Se specificato, questo parametro indica che gli oggetti di associazione restituiti devono essere limitati a quelli in cui l'oggetto di origine gioca un ruolo specifico.</span><span class="sxs-lookup"><span data-stu-id="829c8-118">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="829c8-119">Il nome di una proprietà di riferimento specificata definisce il ruolo di un'associazione.</span><span class="sxs-lookup"><span data-stu-id="829c8-119">The name of a specified reference property defines the role of an association.</span></span>

</dd> <dt>

<span data-ttu-id="829c8-120">*bClassesOnly* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="829c8-120">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="829c8-121">Valore booleano che indica se deve essere restituito un elenco di nomi di classe anziché le istanze effettive delle classi.</span><span class="sxs-lookup"><span data-stu-id="829c8-121">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="829c8-122">Queste sono le classi a cui appartengono gli oggetti Association.</span><span class="sxs-lookup"><span data-stu-id="829c8-122">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="829c8-123">Il valore predefinito per questo parametro è **false**.</span><span class="sxs-lookup"><span data-stu-id="829c8-123">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="829c8-124">*bSchemaOnly* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="829c8-124">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="829c8-125">Valore booleano che indica se la query viene applicata o meno allo schema anziché ai dati.</span><span class="sxs-lookup"><span data-stu-id="829c8-125">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="829c8-126">Il valore predefinito per questo parametro è **false**.</span><span class="sxs-lookup"><span data-stu-id="829c8-126">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="829c8-127">Può essere impostato su **true** solo se l'oggetto su cui viene richiamato questo metodo è una classe.</span><span class="sxs-lookup"><span data-stu-id="829c8-127">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="829c8-128">Se è impostato su **true**, il set di endpoint restituiti rappresenta le classi associate adeguatamente alla classe di origine nello schema.</span><span class="sxs-lookup"><span data-stu-id="829c8-128">When set to **TRUE**, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="829c8-129">*strRequiredQualifier* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="829c8-129">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="829c8-130">Stringa che contiene un nome di qualificatore.</span><span class="sxs-lookup"><span data-stu-id="829c8-130">String that contains a qualifier name.</span></span> <span data-ttu-id="829c8-131">Se specificato, questo parametro indica che gli oggetti Association restituiti devono includere il qualificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="829c8-131">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="829c8-132">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="829c8-132">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="829c8-133">Integer che specifica flag aggiuntivi per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="829c8-133">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="829c8-134">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="829c8-134">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="829c8-135"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="829c8-135"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="829c8-136">Fa in modo che le chiamate asincrone inviino gli aggiornamenti di stato al gestore eventi [**SWbemSink. OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="829c8-136">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="829c8-137"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="829c8-137"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="829c8-138">Impedisce alle chiamate asincrone di inviare aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="829c8-138">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="829c8-139"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="829c8-139"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="829c8-140">Fa in modo che Strumentazione gestione Windows (WMI) restituisca i dati di modifica della classe con la definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="829c8-140">Causes Windows Management Instrumentation (WMI) to return class amendment data with the base class definition.</span></span> <span data-ttu-id="829c8-141">Per ulteriori informazioni, vedere la pagina relativa alla [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="829c8-141">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="829c8-142">*objwbemNamedValueSet* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="829c8-142">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="829c8-143">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="829c8-143">Typically, this is undefined.</span></span> <span data-ttu-id="829c8-144">In caso contrario, si tratta di un oggetto [SWbemNamedValueSet](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="829c8-144">Otherwise, this is an [SWbemNamedValueSet](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="829c8-145">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="829c8-145">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="829c8-146">*objWbemAsyncContext* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="829c8-146">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="829c8-147">Si tratta di un oggetto [SWbemNamedValueSet](swbemnamedvalueset.md) che restituisce al sink di oggetto per identificare l'origine della chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="829c8-147">This is an [SWbemNamedValueSet](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="829c8-148">Utilizzare questo parametro se si eseguono più chiamate asincrone utilizzando lo stesso sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="829c8-148">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="829c8-149">Per usare questo parametro, creare un oggetto SWbemNamedValueSet e usare il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona che si sta effettuando.</span><span class="sxs-lookup"><span data-stu-id="829c8-149">To use this parameter, create an SWbemNamedValueSet object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="829c8-150">Questo oggetto SWbemNamedValueSet viene restituito al sink di oggetto e l'origine della chiamata può essere estratta tramite il metodo [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="829c8-150">This SWbemNamedValueSet object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="829c8-151">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="829c8-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="829c8-152">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="829c8-152">Return value</span></span>

<span data-ttu-id="829c8-153">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="829c8-153">This method does not return a value.</span></span> <span data-ttu-id="829c8-154">In caso di esito positivo, il sink riceve un evento [**OnObjectReady**](swbemsink-onobjectready.md) per ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="829c8-154">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="829c8-155">Dopo l'ultima istanza, il sink di oggetto riceve un evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="829c8-155">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="829c8-156">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="829c8-156">Error codes</span></span>

<span data-ttu-id="829c8-157">Dopo il completamento del metodo **ReferencesAsync \_** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="829c8-157">After the completion of the **ReferencesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="829c8-158">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="829c8-158">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="829c8-159">L'utente corrente non dispone delle autorizzazioni necessarie per visualizzare una o più classi restituite dalla chiamata.</span><span class="sxs-lookup"><span data-stu-id="829c8-159">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="829c8-160">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="829c8-160">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="829c8-161">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="829c8-161">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="829c8-162">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="829c8-162">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="829c8-163">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="829c8-163">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="829c8-164">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="829c8-164">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="829c8-165">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="829c8-165">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="829c8-166">Commenti</span><span class="sxs-lookup"><span data-stu-id="829c8-166">Remarks</span></span>

<span data-ttu-id="829c8-167">Questa chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="829c8-167">This call returns immediately.</span></span> <span data-ttu-id="829c8-168">Gli oggetti e lo stato richiesti vengono restituiti al chiamante tramite callback recapitati al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="829c8-168">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="829c8-169">Per elaborare ogni oggetto all'arrivo, creare un *objWbemSink*. Subroutine dell'evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="829c8-169">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="829c8-170">Dopo la restituzione di tutti gli oggetti, è possibile eseguire l'elaborazione finale nell'implementazione di *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="829c8-170">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="829c8-171">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="829c8-171">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="829c8-172">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="829c8-172">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="829c8-173">Per eliminare i rischi, usare la comunicazione semisincrono o la comunicazione sincrona.</span><span class="sxs-lookup"><span data-stu-id="829c8-173">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="829c8-174">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="829c8-174">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="829c8-175">Per ulteriori informazioni sui riferimenti della query WQL associata, delle istanze di origine e degli oggetti di associazione, vedere associazioners [of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="829c8-175">For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="829c8-176">Requisiti</span><span class="sxs-lookup"><span data-stu-id="829c8-176">Requirements</span></span>



| <span data-ttu-id="829c8-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="829c8-177">Requirement</span></span> | <span data-ttu-id="829c8-178">Valore</span><span class="sxs-lookup"><span data-stu-id="829c8-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="829c8-179">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="829c8-179">Minimum supported client</span></span><br/> | <span data-ttu-id="829c8-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="829c8-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="829c8-181">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="829c8-181">Minimum supported server</span></span><br/> | <span data-ttu-id="829c8-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="829c8-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="829c8-183">Intestazione</span><span class="sxs-lookup"><span data-stu-id="829c8-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="829c8-184"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="829c8-184"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="829c8-185">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="829c8-185">Type library</span></span><br/>             | <dl> <span data-ttu-id="829c8-186"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="829c8-186"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="829c8-187">DLL</span><span class="sxs-lookup"><span data-stu-id="829c8-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="829c8-188"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="829c8-188"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="829c8-189">CLSID</span><span class="sxs-lookup"><span data-stu-id="829c8-189">CLSID</span></span><br/>                    | <span data-ttu-id="829c8-190">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="829c8-190">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="829c8-191">IID</span><span class="sxs-lookup"><span data-stu-id="829c8-191">IID</span></span><br/>                      | <span data-ttu-id="829c8-192">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="829c8-192">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="829c8-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="829c8-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="829c8-194">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="829c8-194">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="829c8-195">**SWbemObject. Associator\_**</span><span class="sxs-lookup"><span data-stu-id="829c8-195">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="829c8-196">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="829c8-196">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="829c8-197">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="829c8-197">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> <dt>

[<span data-ttu-id="829c8-198">**SWbemServices. ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="829c8-198">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)
</dt> </dl>

 

