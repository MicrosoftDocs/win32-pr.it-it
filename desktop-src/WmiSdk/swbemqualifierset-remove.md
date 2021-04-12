---
description: Il metodo Remove dell'oggetto dell'SWbemQualifierSet Elimina un qualificatore denominato dalla raccolta.
ms.assetid: 7d386858-efd1-42e6-9176-9cb4bcfc77d0
ms.tgt_platform: multiple
title: Metodo dell'SWbemQualifierSet. Remove (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 39c95f268328bc0cad3f3c0874b633fc36c4f5b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528471"
---
# <a name="swbemqualifiersetremove-method"></a><span data-ttu-id="2fea9-103">Metodo dell'SWbemQualifierSet. Remove</span><span class="sxs-lookup"><span data-stu-id="2fea9-103">SWbemQualifierSet.Remove method</span></span>

<span data-ttu-id="2fea9-104">Il metodo **Remove** dell'oggetto [**dell'SWbemQualifierSet**](swbemqualifierset.md) Elimina un qualificatore denominato dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="2fea9-104">The **Remove** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object deletes a named qualifier from the collection.</span></span>

<span data-ttu-id="2fea9-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2fea9-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2fea9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fea9-106">Syntax</span></span>


```VB
SWbemQualifierSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="2fea9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2fea9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fea9-108">*strName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2fea9-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fea9-109">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2fea9-109">Required.</span></span> <span data-ttu-id="2fea9-110">Nome del qualificatore da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2fea9-110">Name of the qualifier to remove.</span></span>

</dd> <dt>

<span data-ttu-id="2fea9-111">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2fea9-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2fea9-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="2fea9-112">Reserved.</span></span> <span data-ttu-id="2fea9-113">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="2fea9-113">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fea9-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2fea9-114">Return value</span></span>

<span data-ttu-id="2fea9-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="2fea9-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2fea9-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="2fea9-116">Error codes</span></span>

<span data-ttu-id="2fea9-117">Dopo il completamento del metodo **Remove** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="2fea9-117">After completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="2fea9-118">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="2fea9-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="2fea9-119">Il parametro *iFlags* non è valido.</span><span class="sxs-lookup"><span data-stu-id="2fea9-119">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2fea9-120">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="2fea9-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="2fea9-121">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="2fea9-121">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="2fea9-122">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="2fea9-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="2fea9-123">Il qualificatore specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="2fea9-123">Specified qualifier does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="2fea9-124">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="2fea9-124">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="2fea9-125">La rimozione del qualificatore non è valida.</span><span class="sxs-lookup"><span data-stu-id="2fea9-125">Removing this qualifier is illegal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2fea9-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="2fea9-126">Remarks</span></span>

<span data-ttu-id="2fea9-127">Non è possibile eseguire l'iterazione di una raccolta durante la rimozione degli elementi perché quando si rimuove un elemento da una raccolta, il puntatore alla raccolta viene spostato nell'elemento successivo.</span><span class="sxs-lookup"><span data-stu-id="2fea9-127">You cannot iterate a collection while removing items because when you remove an element from a collection, the collection pointer is moved to the next element.</span></span> <span data-ttu-id="2fea9-128">Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="2fea9-128">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2fea9-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fea9-129">Requirements</span></span>



| <span data-ttu-id="2fea9-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fea9-130">Requirement</span></span> | <span data-ttu-id="2fea9-131">Valore</span><span class="sxs-lookup"><span data-stu-id="2fea9-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fea9-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fea9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2fea9-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fea9-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2fea9-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fea9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2fea9-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fea9-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2fea9-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2fea9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fea9-137"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fea9-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2fea9-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2fea9-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="2fea9-139"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2fea9-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2fea9-140">DLL</span><span class="sxs-lookup"><span data-stu-id="2fea9-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fea9-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fea9-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2fea9-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="2fea9-142">CLSID</span></span><br/>                    | <span data-ttu-id="2fea9-143">\_Dell'SWBEMQUALIFIERSET CLSID</span><span class="sxs-lookup"><span data-stu-id="2fea9-143">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="2fea9-144">IID</span><span class="sxs-lookup"><span data-stu-id="2fea9-144">IID</span></span><br/>                      | <span data-ttu-id="2fea9-145">\_ISWBEMQUALIFIERSET IID</span><span class="sxs-lookup"><span data-stu-id="2fea9-145">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="2fea9-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2fea9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fea9-147">**Dell'SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="2fea9-147">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="2fea9-148">**Dell'SWbemQualifierSet. Add**</span><span class="sxs-lookup"><span data-stu-id="2fea9-148">**SWbemQualifierSet.Add**</span></span>](swbemqualifierset-add.md)
</dt> </dl>

 

 




