---
title: Funzione UtilAssembleStringsWithAlloc (Ndattributils. h)
description: Alloca una stringa e la formatta usando le stringhe fornite dalla tabella delle stringhe. Questa funzione USA StringCchPrintf per creare la stringa formattata.
ms.assetid: eedc2874-b949-4cc2-ba7c-ebf1924f1156
keywords:
- UtilAssembleStringsWithAlloc funzione NDF
topic_type:
- apiref
api_name:
- UtilAssembleStringsWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dae121b1d5f2d968f696190c64828be91adc71da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743882"
---
# <a name="utilassemblestringswithalloc-function"></a><span data-ttu-id="52cb5-105">UtilAssembleStringsWithAlloc (funzione)</span><span class="sxs-lookup"><span data-stu-id="52cb5-105">UtilAssembleStringsWithAlloc function</span></span>

<span data-ttu-id="52cb5-106">La funzione **UtilAssembleStringsWithAlloc** alloca una stringa e la formatta usando le stringhe fornite dalla tabella delle stringhe.</span><span class="sxs-lookup"><span data-stu-id="52cb5-106">The **UtilAssembleStringsWithAlloc** function allocates a string and formats it using strings provided by the string table.</span></span> <span data-ttu-id="52cb5-107">Questa funzione usa [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) per creare la stringa formattata.</span><span class="sxs-lookup"><span data-stu-id="52cb5-107">This function uses [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) to create the formatted string.</span></span>

## <a name="syntax"></a><span data-ttu-id="52cb5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52cb5-108">Syntax</span></span>


```C++
HRESULT UtilAssembleStringsWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR InputFormat,
  _In_  LPCWSTR InputString,
  _In_  BOOLEAN AdditionalArgument,
  _In_  ULONG   AdditionalValue
);
```



## <a name="parameters"></a><span data-ttu-id="52cb5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="52cb5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52cb5-110">*Buffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="52cb5-110">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52cb5-111">Tipo: \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="52cb5-111">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="52cb5-112">Posizione in cui verrà posizionata la stringa appena allocata.</span><span class="sxs-lookup"><span data-stu-id="52cb5-112">The location where the newly allocated string will be placed.</span></span> <span data-ttu-id="52cb5-113">Quando la stringa non è più necessaria, deve essere rilasciata con [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="52cb5-113">When the string is no longer needed, it must be released with [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="52cb5-114">*BufferMax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52cb5-114">*BufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52cb5-115">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="52cb5-115">Type: **UINT**</span></span>

<span data-ttu-id="52cb5-116">Numero massimo di caratteri consentiti nella stringa allocata dal *buffer*.</span><span class="sxs-lookup"><span data-stu-id="52cb5-116">The maximum number of characters allowed in the string allocated by *Buffer*.</span></span> <span data-ttu-id="52cb5-117">Se la stringa formattata risultante supera il numero di caratteri specificato, viene troncata e terminata con null.</span><span class="sxs-lookup"><span data-stu-id="52cb5-117">If the resulting formatted string is longer than the number of characters specified, it is truncated and null-terminated.</span></span>

> [!Note]  
> <span data-ttu-id="52cb5-118">Questo parametro non può essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="52cb5-118">This parameter may not be set to zero.</span></span>

 

</dd> <dt>

<span data-ttu-id="52cb5-119">*InputFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52cb5-119">*InputFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52cb5-120">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="52cb5-120">Type: **LPCWSTR**</span></span>

<span data-ttu-id="52cb5-121">Risorsa di stringa fuori dalla tabella delle stringhe che rappresenta un parametro di formato passato a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa).</span><span class="sxs-lookup"><span data-stu-id="52cb5-121">String resource out of the string table representing a format parameter passed to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa).</span></span> <span data-ttu-id="52cb5-122">Viene costruito usando [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span><span class="sxs-lookup"><span data-stu-id="52cb5-122">It is constructed using [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span></span>

<span data-ttu-id="52cb5-123">Il formato della stringa di risorsa deve specificare un parametro di formato che accetta una stringa di caratteri "wide" oppure un parametro di formato che accetta un valore long senza segno e una stringa di caratteri "wide".</span><span class="sxs-lookup"><span data-stu-id="52cb5-123">The resource string format must specify either a format parameter taking a wide string, or a format parameter taking an unsigned long and a wide string.</span></span>

</dd> <dt>

<span data-ttu-id="52cb5-124">*InputString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52cb5-124">*InputString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52cb5-125">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="52cb5-125">Type: **LPCWSTR**</span></span>

<span data-ttu-id="52cb5-126">Risorsa di tipo stringa fuori dalla tabella delle stringhe che rappresenta un argomento passato a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) al posto della stringa estesa nel parametro format.</span><span class="sxs-lookup"><span data-stu-id="52cb5-126">String resource out of the string table representing an argument passed to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) in place of the wide string in the format parameter.</span></span> <span data-ttu-id="52cb5-127">Viene costruito usando [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span><span class="sxs-lookup"><span data-stu-id="52cb5-127">It is constructed using [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span></span>

</dd> <dt>

<span data-ttu-id="52cb5-128">*AdditionalArgument* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52cb5-128">*AdditionalArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52cb5-129">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="52cb5-129">Type: **BOOLEAN**</span></span>

<span data-ttu-id="52cb5-130">True se *AdditionalValue* deve essere passato come primo argomento di formattazione a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa); in caso contrario, false (verrà passata solo la stringa di risorsa identificata da *InputString* ).</span><span class="sxs-lookup"><span data-stu-id="52cb5-130">True if *AdditionalValue* should be passed in as the first formatting argument to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa); otherwise, false (and only the resource string identified by *InputString* will be passed).</span></span>

</dd> <dt>

<span data-ttu-id="52cb5-131">*AdditionalValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52cb5-131">*AdditionalValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52cb5-132">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="52cb5-132">Type: **ULONG**</span></span>

<span data-ttu-id="52cb5-133">Valore da passare come primo argomento di formattazione a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) se *AdditionalArgument* è true.</span><span class="sxs-lookup"><span data-stu-id="52cb5-133">The value to pass as the first formatting argument to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) if *AdditionalArgument* is true.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52cb5-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52cb5-134">Return value</span></span>

<span data-ttu-id="52cb5-135">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="52cb5-135">Type: **HRESULT**</span></span>

<span data-ttu-id="52cb5-136">I valori restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="52cb5-136">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="52cb5-137">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="52cb5-137">Return code</span></span>                                                                                  | <span data-ttu-id="52cb5-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52cb5-138">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="52cb5-139"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="52cb5-139"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="52cb5-140">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="52cb5-140">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="52cb5-141"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="52cb5-141"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="52cb5-142">Uno o più parametri non sono stati specificati correttamente.</span><span class="sxs-lookup"><span data-stu-id="52cb5-142">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="52cb5-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52cb5-143">Requirements</span></span>



| <span data-ttu-id="52cb5-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="52cb5-144">Requirement</span></span> | <span data-ttu-id="52cb5-145">Valore</span><span class="sxs-lookup"><span data-stu-id="52cb5-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="52cb5-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52cb5-146">Minimum supported client</span></span><br/> | <span data-ttu-id="52cb5-147">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="52cb5-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="52cb5-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52cb5-148">Minimum supported server</span></span><br/> | <span data-ttu-id="52cb5-149">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="52cb5-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="52cb5-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52cb5-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="52cb5-151"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="52cb5-151"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52cb5-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52cb5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52cb5-153">**UtilStringCopyWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="52cb5-153">**UtilStringCopyWithAlloc**</span></span>](utilstringcopywithalloc.md)
</dt> <dt>

[<span data-ttu-id="52cb5-154">**UtilLoadStringWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="52cb5-154">**UtilLoadStringWithAlloc**</span></span>](utilloadstringwithalloc.md)
</dt> <dt>

[<span data-ttu-id="52cb5-155">**StringCchPrintf**</span><span class="sxs-lookup"><span data-stu-id="52cb5-155">**StringCchPrintf**</span></span>](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)
</dt> <dt>

[<span data-ttu-id="52cb5-156">**MAKEINTRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="52cb5-156">**MAKEINTRESOURCE**</span></span>](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)
</dt> <dt>

[<span data-ttu-id="52cb5-157">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="52cb5-157">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

