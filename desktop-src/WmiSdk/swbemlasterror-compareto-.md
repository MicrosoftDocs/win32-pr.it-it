---
description: Il \_ Metodo CompareTo dell'oggetto SWbemLastError Confronta due oggetti SWbemObject. Questo confronto è soggetto a determinati vincoli in base ai valori specificati nel parametro iFlags.
ms.assetid: 541510e4-ef8d-4436-966f-19c5df422281
ms.tgt_platform: multiple
title: Metodo SWbemLastError.CompareTo_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4c24eb6e57e81c6c44922b2d6643be65198951ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309848"
---
# <a name="swbemlasterrorcompareto_-method"></a><span data-ttu-id="86b52-104">Metodo SWbemLastError. CompareTo \_</span><span class="sxs-lookup"><span data-stu-id="86b52-104">SWbemLastError.CompareTo\_ method</span></span>

<span data-ttu-id="86b52-105">Il **metodo \_ CompareTo** dell'oggetto [**SWbemLastError**](swbemlasterror.md) Confronta due oggetti [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="86b52-105">The **CompareTo\_** method of the [**SWbemLastError**](swbemlasterror.md) object compares two [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="86b52-106">Questo confronto è soggetto a determinati vincoli in base ai valori specificati nel parametro *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="86b52-106">This comparison is subject to certain constraints based on the values specified in the *iFlags* parameter.</span></span>

<span data-ttu-id="86b52-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="86b52-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="86b52-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86b52-108">Syntax</span></span>


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="86b52-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="86b52-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86b52-110">*objwbemObject* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86b52-110">*objwbemObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86b52-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="86b52-111">Required.</span></span> <span data-ttu-id="86b52-112">Oggetto della classe [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="86b52-112">An [**SWbemObject**](swbemobject.md) class object.</span></span> <span data-ttu-id="86b52-113">Questo parametro è l'oggetto con cui viene confrontato il primo oggetto.</span><span class="sxs-lookup"><span data-stu-id="86b52-113">This parameter is the object with which the first object is compared.</span></span> <span data-ttu-id="86b52-114">L'oggetto deve essere un'istanza di **SWbemObject** valida.</span><span class="sxs-lookup"><span data-stu-id="86b52-114">The object must be a valid **SWbemObject** instance.</span></span>

</dd> <dt>

<span data-ttu-id="86b52-115">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="86b52-115">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="86b52-116">Intero che specifica flag aggiuntivi per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="86b52-116">An integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="86b52-117">Questo parametro specifica le caratteristiche dell'oggetto da considerare quando vengono eseguiti i confronti degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="86b52-117">This parameter specifies the object characteristics to consider when object comparisons are made.</span></span> <span data-ttu-id="86b52-118">È possibile utilizzare **wbemComparisonFlagIncludeAll** per considerare tutte le funzionalità (impostazione predefinita) o qualsiasi combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="86b52-118">You can use **wbemComparisonFlagIncludeAll** to consider all features (default) or any combination of the following values.</span></span>

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span data-ttu-id="86b52-119"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemComparisonFlagIncludeAll \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="86b52-119"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>\*\*\*\*wbemComparisonFlagIncludeAll\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="86b52-120">Causa il confronto di tutte le proprietà, i qualificatori e le versioni.</span><span class="sxs-lookup"><span data-stu-id="86b52-120">Causes all properties, qualifiers, and flavors to be compared.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span data-ttu-id="86b52-121"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemComparisonFlagIgnoreQualifiers \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="86b52-121"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>\*\*\*\*wbemComparisonFlagIgnoreQualifiers\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="86b52-122">Fa in modo che tutti i qualificatori, incluse la **chiave** e la **dinamica**, vengano ignorati in confronto.</span><span class="sxs-lookup"><span data-stu-id="86b52-122">Causes all qualifiers (including **Key** and **Dynamic**) to be ignored in comparison.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span data-ttu-id="86b52-123"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemComparisonFlagIgnoreObjectSource \* \* \* \* (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="86b52-123"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>\*\*\*\*wbemComparisonFlagIgnoreObjectSource\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="86b52-124">Causa l'origine degli oggetti, ovvero il server e lo spazio dei nomi da cui provengono, da ignorare rispetto ad altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="86b52-124">Causes the source of the objects, namely the server and the namespace they came from, to be ignored in comparison to other objects.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span data-ttu-id="86b52-125"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemComparisonFlagIgnoreDefaultValues \* \* \* \* (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="86b52-125"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>\*\*\*\*wbemComparisonFlagIgnoreDefaultValues\*\*\*\* (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="86b52-126">Fa in modo che i valori predefiniti delle proprietà vengano ignorati.</span><span class="sxs-lookup"><span data-stu-id="86b52-126">Causes the default values of properties to be ignored.</span></span> <span data-ttu-id="86b52-127">Questo flag è significativo solo quando si confrontano le classi.</span><span class="sxs-lookup"><span data-stu-id="86b52-127">This flag is only meaningful when comparing classes.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span data-ttu-id="86b52-128"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemComparisonFlagIgnoreClass \* \* \* \* (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="86b52-128"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>\*\*\*\*wbemComparisonFlagIgnoreClass\*\*\*\* (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="86b52-129">Indica al sistema di presumere che gli oggetti da confrontare siano istanze della stessa classe.</span><span class="sxs-lookup"><span data-stu-id="86b52-129">Instructs the system to assume that the objects being compared are instances of the same class.</span></span> <span data-ttu-id="86b52-130">Di conseguenza, questo flag confronta solo le informazioni correlate all'istanza.</span><span class="sxs-lookup"><span data-stu-id="86b52-130">Consequently, this flag compares instance-related information only.</span></span> <span data-ttu-id="86b52-131">Utilizzare questo flag per ottimizzare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="86b52-131">Use this flag to optimize performance.</span></span> <span data-ttu-id="86b52-132">Se gli oggetti non appartengono alla stessa classe, i risultati sono indefiniti.</span><span class="sxs-lookup"><span data-stu-id="86b52-132">If the objects are not of the same class, the results are undefined.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span data-ttu-id="86b52-133"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemComparisonFlagIgnoreCase \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="86b52-133"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>\*\*\*\*wbemComparisonFlagIgnoreCase\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="86b52-134">Fa in modo che i valori stringa vengano confrontati senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="86b52-134">Causes string values to be compared in a case-insensitive manner.</span></span> <span data-ttu-id="86b52-135">Questo vale sia per le stringhe sia per i valori del qualificatore.</span><span class="sxs-lookup"><span data-stu-id="86b52-135">This applies both to strings and to qualifier values.</span></span> <span data-ttu-id="86b52-136">I nomi di proprietà e di qualificatori vengono sempre confrontati senza distinzione tra maiuscole e minuscole, indipendentemente dal fatto che questo flag sia specificato.</span><span class="sxs-lookup"><span data-stu-id="86b52-136">Property and qualifier names are always compared in a case-insensitive manner whether this flag is specified or not.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span data-ttu-id="86b52-137"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemComparisonFlagIgnoreFlavor \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="86b52-137"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>\*\*\*\*wbemComparisonFlagIgnoreFlavor\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="86b52-138">Consente di ignorare le versioni del qualificatore.</span><span class="sxs-lookup"><span data-stu-id="86b52-138">Causes qualifier flavors to be ignored.</span></span> <span data-ttu-id="86b52-139">Impostando questo flag, anche se vengono presi in considerazione i valori del qualificatore, vengono tuttavia ignorate le distinzioni tra le caratteristiche, quali le regole di propagazione e le limitazioni di override.</span><span class="sxs-lookup"><span data-stu-id="86b52-139">This flag still takes qualifier values into account, but ignores flavor distinctions such as propagation rules and override restrictions.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86b52-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86b52-140">Return value</span></span>

<span data-ttu-id="86b52-141">Il **metodo \_ CompareTo** restituisce il valore booleano **true** se gli oggetti corrispondono; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="86b52-141">The **CompareTo\_** method returns the Boolean value **TRUE** if the objects match; otherwise, it returns **FALSE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="86b52-142">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="86b52-142">Error codes</span></span>

<span data-ttu-id="86b52-143">Al termine del metodo **CompareTo \_** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="86b52-143">Upon the completion of the **CompareTo\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="86b52-144">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="86b52-144">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="86b52-145">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="86b52-145">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="86b52-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="86b52-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="86b52-147">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="86b52-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="86b52-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="86b52-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="86b52-149">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="86b52-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="86b52-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86b52-150">Requirements</span></span>



| <span data-ttu-id="86b52-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="86b52-151">Requirement</span></span> | <span data-ttu-id="86b52-152">Valore</span><span class="sxs-lookup"><span data-stu-id="86b52-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86b52-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86b52-153">Minimum supported client</span></span><br/> | <span data-ttu-id="86b52-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86b52-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="86b52-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86b52-155">Minimum supported server</span></span><br/> | <span data-ttu-id="86b52-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86b52-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="86b52-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86b52-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="86b52-158"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="86b52-158"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="86b52-159">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="86b52-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="86b52-160"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="86b52-160"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="86b52-161">DLL</span><span class="sxs-lookup"><span data-stu-id="86b52-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86b52-162"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86b52-162"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="86b52-163">CLSID</span><span class="sxs-lookup"><span data-stu-id="86b52-163">CLSID</span></span><br/>                    | <span data-ttu-id="86b52-164">\_SWBEMLASTERROR CLSID</span><span class="sxs-lookup"><span data-stu-id="86b52-164">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="86b52-165">IID</span><span class="sxs-lookup"><span data-stu-id="86b52-165">IID</span></span><br/>                      | <span data-ttu-id="86b52-166">\_ISWBEMLASTERROR IID</span><span class="sxs-lookup"><span data-stu-id="86b52-166">IID\_ISWbemLastError</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="86b52-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86b52-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86b52-168">**SWbemLastError**</span><span class="sxs-lookup"><span data-stu-id="86b52-168">**SWbemLastError**</span></span>](swbemlasterror.md)
</dt> <dt>

[<span data-ttu-id="86b52-169">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="86b52-169">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

 




