---
description: Restituisce un oggetto SWbemObjectSet.
ms.assetid: cfe08956-7215-4e2e-a279-6e86f14e5c27
ms.tgt_platform: multiple
title: Metodo SWbemServices. SubclassesOf (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.SubclassesOf
- ISWbemServices.SubclassesOf
- ISWbemServices.SubclassesOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e8c23dee5ee3f0a1cf5babe37d0ccb6aa0a3ac7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309770"
---
# <a name="swbemservicessubclassesof-method"></a><span data-ttu-id="552d0-103">SWbemServices. SubclassesOf, metodo</span><span class="sxs-lookup"><span data-stu-id="552d0-103">SWbemServices.SubclassesOf method</span></span>

<span data-ttu-id="552d0-104">Il metodo **SubclassesOf** dell'oggetto [**SWbemServices**](swbemservices.md) restituisce un oggetto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="552d0-104">The **SubclassesOf** method of the [**SWbemServices**](swbemservices.md) object returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="552d0-105">Questo oggetto è una raccolta di sottoclassi di una classe specificata.</span><span class="sxs-lookup"><span data-stu-id="552d0-105">This object is a collection of subclasses of a specified class.</span></span> <span data-ttu-id="552d0-106">Gli elementi nella raccolta restituita possono essere ottenuti utilizzando metodi di raccolta standard.</span><span class="sxs-lookup"><span data-stu-id="552d0-106">Items in the returned collection can be obtained using standard collection methods.</span></span> <span data-ttu-id="552d0-107">Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="552d0-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="552d0-108">Questo metodo funziona solo per gli oggetti classe.</span><span class="sxs-lookup"><span data-stu-id="552d0-108">This method only works for class objects.</span></span>

<span data-ttu-id="552d0-109">Il metodo viene chiamato in modalità semisincrono.</span><span class="sxs-lookup"><span data-stu-id="552d0-109">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="552d0-110">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="552d0-110">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="552d0-111">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="552d0-111">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="552d0-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="552d0-112">Syntax</span></span>


```VB
objWbemObjectSet = .SubclassesOf( _
  [ ByVal strSuperclass ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="552d0-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="552d0-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="552d0-114">*strSuperclass* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="552d0-114">*strSuperclass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="552d0-115">Specifica un nome di classe padre.</span><span class="sxs-lookup"><span data-stu-id="552d0-115">Specifies a parent class name.</span></span> <span data-ttu-id="552d0-116">Solo le sottoclassi di questa classe restituiscono nell'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="552d0-116">Only subclasses of this class return in the enumerator.</span></span> <span data-ttu-id="552d0-117">Se si lascia vuoto questo parametro e se *iFlags* è **wbemQueryFlagShallow**, vengono restituite solo le classi di livello superiore, ovvero le classi prive di classe padre.</span><span class="sxs-lookup"><span data-stu-id="552d0-117">If you leave this parameter blank, and if *iFlags* is **wbemQueryFlagShallow**, only the top-level classes are returned (that is, classes that have no parent class).</span></span> <span data-ttu-id="552d0-118">Se questo parametro è vuoto e *iFlags* è **wbemQueryFlagDeep** , vengono restituite tutte le classi all'interno dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="552d0-118">If this parameter is blank and *iFlags* is **wbemQueryFlagDeep** all classes within the namespace are returned.</span></span>

</dd> <dt>

<span data-ttu-id="552d0-119">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="552d0-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="552d0-120">Determina la modalità di enumerazione della chiamata.</span><span class="sxs-lookup"><span data-stu-id="552d0-120">Determines how detailed the call enumerates.</span></span> <span data-ttu-id="552d0-121">I valori predefiniti per questo parametro sono **wbemFlagReturnImmediately** e **wbemQueryFlagDeep**.</span><span class="sxs-lookup"><span data-stu-id="552d0-121">The default values for this parameter are **wbemFlagReturnImmediately** and **wbemQueryFlagDeep**.</span></span> <span data-ttu-id="552d0-122">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="552d0-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="552d0-123"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="552d0-123"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="552d0-124">Impone all'enumerazione di includere solo le sottoclassi immediate della classe padre specificata.</span><span class="sxs-lookup"><span data-stu-id="552d0-124">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="552d0-125"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="552d0-125"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="552d0-126">Valore predefinito per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="552d0-126">Default for this parameter.</span></span> <span data-ttu-id="552d0-127">Questo valore forza l'enumerazione ricorsiva in tutte le sottoclassi derivate dalla classe padre specificata.</span><span class="sxs-lookup"><span data-stu-id="552d0-127">This value forces recursive enumeration into all subclasses that are derived from the specified parent class.</span></span> <span data-ttu-id="552d0-128">La classe padre non viene restituita nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="552d0-128">The parent class is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="552d0-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="552d0-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="552d0-130">Causa la restituzione immediata della chiamata.</span><span class="sxs-lookup"><span data-stu-id="552d0-130">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="552d0-131"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="552d0-131"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="552d0-132">Causa il blocco della chiamata fino al completamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="552d0-132">Causes this call to block until the call has completed.</span></span> <span data-ttu-id="552d0-133">Questo flag chiama il metodo in modalità sincrona.</span><span class="sxs-lookup"><span data-stu-id="552d0-133">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="552d0-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="552d0-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="552d0-135">Causa la restituzione dei dati di modifica della classe da parte di WMI con la definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="552d0-135">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="552d0-136">Per ulteriori informazioni, vedere la pagina relativa alla [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="552d0-136">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="552d0-137">*objWbemNamedValueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="552d0-137">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="552d0-138">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="552d0-138">Typically, this is undefined.</span></span> <span data-ttu-id="552d0-139">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider per la manutenzione della richiesta.</span><span class="sxs-lookup"><span data-stu-id="552d0-139">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider servicing the request.</span></span> <span data-ttu-id="552d0-140">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="552d0-140">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="552d0-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="552d0-141">Return value</span></span>

<span data-ttu-id="552d0-142">Se il metodo ha esito positivo, viene restituito un oggetto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="552d0-142">If the method is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="552d0-143">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="552d0-143">Error codes</span></span>

<span data-ttu-id="552d0-144">Dopo il completamento del metodo **SubclassesOf** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="552d0-144">After the completion of the **SubclassesOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="552d0-145">Una raccolta restituita con zero elementi non è un errore.</span><span class="sxs-lookup"><span data-stu-id="552d0-145">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="552d0-146">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="552d0-146">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="552d0-147">L'utente corrente non dispone dell'autorizzazione per visualizzare una o più classi restituite dalla chiamata.</span><span class="sxs-lookup"><span data-stu-id="552d0-147">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="552d0-148">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="552d0-148">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="552d0-149">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="552d0-149">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="552d0-150">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="552d0-150">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="552d0-151">La classe specificata non esiste.</span><span class="sxs-lookup"><span data-stu-id="552d0-151">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="552d0-152">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="552d0-152">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="552d0-153">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="552d0-153">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="552d0-154">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="552d0-154">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="552d0-155">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="552d0-155">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="552d0-156">Esempio</span><span class="sxs-lookup"><span data-stu-id="552d0-156">Examples</span></span>

<span data-ttu-id="552d0-157">Nell'esempio di PowerShell seguente viene illustrato come recuperare le sottoclassi di una classe in un sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="552d0-157">The following PowerShell sample shows how to retrieve the subclasses of a class on a remote system.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="552d0-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="552d0-158">Requirements</span></span>



| <span data-ttu-id="552d0-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="552d0-159">Requirement</span></span> | <span data-ttu-id="552d0-160">Valore</span><span class="sxs-lookup"><span data-stu-id="552d0-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="552d0-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="552d0-161">Minimum supported client</span></span><br/> | <span data-ttu-id="552d0-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="552d0-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="552d0-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="552d0-163">Minimum supported server</span></span><br/> | <span data-ttu-id="552d0-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="552d0-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="552d0-165">Intestazione</span><span class="sxs-lookup"><span data-stu-id="552d0-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="552d0-166"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="552d0-166"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="552d0-167">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="552d0-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="552d0-168"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="552d0-168"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="552d0-169">DLL</span><span class="sxs-lookup"><span data-stu-id="552d0-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="552d0-170"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="552d0-170"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="552d0-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="552d0-171">CLSID</span></span><br/>                    | <span data-ttu-id="552d0-172">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="552d0-172">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="552d0-173">IID</span><span class="sxs-lookup"><span data-stu-id="552d0-173">IID</span></span><br/>                      | <span data-ttu-id="552d0-174">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="552d0-174">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="552d0-175">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="552d0-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="552d0-176">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="552d0-176">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="552d0-177">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="552d0-177">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




