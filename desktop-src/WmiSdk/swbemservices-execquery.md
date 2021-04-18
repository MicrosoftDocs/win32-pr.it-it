---
description: Esegue una query per il recupero di oggetti.
ms.assetid: 06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f
ms.tgt_platform: multiple
title: Metodo SWbemServices.ExecQuery (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQuery
- ISWbemServices.ExecQuery
- ISWbemServices.ExecQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2f3a894681bafc71de34ae7722b985494ef80b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313163"
---
# <a name="swbemservicesexecquery-method"></a><span data-ttu-id="23982-103">Metodo cQuery SWbemServices.Exe</span><span class="sxs-lookup"><span data-stu-id="23982-103">SWbemServices.ExecQuery method</span></span>

<span data-ttu-id="23982-104">Il metodo **ExecQuery** dell'oggetto [**SWbemServices**](swbemservices.md) esegue una query per recuperare gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="23982-104">The **ExecQuery** method of the [**SWbemServices**](swbemservices.md) object executes a query to retrieve objects.</span></span> <span data-ttu-id="23982-105">Questi oggetti sono disponibili tramite la raccolta [**SWbemObjectSet**](swbemobjectset.md) restituita.</span><span class="sxs-lookup"><span data-stu-id="23982-105">These objects are available through the returned [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span>

<span data-ttu-id="23982-106">Questo metodo viene chiamato in modalità semisincrono.</span><span class="sxs-lookup"><span data-stu-id="23982-106">This method is called in the semisynchronous mode.</span></span> <span data-ttu-id="23982-107">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="23982-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="23982-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="23982-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="23982-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23982-109">Syntax</span></span>


```VB
objWbemObjectSet = .ExecQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="23982-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="23982-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23982-111">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="23982-111">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="23982-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="23982-112">Required.</span></span> <span data-ttu-id="23982-113">Stringa che contiene il testo della query.</span><span class="sxs-lookup"><span data-stu-id="23982-113">String that contains the text of the query.</span></span> <span data-ttu-id="23982-114">Questo parametro non può essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="23982-114">This parameter cannot be blank.</span></span> <span data-ttu-id="23982-115">Per ulteriori informazioni sulla creazione di stringhe di query WMI, vedere [esecuzione di query con WQL](querying-with-wql.md) e informazioni di riferimento su [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="23982-115">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="23982-116">*strQueryLanguage* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="23982-116">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="23982-117">Stringa che contiene il linguaggio di query da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="23982-117">String that contains the query language to be used.</span></span> <span data-ttu-id="23982-118">Se specificato, questo valore deve essere "WQL".</span><span class="sxs-lookup"><span data-stu-id="23982-118">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="23982-119">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="23982-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="23982-120">Integer che determina il comportamento della query e determina se la chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="23982-120">Integer that determines the behavior of the query and determines whether this call returns immediately.</span></span> <span data-ttu-id="23982-121">Il valore predefinito per questo parametro è **wbemFlagReturnImmediately**.</span><span class="sxs-lookup"><span data-stu-id="23982-121">The default value for this parameter is **wbemFlagReturnImmediately**.</span></span> <span data-ttu-id="23982-122">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="23982-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="23982-123"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="23982-123"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="23982-124">Causa la restituzione di un enumeratore di sola trasmissione.</span><span class="sxs-lookup"><span data-stu-id="23982-124">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="23982-125">Gli enumeratori di solo avanzamento sono in genere molto più veloci e utilizzano meno memoria rispetto agli enumeratori convenzionali, ma non consentono chiamate a [**SWbemObject \_ . Clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="23982-125">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="23982-126"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="23982-126"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="23982-127">Causa la conservazione dei puntatori agli oggetti dell'enumerazione da parte di WMI finché il client non rilascia l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="23982-127">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="23982-128"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="23982-128"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="23982-129">Causa la restituzione immediata della chiamata.</span><span class="sxs-lookup"><span data-stu-id="23982-129">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="23982-130"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="23982-130"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="23982-131">Causa il blocco della chiamata fino al completamento della query.</span><span class="sxs-lookup"><span data-stu-id="23982-131">Causes this call to block until the query is complete.</span></span> <span data-ttu-id="23982-132">Questo flag chiama il metodo in modalità sincrona.</span><span class="sxs-lookup"><span data-stu-id="23982-132">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span data-ttu-id="23982-133"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype \* \* \* \* (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="23982-133"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>\*\*\*\*wbemQueryFlagPrototype\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="23982-134">Usato per la realizzazione di prototipi.</span><span class="sxs-lookup"><span data-stu-id="23982-134">Used for prototyping.</span></span> <span data-ttu-id="23982-135">Questo flag interrompe l'esecuzione della query e restituisce un oggetto simile a un oggetto risultato tipico.</span><span class="sxs-lookup"><span data-stu-id="23982-135">This flag stops the query from happening and returns an object that looks like a typical result object.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="23982-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="23982-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="23982-137">Causa la restituzione dei dati di modifica della classe da parte di WMI con la definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="23982-137">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="23982-138">Per ulteriori informazioni, vedere la pagina relativa alla [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="23982-138">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="23982-139">*objWbemNamedValueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="23982-139">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="23982-140">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="23982-140">Typically, this is undefined.</span></span> <span data-ttu-id="23982-141">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="23982-141">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="23982-142">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="23982-142">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23982-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23982-143">Return value</span></span>

<span data-ttu-id="23982-144">Se non si verificano errori, questo metodo restituisce un oggetto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="23982-144">If no error occurs, this method returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="23982-145">Si tratta di una raccolta di oggetti che contiene il set di risultati della query.</span><span class="sxs-lookup"><span data-stu-id="23982-145">This is an object collection that contains the result set of the query.</span></span> <span data-ttu-id="23982-146">Il chiamante può esaminare la raccolta usando l'implementazione delle raccolte per il linguaggio di programmazione in uso.</span><span class="sxs-lookup"><span data-stu-id="23982-146">The caller can examine the collection using the implementation of collections for the programming language you are using.</span></span> <span data-ttu-id="23982-147">Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="23982-147">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="23982-148">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="23982-148">Error codes</span></span>

<span data-ttu-id="23982-149">Dopo il completamento del metodo **ExecQuery** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="23982-149">After the completion of the **ExecQuery** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object can contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="23982-150">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="23982-150">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="23982-151">L'utente corrente non dispone dell'autorizzazione per visualizzare il set di risultati.</span><span class="sxs-lookup"><span data-stu-id="23982-151">Current user does not have the permission to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="23982-152">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="23982-152">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="23982-153">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="23982-153">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="23982-154">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="23982-154">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="23982-155">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="23982-155">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="23982-156">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="23982-156">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="23982-157">Sintassi di query non valida.</span><span class="sxs-lookup"><span data-stu-id="23982-157">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="23982-158">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="23982-158">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="23982-159">Il linguaggio di query richiesto non è supportato.</span><span class="sxs-lookup"><span data-stu-id="23982-159">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="23982-160">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="23982-160">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="23982-161">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="23982-161">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23982-162">Commenti</span><span class="sxs-lookup"><span data-stu-id="23982-162">Remarks</span></span>

<span data-ttu-id="23982-163">**ExecQuery** è una delle chiamate più diffuse per recuperare le informazioni WMI.</span><span class="sxs-lookup"><span data-stu-id="23982-163">**ExecQuery** is one of the most commonly-used calls to retrieve WMI information.</span></span> <span data-ttu-id="23982-164">Una chiamata standard a **ExecQuery** ha un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="23982-164">A standard call to **ExecQuery** looks like the following:</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```



<span data-ttu-id="23982-165">Si noti che si crea l'oggetto [**SWbemServices**](swbemservices.md) con un moniker che rappresenta lo spazio dei nomi e la sicurezza appropriati, quindi si effettua la chiamata **ExecQuery** tramite il servizio.</span><span class="sxs-lookup"><span data-stu-id="23982-165">Note that you create the [**SWbemServices**](swbemservices.md) object with a moniker that represents the appropriate namespace and security, then make the **ExecQuery** call through the service.</span></span> <span data-ttu-id="23982-166">Per una descrizione più completa, vedere [creazione di uno script WMI](creating-a-wmi-script.md) ed [enumerazione di WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="23982-166">For a more complete discussion, see [Creating a WMI Script](creating-a-wmi-script.md) and [Enumerating WMI](enumerating-wmi.md).</span></span>

<span data-ttu-id="23982-167">Come il metodo [**InstancesOf**](swbemservices-instancesof.md) , il metodo **ExecQuery** restituisce sempre una raccolta [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="23982-167">Like the [**InstancesOf**](swbemservices-instancesof.md) method, the **ExecQuery** method always returns an [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span> <span data-ttu-id="23982-168">Pertanto, lo script WMI deve enumerare la raccolta restituita da ExecQuery per accedere a ogni istanza di risorsa gestita nella raccolta, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="23982-168">Thus your WMI script must enumerate the collection ExecQuery returns in order to access each managed resource instance in the collection, as shown here:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
   ("SELECT * FROM Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="23982-169">Altri metodi [**SWbemServices**](swbemservices.md) che restituiscono [**un SWbemObjectSet**](swbemobjectset.md) includono [**AssociatorsOf**](swbemservices-associatorsof.md), [**ReferencesTo**](swbemservices-referencesto.md)e [**SubclassesOf**](swbemservices-subclassesof.md).</span><span class="sxs-lookup"><span data-stu-id="23982-169">Other [**SWbemServices**](swbemservices.md) methods that return an [**SWbemObjectSet**](swbemobjectset.md) include [**AssociatorsOf**](swbemservices-associatorsof.md), [**ReferencesTo**](swbemservices-referencesto.md), and [**SubclassesOf**](swbemservices-subclassesof.md).</span></span>

<span data-ttu-id="23982-170">Non si tratta di un errore perché la query restituisca un set di risultati vuoto.</span><span class="sxs-lookup"><span data-stu-id="23982-170">It is not an error for the query to return an empty result set.</span></span> <span data-ttu-id="23982-171">Il metodo **ExecQuery** restituisce le proprietà chiave se la proprietà Key è richiesta nell'argomento *strQuery* .</span><span class="sxs-lookup"><span data-stu-id="23982-171">The **ExecQuery** method returns key properties whether or not the key property is requested in the *strQuery* argument.</span></span> <span data-ttu-id="23982-172">Se si verifica un errore durante l'esecuzione di questo metodo e non si utilizza il flag **wbemFlagReturnImmediately** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) non viene impostato fino a quando non si tenta di accedere al set di oggetti restituito.</span><span class="sxs-lookup"><span data-stu-id="23982-172">If an error occurs when executing this method and you do not use the **wbemFlagReturnImmediately** flag, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object is not set until you attempt to access the returned object set.</span></span> <span data-ttu-id="23982-173">Tuttavia, se si usa il flag **wbemFlagReturnWhenComplete** , l'oggetto Err viene impostato quando viene chiamato il metodo **ExecQuery** .</span><span class="sxs-lookup"><span data-stu-id="23982-173">However, if you use the **wbemFlagReturnWhenComplete** flag, the Err object is set when the **ExecQuery** method is called.</span></span>

<span data-ttu-id="23982-174">Esistono limiti al numero di parole chiave **and** e **or** che possono essere utilizzate nelle query WQL.</span><span class="sxs-lookup"><span data-stu-id="23982-174">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="23982-175">Un numero elevato di parole chiave WQL utilizzate in una query complessa può causare la restituzione del codice di errore di **\_ \_ \_ violazione della quota E di WBEM** come valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="23982-175">Large numbers of WQL keywords that are used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="23982-176">Il limite di parole chiave WQL dipende dalla complessità della query.</span><span class="sxs-lookup"><span data-stu-id="23982-176">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="23982-177">Esempio</span><span class="sxs-lookup"><span data-stu-id="23982-177">Examples</span></span>

<span data-ttu-id="23982-178">Nell'esempio di codice VBScript seguente vengono individuate tutte le unità disco nel computer locale e vengono visualizzati l'ID del dispositivo e il tipo dell'unità disco.</span><span class="sxs-lookup"><span data-stu-id="23982-178">The following VBScript code example locates all the disk drives on the local computer and displays the device ID and the type of the disk drive.</span></span>


```VB
Set colDisks = GetObject( _
    "Winmgmts:").ExecQuery("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
 
    Select Case objDisk.DriveType
        Case 1
            Wscript.Echo "No root directory. Drive type could not be determined."
        Case 2
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Removable drive" 
        Case 3
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Local hard disk" 
        Case 4
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Network disk" 
        Case 5
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Compact disk" 
        Case 6
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = RAM disk" 
        Case Else
            Wscript.Echo "Drive type could not be determined."
    End Select
Next
```



## <a name="requirements"></a><span data-ttu-id="23982-179">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23982-179">Requirements</span></span>



| <span data-ttu-id="23982-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="23982-180">Requirement</span></span> | <span data-ttu-id="23982-181">Valore</span><span class="sxs-lookup"><span data-stu-id="23982-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23982-182">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23982-182">Minimum supported client</span></span><br/> | <span data-ttu-id="23982-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23982-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="23982-184">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23982-184">Minimum supported server</span></span><br/> | <span data-ttu-id="23982-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23982-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="23982-186">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23982-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="23982-187"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="23982-187"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="23982-188">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="23982-188">Type library</span></span><br/>             | <dl> <span data-ttu-id="23982-189"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="23982-189"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="23982-190">DLL</span><span class="sxs-lookup"><span data-stu-id="23982-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23982-191"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23982-191"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="23982-192">CLSID</span><span class="sxs-lookup"><span data-stu-id="23982-192">CLSID</span></span><br/>                    | <span data-ttu-id="23982-193">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="23982-193">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="23982-194">IID</span><span class="sxs-lookup"><span data-stu-id="23982-194">IID</span></span><br/>                      | <span data-ttu-id="23982-195">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="23982-195">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="23982-196">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23982-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23982-197">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="23982-197">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="23982-198">**SWbemServices. Get**</span><span class="sxs-lookup"><span data-stu-id="23982-198">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> <dt>

[<span data-ttu-id="23982-199">Esecuzione di query con WQL</span><span class="sxs-lookup"><span data-stu-id="23982-199">Querying with WQL</span></span>](querying-with-wql.md)
</dt> <dt>

[<span data-ttu-id="23982-200">Creazione di uno script WMI</span><span class="sxs-lookup"><span data-stu-id="23982-200">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> <dt>

[<span data-ttu-id="23982-201">Enumerazione di WMI</span><span class="sxs-lookup"><span data-stu-id="23982-201">Enumerating WMI</span></span>](enumerating-wmi.md)
</dt> </dl>

 

