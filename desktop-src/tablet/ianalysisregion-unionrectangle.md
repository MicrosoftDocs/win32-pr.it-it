---
description: Espande l'area di questo IAnalysisRegion all'area creata dalla relativa unione con il rettangolo specificato.
ms.assetid: 9b12f509-4f6a-43b0-9639-bef060fd6d50
title: 'Metodo IAnalysisRegion:: UnionRectangle (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3a28a60eae95641225dd9c01791d89a9c38ada82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307459"
---
# <a name="ianalysisregionunionrectangle-method"></a><span data-ttu-id="b5cb6-103">Metodo IAnalysisRegion:: UnionRectangle</span><span class="sxs-lookup"><span data-stu-id="b5cb6-103">IAnalysisRegion::UnionRectangle method</span></span>

<span data-ttu-id="b5cb6-104">Espande l'area di questo [**IAnalysisRegion**](ianalysisregion.md) all'area creata dalla relativa unione con il rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="b5cb6-104">Expands the area of this [**IAnalysisRegion**](ianalysisregion.md) to the area created by its union with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5cb6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5cb6-105">Syntax</span></span>


```C++
HRESULT UnionRectangle(
  [in] RECT *pRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="b5cb6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5cb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5cb6-107">*pRectangle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5cb6-107">*pRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5cb6-108">Puntatore al rettangolo con il quale combinare le coordinate dello spazio input penna.</span><span class="sxs-lookup"><span data-stu-id="b5cb6-108">A pointer to the rectangle with which to combine, in ink-space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5cb6-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5cb6-109">Return value</span></span>

<span data-ttu-id="b5cb6-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b5cb6-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b5cb6-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5cb6-111">Remarks</span></span>

<span data-ttu-id="b5cb6-112">Le coordinate del rettangolo sono espresse in unità HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="b5cb6-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="b5cb6-113">Se una delle due aree è infinita, anche la nuova area è infinita.</span><span class="sxs-lookup"><span data-stu-id="b5cb6-113">If either area is infinite, the new area is also infinite.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5cb6-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5cb6-114">Requirements</span></span>



| <span data-ttu-id="b5cb6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5cb6-115">Requirement</span></span> | <span data-ttu-id="b5cb6-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b5cb6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5cb6-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5cb6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b5cb6-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b5cb6-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b5cb6-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5cb6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b5cb6-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b5cb6-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b5cb6-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5cb6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5cb6-122"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b5cb6-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b5cb6-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b5cb6-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5cb6-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5cb6-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b5cb6-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5cb6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5cb6-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="b5cb6-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="b5cb6-127">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="b5cb6-127">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="b5cb6-128">**Metodo IAnalysisRegion:: ExcludeRegion**</span><span class="sxs-lookup"><span data-stu-id="b5cb6-128">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="b5cb6-129">**Metodo IAnalysisRegion:: IntersectRectangle**</span><span class="sxs-lookup"><span data-stu-id="b5cb6-129">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="b5cb6-130">**Metodo IAnalysisRegion:: IntersectRegion**</span><span class="sxs-lookup"><span data-stu-id="b5cb6-130">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="b5cb6-131">**Metodo IAnalysisRegion:: UnionRegion**</span><span class="sxs-lookup"><span data-stu-id="b5cb6-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="b5cb6-132">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="b5cb6-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




