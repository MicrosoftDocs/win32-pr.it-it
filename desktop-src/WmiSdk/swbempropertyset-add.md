---
description: Il metodo Add dell'oggetto SWbemPropertySet aggiunge un oggetto SWbemProperty alla raccolta SWbemPropertySet. Se nella raccolta esiste già una proprietà con lo stesso nome, il relativo contenuto viene sostituito con la nuova definizione.
ms.assetid: 52a5f964-3d53-441b-9a58-650afdc5b1b9
ms.tgt_platform: multiple
title: Metodo SWbemPropertySet. Add (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Add
- ISWbemPropertySet.Add
- ISWbemPropertySet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1ad5b40d31d162b287bdb1a387cd0602e0be1ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318172"
---
# <a name="swbempropertysetadd-method"></a><span data-ttu-id="904e3-104">SWbemPropertySet. Add, metodo</span><span class="sxs-lookup"><span data-stu-id="904e3-104">SWbemPropertySet.Add method</span></span>

<span data-ttu-id="904e3-105">Il metodo **Add** dell'oggetto [**SWbemPropertySet**](swbempropertyset.md) aggiunge un oggetto [**SWbemProperty**](swbemproperty.md) alla raccolta **SWbemPropertySet** .</span><span class="sxs-lookup"><span data-stu-id="904e3-105">The **Add** method of the [**SWbemPropertySet**](swbempropertyset.md) object adds an [**SWbemProperty**](swbemproperty.md) object to the **SWbemPropertySet** collection.</span></span> <span data-ttu-id="904e3-106">Se nella raccolta esiste già una proprietà con lo stesso nome, il relativo contenuto viene sostituito con la nuova definizione.</span><span class="sxs-lookup"><span data-stu-id="904e3-106">If a property with the same name already exists in the collection, its contents are replaced with the new definition.</span></span>

> [!Note]  
> <span data-ttu-id="904e3-107">Il valore della proprietà aggiunta è **null** (non assegnato) dopo questa operazione.</span><span class="sxs-lookup"><span data-stu-id="904e3-107">The value of the added property is **NULL** (unassigned) after this operation.</span></span> <span data-ttu-id="904e3-108">Per impostare o modificare il valore di una proprietà WMI, è necessario impostare la proprietà [**value**](swbemdatetime-value.md) dell'oggetto [**SWbemProperty**](swbemproperty.md) restituito.</span><span class="sxs-lookup"><span data-stu-id="904e3-108">To set or change the value of a WMI property, you must set the [**Value**](swbemdatetime-value.md) property of the returned [**SWbemProperty**](swbemproperty.md) object.</span></span>

 

<span data-ttu-id="904e3-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="904e3-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="904e3-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="904e3-110">Syntax</span></span>


```VB
objProperty = .Add( _
  ByVal strName, _
  ByVal iCIMType, _
  [ ByVal bIsArray ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="904e3-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="904e3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="904e3-112">*strName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="904e3-112">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="904e3-113">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="904e3-113">Required.</span></span> <span data-ttu-id="904e3-114">Nome della nuova proprietà.</span><span class="sxs-lookup"><span data-stu-id="904e3-114">Name of the new property.</span></span>

</dd> <dt>

<span data-ttu-id="904e3-115">*iCIMType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="904e3-115">*iCIMType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="904e3-116">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="904e3-116">Required.</span></span> <span data-ttu-id="904e3-117">Intero che rappresenta il qualificatore **CimType** della nuova proprietà.</span><span class="sxs-lookup"><span data-stu-id="904e3-117">An integer that represents the **CIMType** qualifier of the new property.</span></span> <span data-ttu-id="904e3-118">Vedere [**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) per l'elenco con i qualificatori **CimType** e i relativi valori.</span><span class="sxs-lookup"><span data-stu-id="904e3-118">See [**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) for the list with the **CIMType** qualifiers and their values.</span></span>

</dd> <dt>

<span data-ttu-id="904e3-119">*bIsArray* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="904e3-119">*bIsArray* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="904e3-120">Specifica se la proprietà è un tipo di matrice.</span><span class="sxs-lookup"><span data-stu-id="904e3-120">Specifies whether the property is an array type.</span></span> <span data-ttu-id="904e3-121">Il valore predefinito per questo parametro è **false**.</span><span class="sxs-lookup"><span data-stu-id="904e3-121">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="904e3-122">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="904e3-122">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="904e3-123">Riservato e deve essere zero se specificato.</span><span class="sxs-lookup"><span data-stu-id="904e3-123">Reserved and must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="904e3-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="904e3-124">Return value</span></span>

<span data-ttu-id="904e3-125">Se ha esito positivo, questo metodo restituisce un oggetto [**SWbemProperty**](swbemproperty.md) che rappresenta la nuova proprietà.</span><span class="sxs-lookup"><span data-stu-id="904e3-125">If successful, this method returns an [**SWbemProperty**](swbemproperty.md) object that represents the new property.</span></span> <span data-ttu-id="904e3-126">In caso contrario, viene restituito un oggetto **null** .</span><span class="sxs-lookup"><span data-stu-id="904e3-126">Otherwise, a **null** object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="904e3-127">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="904e3-127">Error codes</span></span>

<span data-ttu-id="904e3-128">Dopo il completamento del metodo **Add** , l'oggetto **Err** può contenere uno dei codici di errore riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="904e3-128">After completion of the **Add** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="904e3-129">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="904e3-129">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="904e3-130">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="904e3-130">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="904e3-131">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="904e3-131">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="904e3-132">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="904e3-132">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="904e3-133">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="904e3-133">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="904e3-134">Memoria insufficiente per l'esecuzione di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="904e3-134">Not enough memory for this method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="904e3-135">**wbemErrInvalidPropertyType** -2147749930</span><span class="sxs-lookup"><span data-stu-id="904e3-135">**wbemErrInvalidPropertyType** - 2147749930</span></span>
</dt> <dd>

<span data-ttu-id="904e3-136">Qualificatore **CimType** non riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="904e3-136">The **CIMType** qualifier is not recognized.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="904e3-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="904e3-137">Examples</span></span>

<span data-ttu-id="904e3-138">Per un esempio di codice che usa questo metodo, vedere l'argomento [**SWbemPropertySet**](swbempropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="904e3-138">For a code example that uses this method, see the [**SWbemPropertySet**](swbempropertyset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="904e3-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="904e3-139">Requirements</span></span>



| <span data-ttu-id="904e3-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="904e3-140">Requirement</span></span> | <span data-ttu-id="904e3-141">Valore</span><span class="sxs-lookup"><span data-stu-id="904e3-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="904e3-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="904e3-142">Minimum supported client</span></span><br/> | <span data-ttu-id="904e3-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="904e3-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="904e3-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="904e3-144">Minimum supported server</span></span><br/> | <span data-ttu-id="904e3-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="904e3-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="904e3-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="904e3-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="904e3-147"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="904e3-147"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="904e3-148">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="904e3-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="904e3-149"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="904e3-149"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="904e3-150">DLL</span><span class="sxs-lookup"><span data-stu-id="904e3-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="904e3-151"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="904e3-151"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="904e3-152">CLSID</span><span class="sxs-lookup"><span data-stu-id="904e3-152">CLSID</span></span><br/>                    | <span data-ttu-id="904e3-153">\_SWBEMPROPERTYSET CLSID</span><span class="sxs-lookup"><span data-stu-id="904e3-153">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="904e3-154">IID</span><span class="sxs-lookup"><span data-stu-id="904e3-154">IID</span></span><br/>                      | <span data-ttu-id="904e3-155">\_ISWBEMPROPERTYSET IID</span><span class="sxs-lookup"><span data-stu-id="904e3-155">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="904e3-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="904e3-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="904e3-157">**SWbemPropertySet**</span><span class="sxs-lookup"><span data-stu-id="904e3-157">**SWbemPropertySet**</span></span>](swbempropertyset.md)
</dt> <dt>

[<span data-ttu-id="904e3-158">**SWbemPropertySet. Remove**</span><span class="sxs-lookup"><span data-stu-id="904e3-158">**SWbemPropertySet.Remove**</span></span>](swbempropertyset-remove.md)
</dt> <dt>

[<span data-ttu-id="904e3-159">**SWbemProperty. Value**</span><span class="sxs-lookup"><span data-stu-id="904e3-159">**SWbemProperty.Value**</span></span>](swbemproperty-value.md)
</dt> </dl>

 

 




