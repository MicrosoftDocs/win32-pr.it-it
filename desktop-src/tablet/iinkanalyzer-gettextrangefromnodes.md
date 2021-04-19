---
description: Trova l'intervallo di testo nella stringa riconosciuta che corrisponde a una raccolta di oggetti IContextNode.
ms.assetid: 2c5bc4a1-08de-4872-b552-6d22924ce2a8
title: 'Metodo IInkAnalyzer:: GetTextRangeFromNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetTextRangeFromNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da27206a33ca58cebd10192393c4cf2efd1d5919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307380"
---
# <a name="iinkanalyzergettextrangefromnodes-method"></a><span data-ttu-id="41b32-103">Metodo IInkAnalyzer:: GetTextRangeFromNodes</span><span class="sxs-lookup"><span data-stu-id="41b32-103">IInkAnalyzer::GetTextRangeFromNodes method</span></span>

<span data-ttu-id="41b32-104">Trova l'intervallo di testo nella stringa riconosciuta che corrisponde a una raccolta di oggetti [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="41b32-104">Finds the text range in the recognized string that corresponds to a collection of [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="41b32-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41b32-105">Syntax</span></span>


```C++
HRESULT GetTextRangeFromNodes(
  [out] LONG          *plStart,
  [out] LONG          *plLength,
  [in]  IContextNodes *pNodesToSearch
);
```



## <a name="parameters"></a><span data-ttu-id="41b32-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="41b32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41b32-107">*plStart* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="41b32-107">*plStart* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41b32-108">Intero con segno a 32 bit che indica l'inizio dell'intervallo di testo.</span><span class="sxs-lookup"><span data-stu-id="41b32-108">A 32-bit signed integer that indicates the start of the text range.</span></span> <span data-ttu-id="41b32-109">Questo parametro viene passato non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="41b32-109">This parameter is passed uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="41b32-110">*plLength* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="41b32-110">*plLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41b32-111">Intero con segno a 32 bit che indica la lunghezza dell'intervallo di testo.</span><span class="sxs-lookup"><span data-stu-id="41b32-111">A 32-bit signed integer that indicates the length of the text range.</span></span> <span data-ttu-id="41b32-112">Questo parametro viene passato non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="41b32-112">This parameter is passed uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="41b32-113">*pNodesToSearch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41b32-113">*pNodesToSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41b32-114">Raccolta di oggetti [**IContextNode**](icontextnode.md) per i quali trovare l'intervallo di testo.</span><span class="sxs-lookup"><span data-stu-id="41b32-114">The collection of [**IContextNode**](icontextnode.md) objects for which to find the text range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41b32-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41b32-115">Return value</span></span>

<span data-ttu-id="41b32-116">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="41b32-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="41b32-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="41b32-117">Remarks</span></span>

<span data-ttu-id="41b32-118">Se *pNodesToSearch* contiene oggetti [**IContextNode**](icontextnode.md) che non sono adiacenti, questo metodo restituisce l'intervallo di testo più piccolo che copre tutti gli oggetti **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="41b32-118">If *pNodesToSearch* contains [**IContextNode**](icontextnode.md) objects that are not adjacent, this method returns the smallest text range that covers all of the **IContextNode** objects.</span></span>

<span data-ttu-id="41b32-119">Questo metodo genera un' \_ eccezione E INVALIDARG quando *pNodesToSearch* contiene un [**IContextNode**](icontextnode.md) che non è associato a [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="41b32-119">This method throws an E\_INVALIDARG exception when *pNodesToSearch* contains an [**IContextNode**](icontextnode.md) that is not associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="41b32-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41b32-120">Requirements</span></span>



| <span data-ttu-id="41b32-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="41b32-121">Requirement</span></span> | <span data-ttu-id="41b32-122">Valore</span><span class="sxs-lookup"><span data-stu-id="41b32-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41b32-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41b32-123">Minimum supported client</span></span><br/> | <span data-ttu-id="41b32-124">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="41b32-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="41b32-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41b32-125">Minimum supported server</span></span><br/> | <span data-ttu-id="41b32-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="41b32-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="41b32-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41b32-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="41b32-128"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="41b32-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="41b32-129">DLL</span><span class="sxs-lookup"><span data-stu-id="41b32-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41b32-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41b32-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="41b32-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41b32-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41b32-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="41b32-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




