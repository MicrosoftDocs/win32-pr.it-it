---
description: Il \_ Metodo CompareTo dell'oggetto SWbemObject Confronta due oggetti SWbemObject. Questo confronto è soggetto a determinati vincoli in base ai valori specificati nel parametro iFlags.
ms.assetid: 38813551-2403-4def-ae57-2b17f72cd180
ms.tgt_platform: multiple
title: Metodo SWbemObject.CompareTo_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.CompareTo_
- ISWbemObject.CompareTo_
- ISWbemObject.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f77bf9db9ee864e136ba695051445e543b466e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755015"
---
# <a name="swbemobjectcompareto_-method"></a><span data-ttu-id="ccd4b-104">Metodo SWbemObject. CompareTo \_</span><span class="sxs-lookup"><span data-stu-id="ccd4b-104">SWbemObject.CompareTo\_ method</span></span>

<span data-ttu-id="ccd4b-105">Il **metodo \_ CompareTo** dell'oggetto [**SWbemObject**](swbemobject.md) Confronta due oggetti **SWbemObject** .</span><span class="sxs-lookup"><span data-stu-id="ccd4b-105">The **CompareTo\_** method of the [**SWbemObject**](swbemobject.md) object compares two **SWbemObject** objects.</span></span> <span data-ttu-id="ccd4b-106">Questo confronto è soggetto a determinati vincoli in base ai valori specificati nel parametro *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="ccd4b-106">This comparison is subject to certain constraints based on the values specified in the *iFlags* parameter.</span></span>

<span data-ttu-id="ccd4b-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ccd4b-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ccd4b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ccd4b-108">Syntax</span></span>


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ccd4b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ccd4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccd4b-110">*objwbemObject* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ccd4b-110">*objwbemObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd4b-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-111">Required.</span></span> <span data-ttu-id="ccd4b-112">Questo parametro è un oggetto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="ccd4b-112">This parameter is an [**SWbemObject**](swbemobject.md) object.</span></span> <span data-ttu-id="ccd4b-113">Si tratta dell'oggetto con il quale viene confrontato il primo oggetto.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-113">This is the object with which the first object is compared.</span></span> <span data-ttu-id="ccd4b-114">L'oggetto deve essere un'istanza di **SWbemObject** valida.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-114">The object must be a valid **SWbemObject** instance.</span></span>

</dd> <dt>

<span data-ttu-id="ccd4b-115">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ccd4b-115">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd4b-116">Specifica le caratteristiche dell'oggetto da considerare quando si confronta un oggetto con altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-116">Specifies the object characteristics to consider when comparing an object with other objects.</span></span> <span data-ttu-id="ccd4b-117">È possibile usare **wbemComparisonFlagIncludeAll** per considerare tutte le funzionalità (impostazione predefinita) o qualsiasi combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-117">You can use **wbemComparisonFlagIncludeAll** to consider all features (this is the default), or any combination of the following values.</span></span>

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span data-ttu-id="ccd4b-118"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemComparisonFlagIncludeAll \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="ccd4b-118"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>\*\*\*\*wbemComparisonFlagIncludeAll\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="ccd4b-119">Confronta tutte le proprietà, i qualificatori e le versioni.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-119">Compares all properties, qualifiers, and flavors.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span data-ttu-id="ccd4b-120"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemComparisonFlagIgnoreObjectSource \* \* \* \* (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="ccd4b-120"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>\*\*\*\*wbemComparisonFlagIgnoreObjectSource\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="ccd4b-121">Causa l'origine degli oggetti, ovvero il server e lo spazio dei nomi da cui provengono, da ignorare rispetto ad altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-121">Causes the source of the objects, namely the server and the namespace they came from, to be ignored in comparison to other objects.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span data-ttu-id="ccd4b-122"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemComparisonFlagIgnoreQualifiers \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="ccd4b-122"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>\*\*\*\*wbemComparisonFlagIgnoreQualifiers\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="ccd4b-123">Fa in modo che tutti i qualificatori, incluse la **chiave** e la **dinamica**, vengano ignorati in confronto.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-123">Causes all qualifiers (including **Key** and **Dynamic**) to be ignored in comparison.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span data-ttu-id="ccd4b-124"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemComparisonFlagIgnoreDefaultValues \* \* \* \* (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="ccd4b-124"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>\*\*\*\*wbemComparisonFlagIgnoreDefaultValues\*\*\*\* (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="ccd4b-125">Fa in modo che i valori predefiniti delle proprietà vengano ignorati.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-125">Causes default values of properties to be ignored.</span></span> <span data-ttu-id="ccd4b-126">Questo flag è significativo solo quando si confrontano le classi.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-126">This flag is only meaningful when comparing classes.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span data-ttu-id="ccd4b-127"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemComparisonFlagIgnoreFlavor \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="ccd4b-127"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>\*\*\*\*wbemComparisonFlagIgnoreFlavor\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="ccd4b-128">Consente di ignorare le versioni del qualificatore.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-128">Causes qualifier flavors to be ignored.</span></span> <span data-ttu-id="ccd4b-129">Questo flag prende in considerazione i valori dei qualificatori, ma ignora le differenze di sapore, ad esempio le regole di propagazione e le restrizioni di sostituzione.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-129">This flag takes qualifier values into account, but ignores flavor distinctions such as propagation rules and override restrictions.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span data-ttu-id="ccd4b-130"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemComparisonFlagIgnoreCase \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="ccd4b-130"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>\*\*\*\*wbemComparisonFlagIgnoreCase\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="ccd4b-131">Confronta i valori stringa senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-131">Compares string values in a case-insensitive manner.</span></span> <span data-ttu-id="ccd4b-132">Questo vale sia per le stringhe sia per i valori del qualificatore.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-132">This applies both to strings and to qualifier values.</span></span> <span data-ttu-id="ccd4b-133">I nomi di proprietà e di qualificatori vengono sempre confrontati senza distinzione tra maiuscole e minuscole, indipendentemente dal fatto che questo flag sia specificato.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-133">Property and qualifier names are always compared in a case-insensitive manner whether this flag is specified or not.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span data-ttu-id="ccd4b-134"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemComparisonFlagIgnoreClass \* \* \* \* (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="ccd4b-134"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>\*\*\*\*wbemComparisonFlagIgnoreClass\*\*\*\* (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="ccd4b-135">Indica al sistema di presumere che gli oggetti da confrontare siano istanze della stessa classe.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-135">Instructs the system to assume that the objects being compared are instances of the same class.</span></span> <span data-ttu-id="ccd4b-136">Di conseguenza, questo flag confronta solo le informazioni correlate all'istanza.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-136">Consequently, this flag compares instance-related information only.</span></span> <span data-ttu-id="ccd4b-137">Utilizzare questo flag per ottimizzare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-137">Use this flag to optimize performance.</span></span> <span data-ttu-id="ccd4b-138">Se gli oggetti non appartengono alla stessa classe, i risultati sono indefiniti.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-138">If the objects are not of the same class, the results are undefined.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccd4b-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ccd4b-139">Return value</span></span>

<span data-ttu-id="ccd4b-140">Questo metodo restituisce il valore booleano **true** se gli oggetti corrispondono.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-140">This method returns the Boolean value of **TRUE** if the objects match.</span></span> <span data-ttu-id="ccd4b-141">Restituisce **false** se gli oggetti non corrispondono.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-141">It returns **FALSE** if the objects do not match.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ccd4b-142">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ccd4b-142">Error codes</span></span>

<span data-ttu-id="ccd4b-143">Dopo il completamento del metodo **CompareTo \_** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-143">After the completion of the **CompareTo\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="ccd4b-144">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="ccd4b-144">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ccd4b-145">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-145">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="ccd4b-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="ccd4b-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="ccd4b-147">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ccd4b-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="ccd4b-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="ccd4b-149">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ccd4b-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ccd4b-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccd4b-150">Requirements</span></span>



| <span data-ttu-id="ccd4b-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccd4b-151">Requirement</span></span> | <span data-ttu-id="ccd4b-152">Valore</span><span class="sxs-lookup"><span data-stu-id="ccd4b-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd4b-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccd4b-153">Minimum supported client</span></span><br/> | <span data-ttu-id="ccd4b-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ccd4b-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ccd4b-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccd4b-155">Minimum supported server</span></span><br/> | <span data-ttu-id="ccd4b-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ccd4b-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ccd4b-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ccd4b-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccd4b-158"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccd4b-158"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ccd4b-159">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ccd4b-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="ccd4b-160"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ccd4b-160"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ccd4b-161">DLL</span><span class="sxs-lookup"><span data-stu-id="ccd4b-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccd4b-162"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccd4b-162"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ccd4b-163">CLSID</span><span class="sxs-lookup"><span data-stu-id="ccd4b-163">CLSID</span></span><br/>                    | <span data-ttu-id="ccd4b-164">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="ccd4b-164">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="ccd4b-165">IID</span><span class="sxs-lookup"><span data-stu-id="ccd4b-165">IID</span></span><br/>                      | <span data-ttu-id="ccd4b-166">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="ccd4b-166">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="ccd4b-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ccd4b-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccd4b-168">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="ccd4b-168">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

 




