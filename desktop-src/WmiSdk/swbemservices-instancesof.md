---
description: Crea un enumeratore che restituisce le istanze di una classe specificata in base ai criteri di selezione specificati dall'utente.
ms.assetid: 6465a981-f98e-4ece-a9b6-9da8ae618bc6
ms.tgt_platform: multiple
title: Metodo SWbemServices. InstancesOf (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.InstancesOf
- ISWbemServices.InstancesOf
- ISWbemServices.InstancesOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e2386b52160b1e2a08c5a345b67922ed24afc44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885214"
---
# <a name="swbemservicesinstancesof-method"></a><span data-ttu-id="94f80-103">SWbemServices. InstancesOf, metodo</span><span class="sxs-lookup"><span data-stu-id="94f80-103">SWbemServices.InstancesOf method</span></span>

<span data-ttu-id="94f80-104">Il metodo **InstancesOf** dell'oggetto [**SWbemServices**](swbemservices.md) crea un enumeratore che restituisce le istanze di una classe specificata in base ai criteri di selezione specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="94f80-104">The **InstancesOf** method of the [**SWbemServices**](swbemservices.md) object creates an enumerator that returns the instances of a specified class according to the user-specified selection criteria.</span></span> <span data-ttu-id="94f80-105">Questo metodo implementa una semplice query.</span><span class="sxs-lookup"><span data-stu-id="94f80-105">This method implements a simple query.</span></span> <span data-ttu-id="94f80-106">Query più complesse possono richiedere l'uso di [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="94f80-106">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="94f80-107">Il metodo viene chiamato in modalità semisincrono.</span><span class="sxs-lookup"><span data-stu-id="94f80-107">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="94f80-108">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="94f80-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="94f80-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="94f80-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="94f80-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94f80-110">Syntax</span></span>


```VB
objWbemObjectSet = .InstancesOf( _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="94f80-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="94f80-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94f80-112">*strClass*</span><span class="sxs-lookup"><span data-stu-id="94f80-112">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="94f80-113">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="94f80-113">Required.</span></span> <span data-ttu-id="94f80-114">Stringa che contiene il nome della classe per cui si desiderano le istanze.</span><span class="sxs-lookup"><span data-stu-id="94f80-114">String that contains the name of the class for which instances are desired.</span></span> <span data-ttu-id="94f80-115">Questo parametro non può essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="94f80-115">This parameter cannot be blank.</span></span>

</dd> <dt>

<span data-ttu-id="94f80-116">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="94f80-116">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="94f80-117">Questo parametro determina il modo in cui la chiamata esegue l'enumerazione e se la chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="94f80-117">This parameter determines how detailed the call enumerates and if this call returns immediately.</span></span> <span data-ttu-id="94f80-118">Il valore predefinito per questo parametro è **wbemFlagReturnImmediately**.</span><span class="sxs-lookup"><span data-stu-id="94f80-118">The default value for this parameter is **wbemFlagReturnImmediately**.</span></span> <span data-ttu-id="94f80-119">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="94f80-119">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="94f80-120"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="94f80-120"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="94f80-121">Causa la restituzione di un enumeratore di sola trasmissione.</span><span class="sxs-lookup"><span data-stu-id="94f80-121">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="94f80-122">Gli enumeratori di solo avanzamento sono in genere molto più veloci e utilizzano meno memoria rispetto agli enumeratori convenzionali, ma non consentono chiamate a [**SWbemObject \_ . Clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="94f80-122">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="94f80-123"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="94f80-123"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="94f80-124">Causa la conservazione dei puntatori agli oggetti dell'enumerazione da parte di WMI finché il client non rilascia l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="94f80-124">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="94f80-125"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="94f80-125"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="94f80-126">Valore predefinito per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="94f80-126">Default value for this parameter.</span></span> <span data-ttu-id="94f80-127">Questo flag causa la restituzione immediata della chiamata.</span><span class="sxs-lookup"><span data-stu-id="94f80-127">This flag causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="94f80-128"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="94f80-128"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="94f80-129">Causa il blocco della chiamata fino al completamento della query.</span><span class="sxs-lookup"><span data-stu-id="94f80-129">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="94f80-130">Questo flag chiama il metodo in modalità sincrona.</span><span class="sxs-lookup"><span data-stu-id="94f80-130">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="94f80-131"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="94f80-131"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="94f80-132">Impone all'enumerazione di includere solo le sottoclassi immediate della classe padre specificata.</span><span class="sxs-lookup"><span data-stu-id="94f80-132">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="94f80-133"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="94f80-133"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="94f80-134">Valore predefinito per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="94f80-134">Default value for this parameter.</span></span> <span data-ttu-id="94f80-135">Questo valore impone all'enumerazione di includere tutte le classi nella gerarchia.</span><span class="sxs-lookup"><span data-stu-id="94f80-135">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="94f80-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="94f80-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="94f80-137">Causa la restituzione dei dati di modifica della classe da parte di WMI con la definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="94f80-137">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="94f80-138">Per ulteriori informazioni, vedere la pagina relativa alla [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="94f80-138">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="94f80-139">*objWbemNamedValueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="94f80-139">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="94f80-140">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="94f80-140">Typically, this is undefined.</span></span> <span data-ttu-id="94f80-141">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="94f80-141">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="94f80-142">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="94f80-142">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94f80-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="94f80-143">Return value</span></span>

<span data-ttu-id="94f80-144">Se ha esito positivo, il metodo restituisce un [**SWbemObjectSet**](swbemobjectset.md).</span><span class="sxs-lookup"><span data-stu-id="94f80-144">If successful, the method returns an [**SWbemObjectSet**](swbemobjectset.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="94f80-145">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="94f80-145">Error codes</span></span>

<span data-ttu-id="94f80-146">Al termine del metodo **InstancesOf** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="94f80-146">Upon the completion of the **InstancesOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="94f80-147">Un enumeratore restituito con zero elementi non è un errore.</span><span class="sxs-lookup"><span data-stu-id="94f80-147">A returned enumerator with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="94f80-148">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="94f80-148">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="94f80-149">L'utente corrente non dispone dell'autorizzazione per visualizzare le istanze della classe specificata.</span><span class="sxs-lookup"><span data-stu-id="94f80-149">Current user does not have the permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="94f80-150">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="94f80-150">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="94f80-151">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="94f80-151">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="94f80-152">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="94f80-152">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="94f80-153">La classe specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="94f80-153">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="94f80-154">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="94f80-154">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="94f80-155">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="94f80-155">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="94f80-156">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="94f80-156">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="94f80-157">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="94f80-157">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94f80-158">Commenti</span><span class="sxs-lookup"><span data-stu-id="94f80-158">Remarks</span></span>

<span data-ttu-id="94f80-159">Il metodo **InstancesOf** funziona solo per gli oggetti classe.</span><span class="sxs-lookup"><span data-stu-id="94f80-159">The **InstancesOf** method only works for class objects.</span></span>

<span data-ttu-id="94f80-160">Per impostazione predefinita, InstancesOf esegue un recupero approfondito.</span><span class="sxs-lookup"><span data-stu-id="94f80-160">By default, InstancesOf performs a deep retrieval.</span></span> <span data-ttu-id="94f80-161">Ovvero, InstancesOf recupera tutte le istanze della risorsa gestita identificata e tutte le istanze di tutte le sottoclassi definite sotto la classe di destinazione.</span><span class="sxs-lookup"><span data-stu-id="94f80-161">That is, InstancesOf retrieves all instances of the managed resource you identify and all instances of all the subclasses defined beneath the target class.</span></span> <span data-ttu-id="94f80-162">Lo script seguente, ad esempio, recupera tutte le risorse modellate da tutte le classi dinamiche definite sotto la \_ classe astratta del servizio CIM.</span><span class="sxs-lookup"><span data-stu-id="94f80-162">For example, the following script retrieves all of the resources modeled by all of the dynamic classes defined beneath the CIM\_Service abstract class.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("CIM_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Object Path: " & objSWbemObject.Path_.Path
Next
```



<span data-ttu-id="94f80-163">Se si esegue questo script, le informazioni vengono restituite.</span><span class="sxs-lookup"><span data-stu-id="94f80-163">If you run this script, you will get information back.</span></span> <span data-ttu-id="94f80-164">Tuttavia, queste informazioni non saranno limitate ai servizi installati in un computer.</span><span class="sxs-lookup"><span data-stu-id="94f80-164">However, this information will not be limited to the services installed on a computer.</span></span> <span data-ttu-id="94f80-165">Ma includerà le informazioni di tutte le classi figlio del [**\_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service), tra cui [**Win32 \_ SystemDriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver) e [**Win32 \_ ApplicationService**](/previous-versions/windows/desktop/legacy/aa394068(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94f80-165">Instead, it will include information from all child classes of [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), including [**Win32\_SystemDriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver) and [**Win32\_ApplicationService**](/previous-versions/windows/desktop/legacy/aa394068(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="94f80-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94f80-166">Requirements</span></span>



| <span data-ttu-id="94f80-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="94f80-167">Requirement</span></span> | <span data-ttu-id="94f80-168">Valore</span><span class="sxs-lookup"><span data-stu-id="94f80-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94f80-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94f80-169">Minimum supported client</span></span><br/> | <span data-ttu-id="94f80-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94f80-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94f80-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94f80-171">Minimum supported server</span></span><br/> | <span data-ttu-id="94f80-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94f80-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94f80-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="94f80-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="94f80-174"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="94f80-174"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="94f80-175">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="94f80-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="94f80-176"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="94f80-176"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="94f80-177">DLL</span><span class="sxs-lookup"><span data-stu-id="94f80-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94f80-178"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94f80-178"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="94f80-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="94f80-179">CLSID</span></span><br/>                    | <span data-ttu-id="94f80-180">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="94f80-180">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="94f80-181">IID</span><span class="sxs-lookup"><span data-stu-id="94f80-181">IID</span></span><br/>                      | <span data-ttu-id="94f80-182">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="94f80-182">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="94f80-183">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94f80-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94f80-184">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="94f80-184">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="94f80-185">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="94f80-185">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

