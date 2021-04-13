---
description: Il metodo Item dell'oggetto SWbemNamedValueSet ottiene un oggetto SWbemNamedValue dalla raccolta.
ms.assetid: ccebe65e-6032-43d5-9004-2247c3b96d6d
ms.tgt_platform: multiple
title: Metodo SWbemNamedValueSet. Item (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a4932409fa7b8ac9e0f326e5de7e8ecf0f89c2b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528477"
---
# <a name="swbemnamedvaluesetitem-method"></a><span data-ttu-id="a330c-103">Metodo SWbemNamedValueSet. Item</span><span class="sxs-lookup"><span data-stu-id="a330c-103">SWbemNamedValueSet.Item method</span></span>

<span data-ttu-id="a330c-104">Il metodo **Item** dell'oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) ottiene un oggetto [**SWbemNamedValue**](swbemnamedvalue.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="a330c-104">The **Item** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object gets an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span>

<span data-ttu-id="a330c-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a330c-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a330c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a330c-106">Syntax</span></span>


```VB
objNamedValue = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a330c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a330c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a330c-108">*strName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a330c-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a330c-109">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a330c-109">Required.</span></span> <span data-ttu-id="a330c-110">Nome del valore da recuperare.</span><span class="sxs-lookup"><span data-stu-id="a330c-110">Name of the value to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="a330c-111">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="a330c-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a330c-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="a330c-112">Reserved.</span></span> <span data-ttu-id="a330c-113">Se specificato, questo valore deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a330c-113">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a330c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a330c-114">Return value</span></span>

<span data-ttu-id="a330c-115">Se l'esito è positivo, viene restituito l'oggetto [**SWbemNamedValue**](swbemnamedvalue.md) richiesto.</span><span class="sxs-lookup"><span data-stu-id="a330c-115">If successful, the requested [**SWbemNamedValue**](swbemnamedvalue.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a330c-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a330c-116">Error codes</span></span>

<span data-ttu-id="a330c-117">Al termine del metodo **Item** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="a330c-117">Upon completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="a330c-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="a330c-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="a330c-119">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="a330c-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="a330c-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="a330c-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="a330c-121">È stato specificato un parametro non valido o non è stato possibile analizzare lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a330c-121">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="a330c-122">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="a330c-122">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="a330c-123">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="a330c-123">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a330c-124">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="a330c-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="a330c-125">Elemento richiesto non trovato.</span><span class="sxs-lookup"><span data-stu-id="a330c-125">The requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a330c-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="a330c-126">Remarks</span></span>

<span data-ttu-id="a330c-127">Per esempi relativi all'aggiunta e al recupero di valori denominati, vedere [**SWbemNamedValue. Value**](swbemnamedvalue-value.md).</span><span class="sxs-lookup"><span data-stu-id="a330c-127">For examples of adding and retrieving named values, see [**SWbemNamedValue.Value**](swbemnamedvalue-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a330c-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a330c-128">Requirements</span></span>



| <span data-ttu-id="a330c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a330c-129">Requirement</span></span> | <span data-ttu-id="a330c-130">Valore</span><span class="sxs-lookup"><span data-stu-id="a330c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a330c-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a330c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a330c-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a330c-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a330c-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a330c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a330c-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a330c-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a330c-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a330c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a330c-136"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a330c-136"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a330c-137">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a330c-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="a330c-138"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a330c-138"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a330c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a330c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a330c-140"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a330c-140"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a330c-141">CLSID</span><span class="sxs-lookup"><span data-stu-id="a330c-141">CLSID</span></span><br/>                    | <span data-ttu-id="a330c-142">\_SWBEMNAMEDVALUESET CLSID</span><span class="sxs-lookup"><span data-stu-id="a330c-142">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="a330c-143">IID</span><span class="sxs-lookup"><span data-stu-id="a330c-143">IID</span></span><br/>                      | <span data-ttu-id="a330c-144">\_ISWBEMNAMEDVALUESET IID</span><span class="sxs-lookup"><span data-stu-id="a330c-144">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="a330c-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a330c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a330c-146">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="a330c-146">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




