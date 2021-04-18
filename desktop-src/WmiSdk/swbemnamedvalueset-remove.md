---
description: Il metodo Remove dell'oggetto SWbemNamedValueSet Elimina un valore denominato dal contesto.
ms.assetid: 8cb353fb-c6d7-41d9-a2d0-ff1ad37264e4
ms.tgt_platform: multiple
title: Metodo SWbemNamedValueSet. Remove (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d41ecd7d28b95534c8e6d88d1c57756c269cf790
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316560"
---
# <a name="swbemnamedvaluesetremove-method"></a><span data-ttu-id="5a5c9-103">Metodo SWbemNamedValueSet. Remove</span><span class="sxs-lookup"><span data-stu-id="5a5c9-103">SWbemNamedValueSet.Remove method</span></span>

<span data-ttu-id="5a5c9-104">Il metodo **Remove** dell'oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) Elimina un valore denominato dal contesto.</span><span class="sxs-lookup"><span data-stu-id="5a5c9-104">The **Remove** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object deletes a named value from the context.</span></span>

<span data-ttu-id="5a5c9-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5a5c9-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a5c9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a5c9-106">Syntax</span></span>


```VB
SWbemNamedValueSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5a5c9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a5c9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a5c9-108">*strName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a5c9-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a5c9-109">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5a5c9-109">Required.</span></span> <span data-ttu-id="5a5c9-110">Nome del valore da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="5a5c9-110">Name of the value to remove.</span></span>

</dd> <dt>

<span data-ttu-id="5a5c9-111">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5a5c9-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5a5c9-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="5a5c9-112">Reserved.</span></span> <span data-ttu-id="5a5c9-113">Se specificato, questo valore deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5a5c9-113">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a5c9-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a5c9-114">Return value</span></span>

<span data-ttu-id="5a5c9-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="5a5c9-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5a5c9-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="5a5c9-116">Error codes</span></span>

<span data-ttu-id="5a5c9-117">Al termine del metodo **Remove** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="5a5c9-117">Upon completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="5a5c9-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="5a5c9-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="5a5c9-119">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="5a5c9-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="5a5c9-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="5a5c9-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="5a5c9-121">È stato specificato un parametro non valido o non è stato possibile analizzare lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5a5c9-121">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="5a5c9-122">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="5a5c9-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="5a5c9-123">Elemento richiesto non trovato.</span><span class="sxs-lookup"><span data-stu-id="5a5c9-123">The requested item was not found.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a5c9-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a5c9-124">Requirements</span></span>



| <span data-ttu-id="5a5c9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a5c9-125">Requirement</span></span> | <span data-ttu-id="5a5c9-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5a5c9-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a5c9-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a5c9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5a5c9-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a5c9-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5a5c9-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a5c9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5a5c9-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a5c9-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5a5c9-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a5c9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a5c9-132"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a5c9-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a5c9-133">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="5a5c9-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="5a5c9-134"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5a5c9-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5a5c9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5a5c9-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a5c9-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a5c9-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5a5c9-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="5a5c9-137">CLSID</span></span><br/>                    | <span data-ttu-id="5a5c9-138">\_SWBEMNAMEDVALUESET CLSID</span><span class="sxs-lookup"><span data-stu-id="5a5c9-138">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="5a5c9-139">IID</span><span class="sxs-lookup"><span data-stu-id="5a5c9-139">IID</span></span><br/>                      | <span data-ttu-id="5a5c9-140">\_ISWBEMNAMEDVALUESET IID</span><span class="sxs-lookup"><span data-stu-id="5a5c9-140">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="5a5c9-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a5c9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a5c9-142">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="5a5c9-142">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




