---
description: Ottiene il rettangolo di delimitazione di IAnalysisRegion.
ms.assetid: 6b9deff7-12e9-4b30-86cb-25b94737d28d
title: 'Metodo IAnalysisRegion:: GetBounds (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetBounds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 12bbb8163aa866648a83effc75d668bc4032c8d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751874"
---
# <a name="ianalysisregiongetbounds-method"></a><span data-ttu-id="ac79d-103">Metodo IAnalysisRegion:: GetBounds</span><span class="sxs-lookup"><span data-stu-id="ac79d-103">IAnalysisRegion::GetBounds method</span></span>

<span data-ttu-id="ac79d-104">Ottiene il rettangolo di delimitazione di [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="ac79d-104">Gets the bounding rectangle of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ac79d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac79d-105">Syntax</span></span>


```C++
HRESULT GetBounds(
  [out] RECT *pBoundingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="ac79d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac79d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac79d-107">*pBoundingRectangle* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ac79d-107">*pBoundingRectangle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac79d-108">Rettangolo di delimitazione di [**IAnalysisRegion**](ianalysisregion.md) nelle coordinate dello spazio di input penna.</span><span class="sxs-lookup"><span data-stu-id="ac79d-108">The bounding rectangle of the [**IAnalysisRegion**](ianalysisregion.md) in ink space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac79d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac79d-109">Return value</span></span>

<span data-ttu-id="ac79d-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ac79d-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ac79d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac79d-111">Remarks</span></span>

<span data-ttu-id="ac79d-112">I limiti si trovano nelle coordinate dello spazio input penna.</span><span class="sxs-lookup"><span data-stu-id="ac79d-112">The bounds are in ink-space coordinates.</span></span>

<span data-ttu-id="ac79d-113">Se il [**IAnalysisRegion**](ianalysisregion.md) rappresenta un'area infinita, i limiti sinistro e superiore sono di **tipo int \_ min**, mentre i limiti destro e inferiore sono di **tipo int \_ Max**.</span><span class="sxs-lookup"><span data-stu-id="ac79d-113">If the [**IAnalysisRegion**](ianalysisregion.md) represents an infinite area, the left and top bounds are **INT\_MIN**; and the right and bottom bounds are **INT\_MAX**.</span></span>

<span data-ttu-id="ac79d-114">Se [**IAnalysisRegion**](ianalysisregion.md) rappresenta un'area vuota, tutti i limiti del rettangolo sono pari a 0.</span><span class="sxs-lookup"><span data-stu-id="ac79d-114">If the [**IAnalysisRegion**](ianalysisregion.md) represents an empty area, all the bounds of the rectangle are 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac79d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac79d-115">Requirements</span></span>



| <span data-ttu-id="ac79d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac79d-116">Requirement</span></span> | <span data-ttu-id="ac79d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ac79d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac79d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac79d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ac79d-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ac79d-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ac79d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac79d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ac79d-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ac79d-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ac79d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac79d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac79d-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ac79d-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ac79d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ac79d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac79d-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac79d-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ac79d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac79d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac79d-127">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="ac79d-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="ac79d-128">**Metodo IAnalysisRegion:: GetRegionScans**</span><span class="sxs-lookup"><span data-stu-id="ac79d-128">**IAnalysisRegion::GetRegionScans Method**</span></span>](ianalysisregion-getregionscans.md)
</dt> <dt>

[<span data-ttu-id="ac79d-129">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="ac79d-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




