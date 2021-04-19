---
description: Limita l'area di IAnalysisRegion alla parte dell'area che non interseca il rettangolo specificato.
ms.assetid: a35b8bfc-a87a-4e9a-908f-2b13a128d222
title: 'Metodo IAnalysisRegion:: ExcludeRectangle (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 684ce2ceb57c7954c732fb2816aca50fcbae5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307468"
---
# <a name="ianalysisregionexcluderectangle-method"></a><span data-ttu-id="02e38-103">Metodo IAnalysisRegion:: ExcludeRectangle</span><span class="sxs-lookup"><span data-stu-id="02e38-103">IAnalysisRegion::ExcludeRectangle method</span></span>

<span data-ttu-id="02e38-104">Limita l'area di [**IAnalysisRegion**](ianalysisregion.md) alla parte dell'area che non interseca il rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="02e38-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the portion of its area that does not intersect the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="02e38-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02e38-105">Syntax</span></span>


```C++
HRESULT ExcludeRectangle(
  [in] RECT *pExcludingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="02e38-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="02e38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02e38-107">*pExcludingRectangle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02e38-107">*pExcludingRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02e38-108">Rettangolo da escludere da questo [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="02e38-108">The rectangle to exclude from this [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02e38-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02e38-109">Return value</span></span>

<span data-ttu-id="02e38-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="02e38-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="02e38-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="02e38-111">Remarks</span></span>

<span data-ttu-id="02e38-112">Le coordinate del rettangolo sono espresse in unità HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="02e38-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="02e38-113">Se le due aree non si intersecano, [**IAnalysisRegion**](ianalysisregion.md) non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="02e38-113">If the two areas do not intersect, the [**IAnalysisRegion**](ianalysisregion.md) is unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="02e38-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02e38-114">Requirements</span></span>



| <span data-ttu-id="02e38-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="02e38-115">Requirement</span></span> | <span data-ttu-id="02e38-116">Valore</span><span class="sxs-lookup"><span data-stu-id="02e38-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02e38-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02e38-117">Minimum supported client</span></span><br/> | <span data-ttu-id="02e38-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="02e38-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="02e38-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02e38-119">Minimum supported server</span></span><br/> | <span data-ttu-id="02e38-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="02e38-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="02e38-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02e38-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="02e38-122"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="02e38-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="02e38-123">DLL</span><span class="sxs-lookup"><span data-stu-id="02e38-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02e38-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02e38-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="02e38-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02e38-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02e38-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="02e38-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="02e38-127">**Metodo IAnalysisRegion:: ExcludeRegion**</span><span class="sxs-lookup"><span data-stu-id="02e38-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="02e38-128">**Metodo IAnalysisRegion:: IntersectRectangle**</span><span class="sxs-lookup"><span data-stu-id="02e38-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="02e38-129">**Metodo IAnalysisRegion:: IntersectRegion**</span><span class="sxs-lookup"><span data-stu-id="02e38-129">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="02e38-130">**Metodo IAnalysisRegion:: UnionRectangle**</span><span class="sxs-lookup"><span data-stu-id="02e38-130">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="02e38-131">**Metodo IAnalysisRegion:: UnionRegion**</span><span class="sxs-lookup"><span data-stu-id="02e38-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="02e38-132">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="02e38-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




