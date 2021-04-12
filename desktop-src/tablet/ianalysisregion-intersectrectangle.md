---
description: Limita l'area di questo IAnalysisRegion all'area creata dalla relativa intersezione con il rettangolo specificato.
ms.assetid: de6b565f-34c1-4551-ab92-db6bacb8608d
title: 'Metodo IAnalysisRegion:: IntersectRectangle (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4ce0e514b24aba0331d9ea604333680db1c67c8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526556"
---
# <a name="ianalysisregionintersectrectangle-method"></a><span data-ttu-id="a2e87-103">Metodo IAnalysisRegion:: IntersectRectangle</span><span class="sxs-lookup"><span data-stu-id="a2e87-103">IAnalysisRegion::IntersectRectangle method</span></span>

<span data-ttu-id="a2e87-104">Limita l'area di questo [**IAnalysisRegion**](ianalysisregion.md) all'area creata dalla relativa intersezione con il rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="a2e87-104">Restricts the area of this [**IAnalysisRegion**](ianalysisregion.md) to the area created by its intersection with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2e87-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2e87-105">Syntax</span></span>


```C++
HRESULT IntersectRectangle(
  [in] RECT *pIntersectingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="a2e87-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2e87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2e87-107">*pIntersectingRectangle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2e87-107">*pIntersectingRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2e87-108">Puntatore al rettangolo con cui intersecare le coordinate dello spazio input penna.</span><span class="sxs-lookup"><span data-stu-id="a2e87-108">A pointer to the rectangle with which to intersect, in ink-space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2e87-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a2e87-109">Return value</span></span>

<span data-ttu-id="a2e87-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a2e87-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a2e87-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2e87-111">Remarks</span></span>

<span data-ttu-id="a2e87-112">Le coordinate del rettangolo sono espresse in unità HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="a2e87-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="a2e87-113">Se le due aree non si intersecano, la nuova area è vuota.</span><span class="sxs-lookup"><span data-stu-id="a2e87-113">If the two areas do not intersect, the new area is empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2e87-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2e87-114">Requirements</span></span>



| <span data-ttu-id="a2e87-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2e87-115">Requirement</span></span> | <span data-ttu-id="a2e87-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a2e87-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2e87-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2e87-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a2e87-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a2e87-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a2e87-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2e87-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a2e87-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a2e87-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a2e87-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2e87-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2e87-122"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a2e87-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a2e87-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a2e87-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2e87-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2e87-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a2e87-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2e87-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2e87-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="a2e87-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="a2e87-127">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="a2e87-127">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="a2e87-128">**Metodo IAnalysisRegion:: ExcludeRegion**</span><span class="sxs-lookup"><span data-stu-id="a2e87-128">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="a2e87-129">**Metodo IAnalysisRegion:: IntersectRegion**</span><span class="sxs-lookup"><span data-stu-id="a2e87-129">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="a2e87-130">**Metodo IAnalysisRegion:: UnionRectangle**</span><span class="sxs-lookup"><span data-stu-id="a2e87-130">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="a2e87-131">**Metodo IAnalysisRegion:: UnionRegion**</span><span class="sxs-lookup"><span data-stu-id="a2e87-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="a2e87-132">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="a2e87-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




