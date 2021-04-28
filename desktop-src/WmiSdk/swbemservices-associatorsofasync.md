---
description: 'Metodo SWbemServices.AssociatersOfAsync: restituisce una raccolta di oggetti (classi o istanze) denominati endpoint associati a un oggetto specificato.'
ms.assetid: 3969d90f-d39c-40f1-9328-fc1afbaa53b1
ms.tgt_platform: multiple
title: Metodo SWbemServices.AssociatorsOfAsync (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4b16eed97c891b4b4f5bd283496868d99f9e0fbc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103669"
---
# <a name="swbemservicesassociatorsofasync-method"></a><span data-ttu-id="d4eb2-103">Metodo SWbemServices.AssociatorsOfAsync</span><span class="sxs-lookup"><span data-stu-id="d4eb2-103">SWbemServices.AssociatorsOfAsync method</span></span>

<span data-ttu-id="d4eb2-104">Il **metodo AssociatorsOfAsync** dell'oggetto [**SWbemServices**](swbemservices.md) restituisce una raccolta di oggetti (classi o istanze) denominati endpoint associati a un oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-104">The **AssociatorsOfAsync** method of the [**SWbemServices**](swbemservices.md) object returns a collection of objects (classes or instances) called endpoints that are associated with a specified object.</span></span> <span data-ttu-id="d4eb2-105">La chiamata a **AssociatorsOfAsync** restituisce immediatamente e i risultati e lo stato vengono restituiti al chiamante tramite eventi recapitati al sink specificato in *objWbemSink.*</span><span class="sxs-lookup"><span data-stu-id="d4eb2-105">The call to **AssociatorsOfAsync** returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="d4eb2-106">Per gestire ogni oggetto restituito, creare *un oggetto objWbemSink.* [**Gestore dell'evento OnObjectReady.**](swbemsink-onobjectready.md)</span><span class="sxs-lookup"><span data-stu-id="d4eb2-106">To handle each returned object, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event handler.</span></span>

<span data-ttu-id="d4eb2-107">Dopo l'arrivo di tutti gli oggetti, l'elaborazione viene eseguita in *objWbemSink.* [**Evento OnCompleted.**](swbemsink-oncompleted.md)</span><span class="sxs-lookup"><span data-stu-id="d4eb2-107">After all the objects arrive, processing is done in the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span> <span data-ttu-id="d4eb2-108">Questo metodo esegue la stessa funzione eseguita dalla query ASSOCIATORS OF WQL.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-108">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span> <span data-ttu-id="d4eb2-109">Per altre informazioni sulla creazione di un sink, vedere [Ricezione di un evento WMI.](receiving-a-wmi-event.md)</span><span class="sxs-lookup"><span data-stu-id="d4eb2-109">For more information about creating a sink, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="d4eb2-110">Il metodo viene chiamato in modalità asincrona.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-110">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="d4eb2-111">Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="d4eb2-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="d4eb2-112">Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d4eb2-112">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d4eb2-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4eb2-113">Syntax</span></span>


```VB
SWbemServices.AssociatorsOfAsync( _
  ByVal objWbemSink, _
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
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d4eb2-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4eb2-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4eb2-115">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="d4eb2-115">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="d4eb2-116">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-116">Required.</span></span> <span data-ttu-id="d4eb2-117">Sink dell'oggetto che riceve gli oggetti in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-117">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="d4eb2-118">Creare un [**oggetto SWbemSink**](swbemsink.md) per ricevere gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-118">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="d4eb2-119">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="d4eb2-119">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="d4eb2-120">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-120">Required.</span></span> <span data-ttu-id="d4eb2-121">Stringa che contiene il percorso dell'oggetto della classe o dell'istanza di origine.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-121">String that contains the object path of the source class or instance.</span></span> <span data-ttu-id="d4eb2-122">Per altre informazioni, vedere [Descrizione del percorso di un oggetto WMI.](describing-the-location-of-a-wmi-object.md)</span><span class="sxs-lookup"><span data-stu-id="d4eb2-122">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4eb2-123">*strAssocClass* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d4eb2-123">*strAssocClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eb2-124">Stringa che contiene una classe di associazione.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-124">String that contains an association class.</span></span> <span data-ttu-id="d4eb2-125">Se specificato, questo parametro indica che gli endpoint restituiti devono essere associati all'origine tramite la classe di associazione specificata o una classe derivata da questa classe di associazione.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-125">When specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="d4eb2-126">*strResultClass* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d4eb2-126">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eb2-127">Stringa che contiene un nome di classe.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-127">String that contains a class name.</span></span> <span data-ttu-id="d4eb2-128">Se specificato, questo parametro facoltativo indica che gli endpoint restituiti devono appartenere o essere derivati dalla classe specificata in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-128">If specified, this optional parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d4eb2-129">*strResultRole* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d4eb2-129">*strResultRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eb2-130">Stringa che contiene il nome di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-130">String that contains a property name.</span></span> <span data-ttu-id="d4eb2-131">Se specificato, questo parametro indica che gli endpoint restituiti devono svolgere un ruolo specifico nella relativa associazione all'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-131">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="d4eb2-132">Il ruolo è definito dal nome di una proprietà specificata (che deve essere una proprietà di riferimento) di un'associazione.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-132">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="d4eb2-133">*strRole* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d4eb2-133">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eb2-134">Stringa che contiene il nome di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-134">String that contains a property name.</span></span> <span data-ttu-id="d4eb2-135">Se specificato, questo parametro indica che gli endpoint restituiti devono partecipare a un'associazione con l'oggetto di origine in cui l'oggetto di origine svolge un ruolo specifico.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-135">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="d4eb2-136">Il ruolo è definito dal nome di una proprietà specificata (che deve essere una proprietà di riferimento) di un'associazione.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-136">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="d4eb2-137">*bClassesOnly* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d4eb2-137">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eb2-138">Valore booleano che indica se deve essere restituito un elenco di nomi di classe anziché istanze effettive delle classi.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-138">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="d4eb2-139">Si tratta delle classi a cui appartengono le istanze dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-139">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="d4eb2-140">Il valore predefinito per questo parametro è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="d4eb2-140">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d4eb2-141">*bSchemaOnly* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d4eb2-141">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eb2-142">Valore booleano che indica se la query si applica allo schema anziché ai dati.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-142">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="d4eb2-143">Il valore predefinito per questo parametro è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="d4eb2-143">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="d4eb2-144">Può essere impostato su **TRUE** solo se il *parametro strObjectPath* specifica il percorso dell'oggetto di una classe.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-144">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="d4eb2-145">Se impostato su **TRUE,** il set di endpoint restituiti rappresenta le classi che sono adeguatamente associate alla classe di origine nello schema.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-145">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="d4eb2-146">*strRequiredAssocQualifier* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d4eb2-146">*strRequiredAssocQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eb2-147">Stringa che contiene un nome di qualificatore.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-147">String that contains a qualifier name.</span></span> <span data-ttu-id="d4eb2-148">Se specificato, questo parametro indica che gli endpoint restituiti devono essere associati all'oggetto di origine tramite una classe di associazione che include il qualificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-148">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="d4eb2-149">*strRequiredQualifier* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d4eb2-149">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eb2-150">Stringa che contiene un nome di qualificatore.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-150">String that contains a qualifier name.</span></span> <span data-ttu-id="d4eb2-151">Se specificato, questo parametro indica che gli endpoint restituiti devono includere il qualificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-151">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="d4eb2-152">*iFlags* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d4eb2-152">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eb2-153">Intero che specifica i flag aggiuntivi per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-153">Integer that specifies the additional flags to the operation.</span></span> <span data-ttu-id="d4eb2-154">Il valore predefinito per questo parametro **è wbemFlagDontSendStatus.**</span><span class="sxs-lookup"><span data-stu-id="d4eb2-154">The default for this parameter is **wbemFlagDontSendStatus**.</span></span> <span data-ttu-id="d4eb2-155">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-155">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="d4eb2-156"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus\*\*\*\* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="d4eb2-156"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="d4eb2-157">Fa sì che le chiamate asincrone inviino aggiornamenti di stato al [**gestore eventi OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-157">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="d4eb2-158"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="d4eb2-158"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d4eb2-159">Impedisce alle chiamate asincrone di inviare aggiornamenti dello stato al [**gestore eventi OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-159">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="d4eb2-160"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="d4eb2-160"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="d4eb2-161">Fa in modo che WMI restituirà i dati di modifica della classe insieme alla definizione della classe di base.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-161">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="d4eb2-162">Per altre informazioni sui qualificatori modificati, vedere [Localizing WMI Class Information](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="d4eb2-162">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d4eb2-163">*objWbemNamedValueSet* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d4eb2-163">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eb2-164">In genere non è definito.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-164">Typically, this is undefined.</span></span> <span data-ttu-id="d4eb2-165">In caso contrario, si tratta di un [**oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni di contesto che possono essere usate dal provider che sta servo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-165">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="d4eb2-166">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-166">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="d4eb2-167">*objWbemAsyncContext* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d4eb2-167">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eb2-168">Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink dell'oggetto per identificare l'origine della chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-168">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="d4eb2-169">Usare questo parametro se si effettuano più chiamate asincrone usando lo stesso sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-169">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="d4eb2-170">Per usare questo parametro, creare un **oggetto SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-170">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="d4eb2-171">Questo **oggetto SWbemNamedValueSet** viene restituito al sink dell'oggetto e l'origine della chiamata può essere estratta usando il metodo [**SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md)</span><span class="sxs-lookup"><span data-stu-id="d4eb2-171">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="d4eb2-172">Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="d4eb2-172">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4eb2-173">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4eb2-173">Return value</span></span>

<span data-ttu-id="d4eb2-174">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-174">This method does not return a value.</span></span> <span data-ttu-id="d4eb2-175">Se ha esito positivo, il sink riceve un [**evento OnObjectReady**](swbemsink-onobjectready.md) per ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-175">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="d4eb2-176">Dopo l'ultima istanza, il sink dell'oggetto riceve un [**evento OnCompleted.**](swbemsink-oncompleted.md)</span><span class="sxs-lookup"><span data-stu-id="d4eb2-176">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d4eb2-177">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d4eb2-177">Error codes</span></span>

<span data-ttu-id="d4eb2-178">Dopo il completamento del **metodo AssociatorsOfAsync,** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-178">After the completion of the **AssociatorsOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d4eb2-179">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="d4eb2-179">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="d4eb2-180">L'utente corrente non dispone dell'autorizzazione per visualizzare una o più classi restituite dalla chiamata.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-180">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="d4eb2-181">**wbemErrFailed** - 2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d4eb2-181">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d4eb2-182">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-182">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d4eb2-183">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d4eb2-183">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d4eb2-184">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-184">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="d4eb2-185">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d4eb2-185">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d4eb2-186">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-186">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d4eb2-187">**wbemErrNotFound** - 2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="d4eb2-187">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="d4eb2-188">L'elemento richiesto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-188">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4eb2-189">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4eb2-189">Remarks</span></span>

<span data-ttu-id="d4eb2-190">Questa chiamata restituisce immediatamente .</span><span class="sxs-lookup"><span data-stu-id="d4eb2-190">This call returns immediately.</span></span> <span data-ttu-id="d4eb2-191">Gli oggetti e lo stato richiesti vengono restituiti al chiamante tramite callback recapitati al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-191">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="d4eb2-192">Per elaborare ogni oggetto quando viene restituito, creare *un objWbemSink*. Subroutine dell'evento [**OnObjectReady.**](swbemsink-onobjectready.md)</span><span class="sxs-lookup"><span data-stu-id="d4eb2-192">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="d4eb2-193">Dopo aver restituito tutti gli oggetti, è possibile eseguire l'elaborazione finale nell'implementazione di *objWbemSink*. [**Evento OnCompleted.**](swbemsink-oncompleted.md)</span><span class="sxs-lookup"><span data-stu-id="d4eb2-193">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="d4eb2-194">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-194">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="d4eb2-195">Ciò comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-195">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="d4eb2-196">Per eliminare i rischi, vedere [Impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="d4eb2-196">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="d4eb2-197">Usare il *parametro objWbemAsyncContext* negli script per verificare l'origine di una chiamata.</span><span class="sxs-lookup"><span data-stu-id="d4eb2-197">Use the *objWbemAsyncContext* parameter in scripts to verify the source of a call.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4eb2-198">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4eb2-198">Requirements</span></span>



| <span data-ttu-id="d4eb2-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4eb2-199">Requirement</span></span> | <span data-ttu-id="d4eb2-200">Valore</span><span class="sxs-lookup"><span data-stu-id="d4eb2-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4eb2-201">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4eb2-201">Minimum supported client</span></span><br/> | <span data-ttu-id="d4eb2-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4eb2-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d4eb2-203">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4eb2-203">Minimum supported server</span></span><br/> | <span data-ttu-id="d4eb2-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4eb2-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d4eb2-205">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4eb2-205">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4eb2-206"><dt>Wbemdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="d4eb2-206"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4eb2-207">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d4eb2-207">Type library</span></span><br/>             | <dl> <span data-ttu-id="d4eb2-208"><dt>Wbemdisp.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d4eb2-208"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d4eb2-209">DLL</span><span class="sxs-lookup"><span data-stu-id="d4eb2-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4eb2-210"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4eb2-210"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d4eb2-211">CLSID</span><span class="sxs-lookup"><span data-stu-id="d4eb2-211">CLSID</span></span><br/>                    | <span data-ttu-id="d4eb2-212">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="d4eb2-212">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="d4eb2-213">IID</span><span class="sxs-lookup"><span data-stu-id="d4eb2-213">IID</span></span><br/>                      | <span data-ttu-id="d4eb2-214">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="d4eb2-214">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="d4eb2-215">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4eb2-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4eb2-216">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="d4eb2-216">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="d4eb2-217">**SWbemObject.Associators\_**</span><span class="sxs-lookup"><span data-stu-id="d4eb2-217">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="d4eb2-218">**SWbemObject.AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="d4eb2-218">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)
</dt> <dt>

[<span data-ttu-id="d4eb2-219">**SWbemObject.References\_**</span><span class="sxs-lookup"><span data-stu-id="d4eb2-219">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="d4eb2-220">**SWbemObject.ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="d4eb2-220">**SWbemObject.ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)
</dt> <dt>

[<span data-ttu-id="d4eb2-221">**SWbemServices.ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="d4eb2-221">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> <dt>

[<span data-ttu-id="d4eb2-222">**SWbemServices.ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="d4eb2-222">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)
</dt> </dl>

 

