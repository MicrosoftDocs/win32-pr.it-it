---
title: Funzione UtilStringCopyWithAlloc (Ndattributils. h)
description: Alloca e copia una stringa di origine.
ms.assetid: e1400ae1-0edd-4b59-af03-3da1b9d7073b
keywords:
- UtilStringCopyWithAlloc funzione NDF
topic_type:
- apiref
api_name:
- UtilStringCopyWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68bd1815ff09473f0431dde19a12a87603a9dec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301357"
---
# <a name="utilstringcopywithalloc-function"></a><span data-ttu-id="00d4f-104">UtilStringCopyWithAlloc (funzione)</span><span class="sxs-lookup"><span data-stu-id="00d4f-104">UtilStringCopyWithAlloc function</span></span>

<span data-ttu-id="00d4f-105">La funzione **UtilStringCopyWithAlloc** alloca e copia una stringa di origine.</span><span class="sxs-lookup"><span data-stu-id="00d4f-105">The **UtilStringCopyWithAlloc** function allocates and copies a source string.</span></span>

## <a name="syntax"></a><span data-ttu-id="00d4f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00d4f-106">Syntax</span></span>


```C++
HRESULT UtilStringCopyWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR Source
);
```



## <a name="parameters"></a><span data-ttu-id="00d4f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="00d4f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00d4f-108">*Buffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="00d4f-108">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00d4f-109">Tipo: \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="00d4f-109">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="00d4f-110">Posizione in cui è archiviato il puntatore alla memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="00d4f-110">The location where the pointer to the allocated memory is stored.</span></span> <span data-ttu-id="00d4f-111">Quando non è più necessario, è necessario rilasciarlo con [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="00d4f-111">When no longer needed, it must be released with [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span> <span data-ttu-id="00d4f-112">Questo buffer è sempre con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="00d4f-112">This buffer is always null-terminated.</span></span>

</dd> <dt>

<span data-ttu-id="00d4f-113">*BufferMax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00d4f-113">*BufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00d4f-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="00d4f-114">Type: **UINT**</span></span>

<span data-ttu-id="00d4f-115">Numero massimo di caratteri da leggere dall' *origine*.</span><span class="sxs-lookup"><span data-stu-id="00d4f-115">The maximum number of characters to read from *Source*.</span></span>

</dd> <dt>

<span data-ttu-id="00d4f-116">*Origine* \[ dati in\]</span><span class="sxs-lookup"><span data-stu-id="00d4f-116">*Source* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00d4f-117">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="00d4f-117">Type: **LPCWSTR**</span></span>

<span data-ttu-id="00d4f-118">Stringa da copiare.</span><span class="sxs-lookup"><span data-stu-id="00d4f-118">The string to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00d4f-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00d4f-119">Return value</span></span>

<span data-ttu-id="00d4f-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="00d4f-120">Type: **HRESULT**</span></span>

<span data-ttu-id="00d4f-121">I valori restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="00d4f-121">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="00d4f-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="00d4f-122">Return code</span></span>                                                                                  | <span data-ttu-id="00d4f-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00d4f-123">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="00d4f-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="00d4f-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="00d4f-125">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="00d4f-125">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="00d4f-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="00d4f-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="00d4f-127">Uno o più parametri non sono stati specificati correttamente.</span><span class="sxs-lookup"><span data-stu-id="00d4f-127">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="00d4f-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00d4f-128">Requirements</span></span>



| <span data-ttu-id="00d4f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="00d4f-129">Requirement</span></span> | <span data-ttu-id="00d4f-130">Valore</span><span class="sxs-lookup"><span data-stu-id="00d4f-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d4f-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00d4f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="00d4f-132">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="00d4f-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="00d4f-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00d4f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="00d4f-134">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="00d4f-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="00d4f-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00d4f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="00d4f-136"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="00d4f-136"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00d4f-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00d4f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00d4f-138">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="00d4f-138">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> <dt>

[<span data-ttu-id="00d4f-139">**UtilAssembleStringsWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="00d4f-139">**UtilAssembleStringsWithAlloc**</span></span>](utilassemblestringswithalloc.md)
</dt> <dt>

[<span data-ttu-id="00d4f-140">**UtilLoadStringWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="00d4f-140">**UtilLoadStringWithAlloc**</span></span>](utilloadstringwithalloc.md)
</dt> </dl>

 

