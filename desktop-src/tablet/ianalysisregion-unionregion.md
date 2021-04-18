---
description: Espande l'area di questo IAnalysisRegion all'area creata dalla relativa unione con il IAnalysisRegion specificato.
ms.assetid: cc3ec5c6-98ff-442e-a1e8-d1a57752ad56
title: 'Metodo IAnalysisRegion:: UnionRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 587986973c4ae4bebaeed3c031c746bc4f842c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307458"
---
# <a name="ianalysisregionunionregion-method"></a><span data-ttu-id="db033-103">Metodo IAnalysisRegion:: UnionRegion</span><span class="sxs-lookup"><span data-stu-id="db033-103">IAnalysisRegion::UnionRegion method</span></span>

<span data-ttu-id="db033-104">Espande l'area di questo [**IAnalysisRegion**](ianalysisregion.md) all'area creata dalla relativa unione con il **IAnalysisRegion** specificato.</span><span class="sxs-lookup"><span data-stu-id="db033-104">Expands the area of this [**IAnalysisRegion**](ianalysisregion.md) to the area created by its union with the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="db033-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db033-105">Syntax</span></span>


```C++
HRESULT UnionRegion(
  [in] IAnalysisRegion *pRegionToUnion
);
```



## <a name="parameters"></a><span data-ttu-id="db033-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="db033-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db033-107">*pRegionToUnion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db033-107">*pRegionToUnion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db033-108">[**IAnalysisRegion**](ianalysisregion.md) con cui combinare.</span><span class="sxs-lookup"><span data-stu-id="db033-108">The [**IAnalysisRegion**](ianalysisregion.md) with which to combine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db033-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db033-109">Return value</span></span>

<span data-ttu-id="db033-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="db033-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="db033-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="db033-111">Remarks</span></span>

<span data-ttu-id="db033-112">Se una delle due aree è infinita, anche la nuova area è infinita.</span><span class="sxs-lookup"><span data-stu-id="db033-112">If either area is infinite, the new area is also infinite.</span></span>

## <a name="requirements"></a><span data-ttu-id="db033-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db033-113">Requirements</span></span>



| <span data-ttu-id="db033-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="db033-114">Requirement</span></span> | <span data-ttu-id="db033-115">Valore</span><span class="sxs-lookup"><span data-stu-id="db033-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db033-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db033-116">Minimum supported client</span></span><br/> | <span data-ttu-id="db033-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="db033-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="db033-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db033-118">Minimum supported server</span></span><br/> | <span data-ttu-id="db033-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="db033-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="db033-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db033-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="db033-121"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="db033-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="db033-122">DLL</span><span class="sxs-lookup"><span data-stu-id="db033-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db033-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db033-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="db033-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db033-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db033-125">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="db033-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="db033-126">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="db033-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="db033-127">**Metodo IAnalysisRegion:: ExcludeRegion**</span><span class="sxs-lookup"><span data-stu-id="db033-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="db033-128">**Metodo IAnalysisRegion:: IntersectRectangle**</span><span class="sxs-lookup"><span data-stu-id="db033-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="db033-129">**Metodo IAnalysisRegion:: IntersectRegion**</span><span class="sxs-lookup"><span data-stu-id="db033-129">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="db033-130">**Metodo IAnalysisRegion:: UnionRectangle**</span><span class="sxs-lookup"><span data-stu-id="db033-130">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="db033-131">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="db033-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




