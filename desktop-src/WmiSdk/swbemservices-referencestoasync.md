---
description: Restituisce tutte le classi o le istanze di associazione che fanno riferimento a una classe o a un'istanza di origine specifica.
ms.assetid: 2ad66ea1-b8f0-4b6b-b68f-29496afbe4bf
ms.tgt_platform: multiple
title: Metodo SWbemServices. ReferencesToAsync (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 64a8b9b336a1e7aa6007b17d2e878f1ace5e6163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309778"
---
# <a name="swbemservicesreferencestoasync-method"></a><span data-ttu-id="d6c36-103">SWbemServices. ReferencesToAsync, metodo</span><span class="sxs-lookup"><span data-stu-id="d6c36-103">SWbemServices.ReferencesToAsync method</span></span>

<span data-ttu-id="d6c36-104">Il metodo **ReferencesToAsync** dell'oggetto [**SWbemServices**](swbemservices.md) restituisce tutte le classi o le istanze di associazione che fanno riferimento a una classe di origine o a un'istanza specifica.</span><span class="sxs-lookup"><span data-stu-id="d6c36-104">The **ReferencesToAsync** method of the [**SWbemServices**](swbemservices.md) object returns all association classes or instances that refer to a specific source class or instance.</span></span> <span data-ttu-id="d6c36-105">Questo metodo esegue la stessa funzione eseguita dai [riferimenti della](references-of-statement.md) query WQL.</span><span class="sxs-lookup"><span data-stu-id="d6c36-105">This method performs the same function that the [REFERENCES OF](references-of-statement.md) WQL query performs.</span></span>

<span data-ttu-id="d6c36-106">Per ulteriori informazioni sulla modalità asincrona, vedere la pagina relativa alla [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="d6c36-106">For more information about the asynchronous mode, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="d6c36-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d6c36-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d6c36-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6c36-108">Syntax</span></span>


```VB
SWbemServices.ReferencesToAsync( _
  ByVal ObjWbemSink, _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d6c36-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d6c36-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6c36-110">*ObjWbemSink*</span><span class="sxs-lookup"><span data-stu-id="d6c36-110">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="d6c36-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d6c36-111">Required.</span></span> <span data-ttu-id="d6c36-112">Sink di oggetto che riceve gli oggetti in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="d6c36-112">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="d6c36-113">Creare un oggetto [**SWbemSink**](swbemsink.md) per ricevere gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="d6c36-113">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="d6c36-114">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="d6c36-114">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="d6c36-115">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d6c36-115">Required.</span></span> <span data-ttu-id="d6c36-116">Stringa che contiene il percorso dell'oggetto dell'origine per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="d6c36-116">String that contains the object path of the source for this method.</span></span> <span data-ttu-id="d6c36-117">Per ulteriori informazioni, vedere la pagina relativa alla [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="d6c36-117">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6c36-118">*strResultClass* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d6c36-118">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c36-119">Stringa che contiene un nome di classe.</span><span class="sxs-lookup"><span data-stu-id="d6c36-119">String that contains a class name.</span></span> <span data-ttu-id="d6c36-120">Se specificato, questo parametro indica che gli oggetti di associazione restituiti devono appartenere o essere derivati dalla classe specificata in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d6c36-120">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class that is specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d6c36-121">*strRole* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d6c36-121">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c36-122">Stringa che contiene un nome di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d6c36-122">String that contains a property name.</span></span> <span data-ttu-id="d6c36-123">Se specificato, questo parametro indica che gli oggetti di associazione restituiti devono essere limitati a quelli in cui l'oggetto di origine gioca un ruolo specifico.</span><span class="sxs-lookup"><span data-stu-id="d6c36-123">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="d6c36-124">Il ruolo è definito dal nome di una proprietà di riferimento specificata di un'associazione.</span><span class="sxs-lookup"><span data-stu-id="d6c36-124">The role is defined by the name of a specified reference property of an association.</span></span>

</dd> <dt>

<span data-ttu-id="d6c36-125">*bClassesOnly* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d6c36-125">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c36-126">Valore booleano che indica se deve essere restituito un elenco di nomi di classe anziché le istanze effettive delle classi.</span><span class="sxs-lookup"><span data-stu-id="d6c36-126">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="d6c36-127">Queste sono le classi a cui appartengono gli oggetti Association.</span><span class="sxs-lookup"><span data-stu-id="d6c36-127">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="d6c36-128">Il valore predefinito per questo parametro è **false**.</span><span class="sxs-lookup"><span data-stu-id="d6c36-128">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d6c36-129">*bSchemaOnly* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d6c36-129">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c36-130">Valore booleano che indica se la query viene applicata o meno allo schema anziché ai dati.</span><span class="sxs-lookup"><span data-stu-id="d6c36-130">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="d6c36-131">Il valore predefinito per questo parametro è **false**.</span><span class="sxs-lookup"><span data-stu-id="d6c36-131">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="d6c36-132">Può essere impostato su **true** solo se il parametro *strObjectPath* specifica il percorso dell'oggetto di una classe.</span><span class="sxs-lookup"><span data-stu-id="d6c36-132">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="d6c36-133">Se impostato su **true**, il set di endpoint restituiti rappresenta le classi associate alla classe di origine nello schema.</span><span class="sxs-lookup"><span data-stu-id="d6c36-133">When set to **TRUE**, the set of returned endpoints represents classes that are associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="d6c36-134">*strRequiredQualifier* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d6c36-134">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c36-135">Stringa che contiene un nome di qualificatore.</span><span class="sxs-lookup"><span data-stu-id="d6c36-135">String that contains a qualifier name.</span></span> <span data-ttu-id="d6c36-136">Se specificato, questo parametro indica che gli oggetti Association restituiti devono includere il qualificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="d6c36-136">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="d6c36-137">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d6c36-137">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c36-138">Integer che specifica flag aggiuntivi per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d6c36-138">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="d6c36-139">Il valore predefinito per questo parametro è **wbemFlagBidirectional**.</span><span class="sxs-lookup"><span data-stu-id="d6c36-139">The default for this parameter is **wbemFlagBidirectional**.</span></span> <span data-ttu-id="d6c36-140">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d6c36-140">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="d6c36-141"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="d6c36-141"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="d6c36-142">Fa in modo che le chiamate asincrone inviino gli aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d6c36-142">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="d6c36-143"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="d6c36-143"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d6c36-144">Impedisce alle chiamate asincrone di inviare aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d6c36-144">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="d6c36-145"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="d6c36-145"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="d6c36-146">Fa in modo che Strumentazione gestione Windows (WMI) restituisca i dati di modifica della classe insieme alla definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="d6c36-146">Causes Windows Management Instrumentation (WMI) to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="d6c36-147">Per ulteriori informazioni, vedere la pagina relativa alla [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="d6c36-147">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d6c36-148">*objWbemNamedValueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d6c36-148">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c36-149">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="d6c36-149">Typically, this is undefined.</span></span> <span data-ttu-id="d6c36-150">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="d6c36-150">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="d6c36-151">Un provider che supporta o richiede informazioni sul contesto deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="d6c36-151">A provider that supports or requires context information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="d6c36-152">*objWbemAsyncContext* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d6c36-152">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c36-153">Si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink di oggetto per identificare l'origine della chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="d6c36-153">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="d6c36-154">Utilizzare questo parametro per effettuare più chiamate asincrone utilizzando lo stesso sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="d6c36-154">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="d6c36-155">Per usare questo parametro, creare un oggetto **SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona che si sta effettuando.</span><span class="sxs-lookup"><span data-stu-id="d6c36-155">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="d6c36-156">Questo oggetto **SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta tramite il metodo [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="d6c36-156">This **SWbemNamedValueSet** object is returned to the object sink, and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="d6c36-157">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="d6c36-157">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6c36-158">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d6c36-158">Return value</span></span>

<span data-ttu-id="d6c36-159">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d6c36-159">This method does not return a value.</span></span> <span data-ttu-id="d6c36-160">In caso di esito positivo, il sink riceve un evento [**OnObjectReady**](swbemsink-onobjectready.md) per ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="d6c36-160">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="d6c36-161">Dopo l'ultima istanza, il sink di oggetto riceve un evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="d6c36-161">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d6c36-162">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d6c36-162">Error codes</span></span>

<span data-ttu-id="d6c36-163">Dopo il completamento del metodo **ReferencesToAsync** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="d6c36-163">After the completion of the **ReferencesToAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="d6c36-164">Una raccolta restituita con zero elementi non è un errore.</span><span class="sxs-lookup"><span data-stu-id="d6c36-164">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="d6c36-165">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="d6c36-165">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="d6c36-166">L'utente corrente non dispone dell'autorizzazione per visualizzare una o più classi restituite dalla chiamata.</span><span class="sxs-lookup"><span data-stu-id="d6c36-166">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="d6c36-167">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d6c36-167">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d6c36-168">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="d6c36-168">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d6c36-169">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d6c36-169">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d6c36-170">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="d6c36-170">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="d6c36-171">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d6c36-171">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d6c36-172">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d6c36-172">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6c36-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="d6c36-173">Remarks</span></span>

<span data-ttu-id="d6c36-174">Questa chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="d6c36-174">This call returns immediately.</span></span> <span data-ttu-id="d6c36-175">Gli oggetti e lo stato richiesti vengono restituiti al chiamante tramite callback recapitati al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="d6c36-175">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="d6c36-176">Per elaborare ogni oggetto quando restituisce, creare un *objWbemSink*. Subroutine dell'evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="d6c36-176">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="d6c36-177">Dopo la restituzione di tutti gli oggetti, è possibile eseguire l'elaborazione finale nell'implementazione di *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="d6c36-177">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="d6c36-178">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="d6c36-178">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="d6c36-179">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d6c36-179">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="d6c36-180">Per eliminare i rischi, vedere [impostazione della sicurezza per una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="d6c36-180">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6c36-181">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6c36-181">Requirements</span></span>



| <span data-ttu-id="d6c36-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6c36-182">Requirement</span></span> | <span data-ttu-id="d6c36-183">Valore</span><span class="sxs-lookup"><span data-stu-id="d6c36-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c36-184">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6c36-184">Minimum supported client</span></span><br/> | <span data-ttu-id="d6c36-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6c36-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d6c36-186">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6c36-186">Minimum supported server</span></span><br/> | <span data-ttu-id="d6c36-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6c36-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d6c36-188">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d6c36-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6c36-189"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6c36-189"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6c36-190">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d6c36-190">Type library</span></span><br/>             | <dl> <span data-ttu-id="d6c36-191"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d6c36-191"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d6c36-192">DLL</span><span class="sxs-lookup"><span data-stu-id="d6c36-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6c36-193"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6c36-193"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d6c36-194">CLSID</span><span class="sxs-lookup"><span data-stu-id="d6c36-194">CLSID</span></span><br/>                    | <span data-ttu-id="d6c36-195">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="d6c36-195">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="d6c36-196">IID</span><span class="sxs-lookup"><span data-stu-id="d6c36-196">IID</span></span><br/>                      | <span data-ttu-id="d6c36-197">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="d6c36-197">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="d6c36-198">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6c36-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6c36-199">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="d6c36-199">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="d6c36-200">**SWbemObject. Associator\_**</span><span class="sxs-lookup"><span data-stu-id="d6c36-200">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="d6c36-201">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="d6c36-201">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="d6c36-202">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="d6c36-202">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

