---
description: Limita l'area di IAnalysisRegion all'area creata dalla relativa intersezione con il IAnalysisRegion specificato.
ms.assetid: 02b3049f-ada9-4de3-a7a2-f9ff8313fbab
title: 'Metodo IAnalysisRegion:: IntersectRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7ff3caad382e54f41685f6102edafdeb86b813c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307465"
---
# <a name="ianalysisregionintersectregion-method"></a><span data-ttu-id="54eac-103">Metodo IAnalysisRegion:: IntersectRegion</span><span class="sxs-lookup"><span data-stu-id="54eac-103">IAnalysisRegion::IntersectRegion method</span></span>

<span data-ttu-id="54eac-104">Limita l'area di [**IAnalysisRegion**](ianalysisregion.md) all'area creata dalla relativa intersezione con il **IAnalysisRegion** specificato.</span><span class="sxs-lookup"><span data-stu-id="54eac-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the area created by its intersection with the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="54eac-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54eac-105">Syntax</span></span>


```C++
HRESULT IntersectRegion(
  [in] IAnalysisRegion *pRegionToIntersect
);
```



## <a name="parameters"></a><span data-ttu-id="54eac-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="54eac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54eac-107">*pRegionToIntersect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54eac-107">*pRegionToIntersect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54eac-108">[**IAnalysisRegion**](ianalysisregion.md) con cui intersecare.</span><span class="sxs-lookup"><span data-stu-id="54eac-108">The [**IAnalysisRegion**](ianalysisregion.md) with which to intersect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54eac-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="54eac-109">Return value</span></span>

<span data-ttu-id="54eac-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="54eac-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="54eac-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="54eac-111">Remarks</span></span>

<span data-ttu-id="54eac-112">Se le due aree non si intersecano, la nuova area è vuota.</span><span class="sxs-lookup"><span data-stu-id="54eac-112">If the two areas do not intersect, the new area is empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="54eac-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54eac-113">Requirements</span></span>



| <span data-ttu-id="54eac-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="54eac-114">Requirement</span></span> | <span data-ttu-id="54eac-115">Valore</span><span class="sxs-lookup"><span data-stu-id="54eac-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54eac-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54eac-116">Minimum supported client</span></span><br/> | <span data-ttu-id="54eac-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="54eac-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="54eac-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54eac-118">Minimum supported server</span></span><br/> | <span data-ttu-id="54eac-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="54eac-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="54eac-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54eac-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="54eac-121"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="54eac-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="54eac-122">DLL</span><span class="sxs-lookup"><span data-stu-id="54eac-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54eac-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54eac-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="54eac-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54eac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54eac-125">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="54eac-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="54eac-126">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="54eac-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="54eac-127">**Metodo IAnalysisRegion:: ExcludeRegion**</span><span class="sxs-lookup"><span data-stu-id="54eac-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="54eac-128">**Metodo IAnalysisRegion:: IntersectRectangle**</span><span class="sxs-lookup"><span data-stu-id="54eac-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="54eac-129">**Metodo IAnalysisRegion:: UnionRectangle**</span><span class="sxs-lookup"><span data-stu-id="54eac-129">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="54eac-130">**Metodo IAnalysisRegion:: UnionRegion**</span><span class="sxs-lookup"><span data-stu-id="54eac-130">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="54eac-131">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="54eac-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




