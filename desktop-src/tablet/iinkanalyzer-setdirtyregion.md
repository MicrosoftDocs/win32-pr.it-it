---
description: Modifica l'area che è stata modificata dopo l'ultima operazione di analisi.
ms.assetid: 1484fd96-2791-4583-b13b-e5a8275ecb0e
title: 'Metodo IInkAnalyzer:: SetDirtyRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 72278dd9fe1d772d4ef340d25694d42f9c48ed7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129439"
---
# <a name="iinkanalyzersetdirtyregion-method"></a><span data-ttu-id="0f537-103">Metodo IInkAnalyzer:: SetDirtyRegion</span><span class="sxs-lookup"><span data-stu-id="0f537-103">IInkAnalyzer::SetDirtyRegion method</span></span>

<span data-ttu-id="0f537-104">Modifica l'area che è stata modificata dopo l'ultima operazione di analisi.</span><span class="sxs-lookup"><span data-stu-id="0f537-104">Modifies the area that has changed since the last analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f537-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f537-105">Syntax</span></span>


```C++
HRESULT SetDirtyRegion(
  [in] IAnalysisRegion *pDirtyRegion
);
```



## <a name="parameters"></a><span data-ttu-id="0f537-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f537-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f537-107">*pDirtyRegion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f537-107">*pDirtyRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f537-108">Oggetto [**IAnalysisRegion**](ianalysisregion.md) che descrive l'area modificata dall'ultima operazione di analisi.</span><span class="sxs-lookup"><span data-stu-id="0f537-108">An [**IAnalysisRegion**](ianalysisregion.md) that describes the area that has changed since the last analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f537-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f537-109">Return value</span></span>

<span data-ttu-id="0f537-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0f537-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0f537-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f537-111">Remarks</span></span>

<span data-ttu-id="0f537-112">Questo metodo identifica le aree che devono essere analizzate o rianalizzate.</span><span class="sxs-lookup"><span data-stu-id="0f537-112">This method identifies the areas that need to be analyzed or reanalyzed.</span></span> <span data-ttu-id="0f537-113">Tutti i metodi [**IInkAnalyzer**](iinkanalyzer.md) che aggiungono, aggiornano o rimuovono i dati del tratto aggiornano l'area dirty.</span><span class="sxs-lookup"><span data-stu-id="0f537-113">All of the [**IInkAnalyzer**](iinkanalyzer.md) methods that add, update, or remove stroke data update the dirty region.</span></span> <span data-ttu-id="0f537-114">Per contrassegnare manualmente un'area per la rianalisi:</span><span class="sxs-lookup"><span data-stu-id="0f537-114">To manually mark an area for reanalysis:</span></span>

1.  <span data-ttu-id="0f537-115">Ottenere l'area dirty usando il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md).</span><span class="sxs-lookup"><span data-stu-id="0f537-115">Get the dirty region using [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md).</span></span>
2.  <span data-ttu-id="0f537-116">Usare il metodo [**IAnalysisRegion:: UnionRegion**](ianalysisregion-unionregion.md) o [**IAnalysisRegion:: UnionRectangle**](ianalysisregion-unionrectangle.md) per aggiungere l'area all'area del passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="0f537-116">Use [**IAnalysisRegion::UnionRegion Method**](ianalysisregion-unionregion.md) or [**IAnalysisRegion::UnionRectangle Method**](ianalysisregion-unionrectangle.md) to add the area to the region from step 1.</span></span>
3.  <span data-ttu-id="0f537-117">Usare il **Metodo IInkAnalyzer:: SetDirtyRegion** per aggiornare l'area dirty.</span><span class="sxs-lookup"><span data-stu-id="0f537-117">Use **IInkAnalyzer::SetDirtyRegion Method** to update the dirty region.</span></span>

<span data-ttu-id="0f537-118">[**IInkAnalyzer**](iinkanalyzer.md) analizza l'input penna all'interno dell'area dirty durante una chiamata al metodo [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="0f537-118">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span> <span data-ttu-id="0f537-119">Tuttavia, **IInkAnalyzer** può espandere l'operazione di analisi per includere le aree adiacenti.</span><span class="sxs-lookup"><span data-stu-id="0f537-119">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f537-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f537-120">Requirements</span></span>



| <span data-ttu-id="0f537-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f537-121">Requirement</span></span> | <span data-ttu-id="0f537-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0f537-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f537-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f537-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0f537-124">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0f537-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0f537-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f537-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0f537-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0f537-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0f537-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f537-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f537-128"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0f537-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0f537-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0f537-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f537-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f537-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0f537-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f537-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f537-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="0f537-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="0f537-133">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="0f537-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="0f537-134">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="0f537-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="0f537-135">**Metodo IInkAnalyzer:: AddStroke**</span><span class="sxs-lookup"><span data-stu-id="0f537-135">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="0f537-136">**Metodo IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="0f537-136">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="0f537-137">**Metodo IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="0f537-137">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="0f537-138">**Metodo IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="0f537-138">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="0f537-139">**Metodo IInkAnalyzer:: RemoveStroke**</span><span class="sxs-lookup"><span data-stu-id="0f537-139">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="0f537-140">**Metodo IInkAnalyzer:: RemoveStrokes**</span><span class="sxs-lookup"><span data-stu-id="0f537-140">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="0f537-141">**Metodo IInkAnalyzer:: UpdateStrokesData**</span><span class="sxs-lookup"><span data-stu-id="0f537-141">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="0f537-142">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="0f537-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




