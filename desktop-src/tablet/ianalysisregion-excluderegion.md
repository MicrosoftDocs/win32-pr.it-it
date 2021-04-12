---
description: Limita l'area di IAnalysisRegion alla parte dell'area che non interseca il IAnalysisRegion specificato.
ms.assetid: 7a11d2a8-c2ca-4088-b932-8a6c3e789b7f
title: 'Metodo IAnalysisRegion:: ExcludeRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13324d872a76a9184e6ea67b227dbd7444684bb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526557"
---
# <a name="ianalysisregionexcluderegion-method"></a><span data-ttu-id="0efa1-103">Metodo IAnalysisRegion:: ExcludeRegion</span><span class="sxs-lookup"><span data-stu-id="0efa1-103">IAnalysisRegion::ExcludeRegion method</span></span>

<span data-ttu-id="0efa1-104">Limita l'area di [**IAnalysisRegion**](ianalysisregion.md) alla parte dell'area che non interseca il **IAnalysisRegion** specificato.</span><span class="sxs-lookup"><span data-stu-id="0efa1-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the portion of its area that does not intersect the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0efa1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0efa1-105">Syntax</span></span>


```C++
HRESULT ExcludeRegion(
  [in] IAnalysisRegion *pRegionToExclude
);
```



## <a name="parameters"></a><span data-ttu-id="0efa1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0efa1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0efa1-107">*pRegionToExclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0efa1-107">*pRegionToExclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0efa1-108">[**IAnalysisRegion**](ianalysisregion.md) da escludere da questo **IAnalysisRegion**.</span><span class="sxs-lookup"><span data-stu-id="0efa1-108">The [**IAnalysisRegion**](ianalysisregion.md) to exclude from this **IAnalysisRegion**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0efa1-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0efa1-109">Return value</span></span>

<span data-ttu-id="0efa1-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0efa1-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0efa1-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="0efa1-111">Remarks</span></span>

<span data-ttu-id="0efa1-112">Se le due aree non si intersecano, questo [**IAnalysisRegion**](ianalysisregion.md) è invariato.</span><span class="sxs-lookup"><span data-stu-id="0efa1-112">If the two areas do not intersect, this [**IAnalysisRegion**](ianalysisregion.md) is unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="0efa1-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0efa1-113">Requirements</span></span>



| <span data-ttu-id="0efa1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0efa1-114">Requirement</span></span> | <span data-ttu-id="0efa1-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0efa1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0efa1-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0efa1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0efa1-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0efa1-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0efa1-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0efa1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0efa1-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0efa1-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0efa1-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0efa1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0efa1-121"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0efa1-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0efa1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0efa1-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0efa1-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0efa1-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0efa1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0efa1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0efa1-125">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="0efa1-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="0efa1-126">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="0efa1-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="0efa1-127">**Metodo IAnalysisRegion:: IntersectRectangle**</span><span class="sxs-lookup"><span data-stu-id="0efa1-127">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="0efa1-128">**Metodo IAnalysisRegion:: IntersectRegion**</span><span class="sxs-lookup"><span data-stu-id="0efa1-128">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="0efa1-129">**Metodo IAnalysisRegion:: UnionRectangle**</span><span class="sxs-lookup"><span data-stu-id="0efa1-129">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="0efa1-130">**Metodo IAnalysisRegion:: UnionRegion**</span><span class="sxs-lookup"><span data-stu-id="0efa1-130">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="0efa1-131">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="0efa1-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




