---
description: Il metodo Add dell'oggetto dell'SWbemQualifierSet aggiunge un oggetto oggetto SWbemQualifier alla raccolta dell'SWbemQualifierSet. Se nella raccolta esiste già un qualificatore con lo stesso nome, viene sostituito.
ms.assetid: 8f4c4da2-4890-4515-a3dc-76d154dae43c
ms.tgt_platform: multiple
title: Metodo dell'SWbemQualifierSet. Add (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Add
- ISWbemQualifierSet.Add
- ISWbemQualifierSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: bbbef15ccc45aeba5b7e3c03f6cb9448cfe03ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349201"
---
# <a name="swbemqualifiersetadd-method"></a><span data-ttu-id="79deb-104">Dell'SWbemQualifierSet. Add, metodo</span><span class="sxs-lookup"><span data-stu-id="79deb-104">SWbemQualifierSet.Add method</span></span>

<span data-ttu-id="79deb-105">Il metodo **Add** dell'oggetto [**dell'SWbemQualifierSet**](swbemqualifierset.md) aggiunge un oggetto [**oggetto SWbemQualifier**](swbemqualifier.md) alla raccolta **dell'SWbemQualifierSet** .</span><span class="sxs-lookup"><span data-stu-id="79deb-105">The **Add** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object adds an [**SWbemQualifier**](swbemqualifier.md) object to the **SWbemQualifierSet** collection.</span></span> <span data-ttu-id="79deb-106">Se nella raccolta esiste già un qualificatore con lo stesso nome, viene sostituito.</span><span class="sxs-lookup"><span data-stu-id="79deb-106">If a qualifier with the same name already exists in the collection, it is replaced.</span></span>

<span data-ttu-id="79deb-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="79deb-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="79deb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79deb-108">Syntax</span></span>


```VB
objQualifier = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal bPropagatesToSubclasses ], _
  [ ByVal bPropagatesToInstances ], _
  [ ByVal bOverridable ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="79deb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="79deb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79deb-110">*strName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79deb-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79deb-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="79deb-111">Required.</span></span> <span data-ttu-id="79deb-112">Nome del nuovo qualificatore.</span><span class="sxs-lookup"><span data-stu-id="79deb-112">Name of the new qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="79deb-113">*varVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79deb-113">*varVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79deb-114">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="79deb-114">Required.</span></span> <span data-ttu-id="79deb-115">Valore Variant del nuovo qualificatore.</span><span class="sxs-lookup"><span data-stu-id="79deb-115">Variant value of the new qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="79deb-116">*bPropagatesToSubclasses* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="79deb-116">*bPropagatesToSubclasses* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="79deb-117">Valore booleano che indica se questo nuovo qualificatore viene propagato alle sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="79deb-117">Boolean value that indicates if this new qualifier is propagated to subclasses.</span></span> <span data-ttu-id="79deb-118">Il valore predefinito è **true**.</span><span class="sxs-lookup"><span data-stu-id="79deb-118">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="79deb-119">*bPropagatesToInstances* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="79deb-119">*bPropagatesToInstances* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="79deb-120">Valore booleano che indica se questo nuovo qualificatore viene propagato alle istanze.</span><span class="sxs-lookup"><span data-stu-id="79deb-120">Boolean value that indicates if this new qualifier is propagated to instances.</span></span> <span data-ttu-id="79deb-121">Il valore predefinito è **true**.</span><span class="sxs-lookup"><span data-stu-id="79deb-121">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="79deb-122">*bOverridable* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="79deb-122">*bOverridable* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="79deb-123">Valore booleano che indica se il qualificatore può essere sottoposto a override quando viene propagato.</span><span class="sxs-lookup"><span data-stu-id="79deb-123">Boolean value that indicates if this qualifier can be overridden when propagated.</span></span> <span data-ttu-id="79deb-124">Il valore predefinito è **true**.</span><span class="sxs-lookup"><span data-stu-id="79deb-124">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="79deb-125">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="79deb-125">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="79deb-126">Riservato.</span><span class="sxs-lookup"><span data-stu-id="79deb-126">Reserved.</span></span> <span data-ttu-id="79deb-127">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="79deb-127">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79deb-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="79deb-128">Return value</span></span>

<span data-ttu-id="79deb-129">Se ha esito positivo, questo metodo restituisce un oggetto [**oggetto SWbemQualifier**](swbemqualifier.md) che rappresenta il nuovo qualificatore.</span><span class="sxs-lookup"><span data-stu-id="79deb-129">If successful, this method returns an [**SWbemQualifier**](swbemqualifier.md) object that represents the new qualifier.</span></span> <span data-ttu-id="79deb-130">In caso contrario, viene restituito un oggetto **null** .</span><span class="sxs-lookup"><span data-stu-id="79deb-130">Otherwise, a **null** object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="79deb-131">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="79deb-131">Error codes</span></span>

<span data-ttu-id="79deb-132">Dopo il completamento del metodo **Add** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="79deb-132">After completion of the **Add** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="79deb-133">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="79deb-133">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="79deb-134">Il parametro *iFlags* non è valido.</span><span class="sxs-lookup"><span data-stu-id="79deb-134">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="79deb-135">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="79deb-135">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="79deb-136">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="79deb-136">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="79deb-137">**wbemErrCannotBeKey** -2147749919 (0x8004101F)</span><span class="sxs-lookup"><span data-stu-id="79deb-137">**wbemErrCannotBeKey** - 2147749919 (0x8004101F)</span></span>
</dt> <dd>

<span data-ttu-id="79deb-138">Si è verificato un tentativo non valido di specificare un qualificatore di **chiave** su una proprietà che non può essere una chiave.</span><span class="sxs-lookup"><span data-stu-id="79deb-138">There was an illegal attempt to specify a **Key** qualifier on a property that cannot be a key.</span></span> <span data-ttu-id="79deb-139">Le chiavi sono specificate nella definizione della classe per un oggetto e non possono essere alterate per singole istanze.</span><span class="sxs-lookup"><span data-stu-id="79deb-139">The keys are specified in the class definition for an object and cannot be altered on a per-instance basis.</span></span>

</dd> <dt>

<span data-ttu-id="79deb-140">**wbemErrInvalidQualifierType** -2147749929 (0x80041029)</span><span class="sxs-lookup"><span data-stu-id="79deb-140">**wbemErrInvalidQualifierType** - 2147749929 (0x80041029)</span></span>
</dt> <dd>

<span data-ttu-id="79deb-141">Il parametro *varVal* non è di un tipo di qualificatore valido.</span><span class="sxs-lookup"><span data-stu-id="79deb-141">The *varVal* parameter is not of a legal qualifier type.</span></span>

</dd> <dt>

<span data-ttu-id="79deb-142">**wbemErrOverrideNotAllowed** -2147749914 (0x8004101A)</span><span class="sxs-lookup"><span data-stu-id="79deb-142">**wbemErrOverrideNotAllowed** - 2147749914 (0x8004101A)</span></span>
</dt> <dd>

<span data-ttu-id="79deb-143">Non è possibile eseguire l'operazione **dell'SWbemQualifierSet. Add** su questo qualificatore perché l'oggetto proprietario non consente le sostituzioni.</span><span class="sxs-lookup"><span data-stu-id="79deb-143">It is not possible to perform the **SWbemQualifierSet.Add** operation on this qualifier because the owning object does not permit overrides.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79deb-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79deb-144">Requirements</span></span>



| <span data-ttu-id="79deb-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="79deb-145">Requirement</span></span> | <span data-ttu-id="79deb-146">Valore</span><span class="sxs-lookup"><span data-stu-id="79deb-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79deb-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79deb-147">Minimum supported client</span></span><br/> | <span data-ttu-id="79deb-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79deb-148">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="79deb-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79deb-149">Minimum supported server</span></span><br/> | <span data-ttu-id="79deb-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79deb-150">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="79deb-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="79deb-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="79deb-152"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="79deb-152"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="79deb-153">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="79deb-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="79deb-154"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="79deb-154"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="79deb-155">DLL</span><span class="sxs-lookup"><span data-stu-id="79deb-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79deb-156"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79deb-156"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="79deb-157">CLSID</span><span class="sxs-lookup"><span data-stu-id="79deb-157">CLSID</span></span><br/>                    | <span data-ttu-id="79deb-158">\_Dell'SWBEMQUALIFIERSET CLSID</span><span class="sxs-lookup"><span data-stu-id="79deb-158">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="79deb-159">IID</span><span class="sxs-lookup"><span data-stu-id="79deb-159">IID</span></span><br/>                      | <span data-ttu-id="79deb-160">\_ISWBEMQUALIFIERSET IID</span><span class="sxs-lookup"><span data-stu-id="79deb-160">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="79deb-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79deb-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79deb-162">**Dell'SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="79deb-162">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="79deb-163">**Dell'SWbemQualifierSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="79deb-163">**SWbemQualifierSet.Remove**</span></span>](swbemqualifierset-remove.md)
</dt> </dl>

 

 




