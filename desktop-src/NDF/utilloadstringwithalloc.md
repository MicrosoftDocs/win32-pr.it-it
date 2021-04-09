---
title: Funzione UtilLoadStringWithAlloc (Ndattributils. h)
description: Alloca e carica una stringa fuori dalla tabella delle risorse.
ms.assetid: 34bf0b93-2bec-49c3-9441-c83686c4abdb
keywords:
- UtilLoadStringWithAlloc funzione NDF
topic_type:
- apiref
api_name:
- UtilLoadStringWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e13930fe9bb11ae9c9456152c823491eabc462
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121651"
---
# <a name="utilloadstringwithalloc-function"></a><span data-ttu-id="b4eb1-104">UtilLoadStringWithAlloc (funzione)</span><span class="sxs-lookup"><span data-stu-id="b4eb1-104">UtilLoadStringWithAlloc function</span></span>

<span data-ttu-id="b4eb1-105">La funzione **UtilLoadStringWithAlloc** alloca e carica una stringa fuori dalla tabella delle risorse.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-105">The **UtilLoadStringWithAlloc** function allocates and loads a string out of the resource table.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4eb1-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4eb1-106">Syntax</span></span>


```C++
HRESULT UtilLoadStringWithAlloc(
  _In_  UINT   uID,
  _Out_ LPWSTR *ppwzBuffer,
  _In_  UINT   cchBufferMax
);
```



## <a name="parameters"></a><span data-ttu-id="b4eb1-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4eb1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4eb1-108">*uID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4eb1-108">*uID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4eb1-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b4eb1-109">Type: **UINT**</span></span>

<span data-ttu-id="b4eb1-110">Identificatore della stringa da caricare.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-110">Identifier of of the string to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="b4eb1-111">*ppwzBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b4eb1-111">*ppwzBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4eb1-112">Tipo: \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="b4eb1-112">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="b4eb1-113">Posizione in cui verrà posizionata la stringa appena allocata.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-113">The location where the newly allocated string will be placed.</span></span> <span data-ttu-id="b4eb1-114">La stringa deve essere liberata usando [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) quando non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-114">The string must be freed using [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) when it is no longer needed.</span></span>

</dd> <dt>

<span data-ttu-id="b4eb1-115">*cchBufferMax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4eb1-115">*cchBufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4eb1-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b4eb1-116">Type: **UINT**</span></span>

<span data-ttu-id="b4eb1-117">Numero massimo di caratteri da caricare dalla tabella delle risorse.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-117">The maximum number of characters to load from the resource table.</span></span> <span data-ttu-id="b4eb1-118">Se la stringa di risorsa supera il numero di caratteri specificato, viene troncata e terminata con null.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-118">If the resource string is longer than the number of characters specified, it is truncated and null-terminated.</span></span>

> [!Note]  
> <span data-ttu-id="b4eb1-119">Questo parametro non può essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-119">This parameter may not be set to zero.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4eb1-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4eb1-120">Return value</span></span>

<span data-ttu-id="b4eb1-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b4eb1-121">Type: **HRESULT**</span></span>

<span data-ttu-id="b4eb1-122">I valori restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-122">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="b4eb1-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b4eb1-123">Return code</span></span>                                                                                  | <span data-ttu-id="b4eb1-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4eb1-124">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b4eb1-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b4eb1-125"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="b4eb1-126">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-126">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="b4eb1-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b4eb1-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="b4eb1-128">Uno o più parametri non sono stati specificati correttamente.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-128">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b4eb1-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4eb1-129">Requirements</span></span>



| <span data-ttu-id="b4eb1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4eb1-130">Requirement</span></span> | <span data-ttu-id="b4eb1-131">Valore</span><span class="sxs-lookup"><span data-stu-id="b4eb1-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4eb1-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4eb1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b4eb1-133">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b4eb1-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b4eb1-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4eb1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b4eb1-135">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b4eb1-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b4eb1-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4eb1-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4eb1-137"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4eb1-137"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4eb1-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4eb1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4eb1-139">**UtilStringCopyWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="b4eb1-139">**UtilStringCopyWithAlloc**</span></span>](utilstringcopywithalloc.md)
</dt> <dt>

[<span data-ttu-id="b4eb1-140">**UtilAssembleStringsWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="b4eb1-140">**UtilAssembleStringsWithAlloc**</span></span>](utilassemblestringswithalloc.md)
</dt> <dt>

[<span data-ttu-id="b4eb1-141">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="b4eb1-141">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

