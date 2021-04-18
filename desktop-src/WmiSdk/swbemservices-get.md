---
description: Recupera un oggetto, ovvero una definizione di classe o un'istanza, in base al percorso dell'oggetto.
ms.assetid: 3071aeb2-adab-47aa-a10c-9796766bb630
ms.tgt_platform: multiple
title: Metodo SWbemServices. Get (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Get
- ISWbemServices.Get
- ISWbemServices.Get
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c8998a1ca04206362fcc0e7405fccf8c923d74d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313161"
---
# <a name="swbemservicesget-method"></a><span data-ttu-id="cdba7-103">Metodo SWbemServices. Get</span><span class="sxs-lookup"><span data-stu-id="cdba7-103">SWbemServices.Get method</span></span>

<span data-ttu-id="cdba7-104">Il metodo **Get** dell'oggetto [**SWbemServices**](swbemservices.md) recupera un oggetto, ovvero una definizione di classe o un'istanza, in base al percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cdba7-104">The **Get** method of the [**SWbemServices**](swbemservices.md) object retrieves an object, that is either a class definition or an instance, based on the object path.</span></span> <span data-ttu-id="cdba7-105">Questo metodo recupera solo gli oggetti dallo spazio dei nomi associato all'oggetto **SWbemServices** corrente.</span><span class="sxs-lookup"><span data-stu-id="cdba7-105">This method retrieves only objects from the namespace that is associated with the current **SWbemServices** object.</span></span>

<span data-ttu-id="cdba7-106">Il metodo viene chiamato in modalità sincrona.</span><span class="sxs-lookup"><span data-stu-id="cdba7-106">The method is called in the synchronous mode.</span></span> <span data-ttu-id="cdba7-107">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="cdba7-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="cdba7-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="cdba7-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cdba7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cdba7-109">Syntax</span></span>


```VB
objWbemObject = .Get( _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="cdba7-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="cdba7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdba7-111">*strObjectPath* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="cdba7-111">*strObjectPath* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cdba7-112">Stringa che contiene il percorso dell'oggetto da recuperare.</span><span class="sxs-lookup"><span data-stu-id="cdba7-112">String that contains the object path of the object to retrieve.</span></span> <span data-ttu-id="cdba7-113">Se questo valore è vuoto, l'oggetto vuoto restituito può diventare una nuova classe.</span><span class="sxs-lookup"><span data-stu-id="cdba7-113">If this value is empty, the empty object that is returned can become a new class.</span></span> <span data-ttu-id="cdba7-114">Per ulteriori informazioni, vedere [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="cdba7-114">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdba7-115">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="cdba7-115">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cdba7-116">Integer che determina il comportamento della query.</span><span class="sxs-lookup"><span data-stu-id="cdba7-116">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="cdba7-117">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="cdba7-117">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="cdba7-118"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="cdba7-118"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="cdba7-119">Causa la restituzione dei dati di modifica della classe da parte di WMI con la definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="cdba7-119">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="cdba7-120">Per ulteriori informazioni sui qualificatori modificati, vedere [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="cdba7-120">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cdba7-121">*objWbemNamedValueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="cdba7-121">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cdba7-122">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="cdba7-122">Typically, this is undefined.</span></span> <span data-ttu-id="cdba7-123">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="cdba7-123">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="cdba7-124">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="cdba7-124">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdba7-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cdba7-125">Return value</span></span>

<span data-ttu-id="cdba7-126">Se ha esito positivo, questo metodo restituisce un oggetto [**SWbemObject**](swbemobject.md) che rappresenta l'oggetto richiesto.</span><span class="sxs-lookup"><span data-stu-id="cdba7-126">If successful, this method returns an [**SWbemObject**](swbemobject.md) object that represents the requested object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cdba7-127">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="cdba7-127">Error codes</span></span>

<span data-ttu-id="cdba7-128">Al termine del metodo **Get** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="cdba7-128">Upon the completion of the **Get** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="cdba7-129">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="cdba7-129">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="cdba7-130">L'utente corrente non dispone dell'autorizzazione per accedere all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cdba7-130">Current user does not have the permission to access the object.</span></span>

</dd> <dt>

<span data-ttu-id="cdba7-131">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="cdba7-131">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="cdba7-132">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="cdba7-132">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="cdba7-133">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="cdba7-133">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="cdba7-134">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="cdba7-134">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="cdba7-135">**wbemErrInvalidObjectPath** -2147749946 (0x8004103A)</span><span class="sxs-lookup"><span data-stu-id="cdba7-135">**wbemErrInvalidObjectPath** - 2147749946 (0x8004103A)</span></span>
</dt> <dd>

<span data-ttu-id="cdba7-136">Il percorso specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="cdba7-136">Specified path was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="cdba7-137">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="cdba7-137">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="cdba7-138">Impossibile trovare l'oggetto richiesto.</span><span class="sxs-lookup"><span data-stu-id="cdba7-138">Requested object could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="cdba7-139">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="cdba7-139">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="cdba7-140">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="cdba7-140">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cdba7-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="cdba7-141">Remarks</span></span>

<span data-ttu-id="cdba7-142">A differenza dei metodi [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) e [**InstancesOf**](swbemservices-instancesof.md) , il metodo Get restituisce sempre un [**SWbemObject**](swbemobject.md) che rappresenta un'istanza specifica di una risorsa gestita da WMI.</span><span class="sxs-lookup"><span data-stu-id="cdba7-142">Unlike the [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) and [**InstancesOf**](swbemservices-instancesof.md) methods, the Get method always returns an [**SWbemObject**](swbemobject.md) representing a specific instance of a WMI-managed resource.</span></span> <span data-ttu-id="cdba7-143">Per ottenere un'istanza specifica di una risorsa gestita da WMI utilizzando il metodo Get, è necessario indicare a di ottenere l'istanza da recuperare passando al metodo il percorso dell'oggetto, come illustrato nello script seguente.</span><span class="sxs-lookup"><span data-stu-id="cdba7-143">To obtain a specific instance of a WMI-managed resource using the Get method, you must tell Get the instance to retrieve by passing the method the object path, as shown in the following script.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set objSWbemObject = objSWbemServices.Get("Win32_Service.Name='Messenger'")
Wscript.Echo "Name:         " & objSWbemObject.Name        & vbCrLf & _
             "Display Name: " & objSWbemObject.DisplayName & vbCrLf & _
             "Start Mode:   " & objSWbemObject.StartMode   & vbCrLf & _
             "State:        " & objSWbemObject.State
```



<span data-ttu-id="cdba7-144">È possibile utilizzare questo metodo per ottenere gli oggetti [*singleton*](gloss-s.md) , ad esempio [**\_ \_ CIMOMIdentification**](--cimomidentification.md), che contiene le informazioni sulla versione relative all'installazione WMI in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="cdba7-144">You can use this method to obtain [*singleton*](gloss-s.md) objects, such as [**\_\_CIMOMIdentification**](--cimomidentification.md), which contains version information about the WMI installation that is running.</span></span>

<span data-ttu-id="cdba7-145">È possibile esaminare il repository con uno strumento di visualizzazione, ad esempio [CIM Studio](further-information.md) , per verificare che la nuova classe e l'istanza vengano visualizzate.</span><span class="sxs-lookup"><span data-stu-id="cdba7-145">You can examine the repository with a viewing tool such as [CIM Studio](further-information.md) to verify that the new class and instance appear.</span></span> <span data-ttu-id="cdba7-146">Per un esempio di rimozione di una classe e di un'istanza dal repository, vedere [**SWbemServices. Delete**](swbemservices-delete.md) o [**SWbemObject \_ . Delete**](swbemobject-delete-.md).</span><span class="sxs-lookup"><span data-stu-id="cdba7-146">For an example of removing a class and instance from the repository, see [**SWbemServices.Delete**](swbemservices-delete.md) or [**SWbemObject.Delete\_**](swbemobject-delete-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cdba7-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdba7-147">Requirements</span></span>



| <span data-ttu-id="cdba7-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdba7-148">Requirement</span></span> | <span data-ttu-id="cdba7-149">Valore</span><span class="sxs-lookup"><span data-stu-id="cdba7-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdba7-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdba7-150">Minimum supported client</span></span><br/> | <span data-ttu-id="cdba7-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cdba7-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cdba7-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdba7-152">Minimum supported server</span></span><br/> | <span data-ttu-id="cdba7-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cdba7-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cdba7-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cdba7-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdba7-155"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdba7-155"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cdba7-156">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="cdba7-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="cdba7-157"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cdba7-157"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cdba7-158">DLL</span><span class="sxs-lookup"><span data-stu-id="cdba7-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdba7-159"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdba7-159"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cdba7-160">CLSID</span><span class="sxs-lookup"><span data-stu-id="cdba7-160">CLSID</span></span><br/>                    | <span data-ttu-id="cdba7-161">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="cdba7-161">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="cdba7-162">IID</span><span class="sxs-lookup"><span data-stu-id="cdba7-162">IID</span></span><br/>                      | <span data-ttu-id="cdba7-163">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="cdba7-163">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="cdba7-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdba7-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdba7-165">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="cdba7-165">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="cdba7-166">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="cdba7-166">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

 




