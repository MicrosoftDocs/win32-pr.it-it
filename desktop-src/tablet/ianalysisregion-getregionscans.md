---
description: Recupera una matrice di rettangoli che definisce l'area di IAnalysisRegion.
ms.assetid: 40de4c27-4b3b-4db3-af08-cb53e638db6b
title: 'Metodo IAnalysisRegion:: GetRegionScans (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetRegionScans
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6cb8db60b5818f5bc2bc38892912e9ec40af1eb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307467"
---
# <a name="ianalysisregiongetregionscans-method"></a><span data-ttu-id="b9891-103">Metodo IAnalysisRegion:: GetRegionScans</span><span class="sxs-lookup"><span data-stu-id="b9891-103">IAnalysisRegion::GetRegionScans method</span></span>

<span data-ttu-id="b9891-104">Recupera una matrice di rettangoli che definisce l'area di [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="b9891-104">Retrieves an array of rectangles that defines the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9891-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9891-105">Syntax</span></span>


```C++
HRESULT GetRegionScans(
  [out] ULONG *pulCount,
  [out] RECT  **pRegionScans
);
```



## <a name="parameters"></a><span data-ttu-id="b9891-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9891-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9891-107">*pulCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b9891-107">*pulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9891-108">Numero di rettangoli restituiti in *pRegionScans*.</span><span class="sxs-lookup"><span data-stu-id="b9891-108">The number of rectangles returned in *pRegionScans*.</span></span>

</dd> <dt>

<span data-ttu-id="b9891-109">*pRegionScans* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b9891-109">*pRegionScans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9891-110">Puntatore a una matrice di rettangoli che definisce l'area di [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="b9891-110">A pointer to an array of rectangles that defines the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9891-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9891-111">Return value</span></span>

<span data-ttu-id="b9891-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b9891-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b9891-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9891-113">Remarks</span></span>

<span data-ttu-id="b9891-114">Se *pRegionScans* viene passato come **null**, il metodo **GetRegionScans** restituisce **S \_ OK** e viene restituito il numero di rettangoli in *pulCount*.</span><span class="sxs-lookup"><span data-stu-id="b9891-114">If *pRegionScans* is passed as **NULL**, the **GetRegionScans** method returns **S\_OK** and the number of rectangles is returned in *pulCount*.</span></span>

> [!Caution]  
> <span data-ttu-id="b9891-115">Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *pRegionScans* quando le informazioni non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="b9891-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pRegionScans* when you no longer need the information.</span></span>

 

<span data-ttu-id="b9891-116">I limiti dei rettangoli si trovano in coordinate di spazio input penna.</span><span class="sxs-lookup"><span data-stu-id="b9891-116">The bounds of the rectangles are in ink-space coordinates.</span></span>

<span data-ttu-id="b9891-117">L'Unione dei rettangoli restituiti rappresenta l'area di [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="b9891-117">The union of the returned rectangles represents the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b9891-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="b9891-118">Examples</span></span>

<span data-ttu-id="b9891-119">Nell'esempio seguente viene illustrato come ottenere i rettangoli che definiscono l'area di [**IAnalysisRegion**](ianalysisregion.md) `region` e come ottenere solo il numero di rettangoli.</span><span class="sxs-lookup"><span data-stu-id="b9891-119">The following example shows how to get the rectangles that define the area of the [**IAnalysisRegion**](ianalysisregion.md), `region` and how to get only the number of rectangles.</span></span>


```C++
// Get the count and the rectangles.
ULONG count = 0;
RECT* rects = 0;
region->GetRegionScans(&count, &rects);

// Use rects

::CoTaskMemFree(rects);

// GetRegionScans just gets the count and returns S_OK
ULONG number = 0;
region->GetRegionScans(&number, NULL); 
```



## <a name="requirements"></a><span data-ttu-id="b9891-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9891-120">Requirements</span></span>



| <span data-ttu-id="b9891-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9891-121">Requirement</span></span> | <span data-ttu-id="b9891-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b9891-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9891-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9891-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b9891-124">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b9891-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b9891-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9891-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b9891-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b9891-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b9891-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9891-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9891-128"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b9891-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b9891-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b9891-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9891-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9891-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b9891-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9891-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9891-132">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="b9891-132">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="b9891-133">**Metodo IAnalysisRegion:: GetBounds**</span><span class="sxs-lookup"><span data-stu-id="b9891-133">**IAnalysisRegion::GetBounds Method**</span></span>](ianalysisregion-getbounds.md)
</dt> <dt>

[<span data-ttu-id="b9891-134">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="b9891-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

