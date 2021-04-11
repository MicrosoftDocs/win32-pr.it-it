---
description: Recupera l'area modificata dall'ultima operazione di analisi.
ms.assetid: 0cd62775-59c6-41f5-957e-709a53a8c257
title: 'Metodo IInkAnalyzer:: GetDirtyRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 56f980189e22f50bb832be904933ef0b26d9b54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226155"
---
# <a name="iinkanalyzergetdirtyregion-method"></a><span data-ttu-id="096ba-103">Metodo IInkAnalyzer:: GetDirtyRegion</span><span class="sxs-lookup"><span data-stu-id="096ba-103">IInkAnalyzer::GetDirtyRegion method</span></span>

<span data-ttu-id="096ba-104">Recupera l'area modificata dall'ultima operazione di analisi.</span><span class="sxs-lookup"><span data-stu-id="096ba-104">Retrieves the area that has changed since the last analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="096ba-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="096ba-105">Syntax</span></span>


```C++
HRESULT GetDirtyRegion(
  [out] IAnalysisRegion **ppDirtyRegion
);
```



## <a name="parameters"></a><span data-ttu-id="096ba-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="096ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="096ba-107">*ppDirtyRegion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="096ba-107">*ppDirtyRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="096ba-108">Oggetto [**IAnalysisRegion**](ianalysisregion.md) che descrive l'area modificata dall'ultima operazione di analisi.</span><span class="sxs-lookup"><span data-stu-id="096ba-108">An [**IAnalysisRegion**](ianalysisregion.md) that describes the area that has changed since the last analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="096ba-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="096ba-109">Return value</span></span>

<span data-ttu-id="096ba-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="096ba-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="096ba-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="096ba-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="096ba-112">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppDirtyRegion* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="096ba-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppDirtyRegion* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="096ba-113">Questo metodo identifica le aree che devono essere analizzate o rianalizzate.</span><span class="sxs-lookup"><span data-stu-id="096ba-113">This method identifies the areas that need to be analyzed or reanalyzed.</span></span> <span data-ttu-id="096ba-114">Tutti i metodi [**IInkAnalyzer**](iinkanalyzer.md) che aggiungono, aggiornano o rimuovono i dati del tratto aggiornano l'area dirty.</span><span class="sxs-lookup"><span data-stu-id="096ba-114">All of the [**IInkAnalyzer**](iinkanalyzer.md) methods that add, update, or remove stroke data update the dirty region.</span></span> <span data-ttu-id="096ba-115">Per contrassegnare manualmente un'area per la rianalisi:</span><span class="sxs-lookup"><span data-stu-id="096ba-115">To manually mark an area for reanalysis:</span></span>

1.  <span data-ttu-id="096ba-116">Ottenere l'area dirty usando il **Metodo IInkAnalyzer:: GetDirtyRegion**.</span><span class="sxs-lookup"><span data-stu-id="096ba-116">Get the dirty region using **IInkAnalyzer::GetDirtyRegion Method**.</span></span>
2.  <span data-ttu-id="096ba-117">Usare il metodo [**IAnalysisRegion:: UnionRegion**](ianalysisregion-unionregion.md) o [**IAnalysisRegion:: UnionRectangle**](ianalysisregion-unionrectangle.md) per aggiungere l'area all'area del passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="096ba-117">Use [**IAnalysisRegion::UnionRegion Method**](ianalysisregion-unionregion.md) or [**IAnalysisRegion::UnionRectangle Method**](ianalysisregion-unionrectangle.md) to add the area to the region from step 1.</span></span>
3.  <span data-ttu-id="096ba-118">Usare il [**Metodo IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) per aggiornare l'area dirty.</span><span class="sxs-lookup"><span data-stu-id="096ba-118">Use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to update the dirty region.</span></span>

<span data-ttu-id="096ba-119">[**IInkAnalyzer**](iinkanalyzer.md) analizza l'input penna all'interno dell'area dirty durante una chiamata al metodo [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="096ba-119">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span> <span data-ttu-id="096ba-120">Tuttavia, **IInkAnalyzer** può espandere l'operazione di analisi per includere le aree adiacenti.</span><span class="sxs-lookup"><span data-stu-id="096ba-120">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="096ba-121">Questa proprietà può contenere aree non adiacenti.</span><span class="sxs-lookup"><span data-stu-id="096ba-121">This property may contain nonadjacent areas.</span></span>

<span data-ttu-id="096ba-122">Usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare la memoria dalla matrice *ppDirtyRegion* al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="096ba-122">Use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory from the *ppDirtyRegion* array when you are finished with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="096ba-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="096ba-123">Requirements</span></span>



| <span data-ttu-id="096ba-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="096ba-124">Requirement</span></span> | <span data-ttu-id="096ba-125">Valore</span><span class="sxs-lookup"><span data-stu-id="096ba-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="096ba-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="096ba-126">Minimum supported client</span></span><br/> | <span data-ttu-id="096ba-127">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="096ba-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="096ba-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="096ba-128">Minimum supported server</span></span><br/> | <span data-ttu-id="096ba-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="096ba-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="096ba-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="096ba-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="096ba-131"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="096ba-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="096ba-132">DLL</span><span class="sxs-lookup"><span data-stu-id="096ba-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="096ba-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="096ba-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="096ba-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="096ba-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="096ba-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="096ba-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="096ba-136">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="096ba-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="096ba-137">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="096ba-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="096ba-138">**Metodo IInkAnalyzer:: AddStroke**</span><span class="sxs-lookup"><span data-stu-id="096ba-138">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="096ba-139">**Metodo IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="096ba-139">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="096ba-140">**Metodo IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="096ba-140">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="096ba-141">**Metodo IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="096ba-141">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="096ba-142">**Metodo IInkAnalyzer:: RemoveStroke**</span><span class="sxs-lookup"><span data-stu-id="096ba-142">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="096ba-143">**Metodo IInkAnalyzer:: RemoveStrokes**</span><span class="sxs-lookup"><span data-stu-id="096ba-143">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="096ba-144">**Metodo IInkAnalyzer:: UpdateStrokesData**</span><span class="sxs-lookup"><span data-stu-id="096ba-144">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="096ba-145">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="096ba-145">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

