---
description: Rimuove il tratto specificato da IInkAnalyzer.
ms.assetid: e182ae35-854e-401d-8e26-aee645c05430
title: 'Metodo IInkAnalyzer:: RemoveStroke (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 03952e6e14679c53f7b65f21463fc0457f302b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526485"
---
# <a name="iinkanalyzerremovestroke-method"></a><span data-ttu-id="072c3-103">Metodo IInkAnalyzer:: RemoveStroke</span><span class="sxs-lookup"><span data-stu-id="072c3-103">IInkAnalyzer::RemoveStroke method</span></span>

<span data-ttu-id="072c3-104">Rimuove il tratto specificato da [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="072c3-104">Removes the specified stroke from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="072c3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="072c3-105">Syntax</span></span>


```C++
HRESULT RemoveStroke(
  [in] LONG *plStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="072c3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="072c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="072c3-107">*plStrokeId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="072c3-107">*plStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="072c3-108">Identificatore del tratto.</span><span class="sxs-lookup"><span data-stu-id="072c3-108">The stroke identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="072c3-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="072c3-109">Return value</span></span>

<span data-ttu-id="072c3-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="072c3-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="072c3-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="072c3-111">Remarks</span></span>

<span data-ttu-id="072c3-112">Questo metodo rimuove i dati del pacchetto per e i riferimenti a, il tratto specificato da [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="072c3-112">This method removes the packet data for, and references to, the specified stroke from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="072c3-113">Questo metodo rimuove il tratto dal nodo di contesto foglia che fa riferimento al tratto.</span><span class="sxs-lookup"><span data-stu-id="072c3-113">This method removes the stroke from the leaf context node that references the stroke.</span></span> <span data-ttu-id="072c3-114">Se [**IContextNode**](icontextnode.md) non fa più riferimento ad alcun tratto, questo metodo elimina **IContextNode** e tutti gli oggetti **IContextNode** predecessore che non hanno più nodi figlio.</span><span class="sxs-lookup"><span data-stu-id="072c3-114">If the [**IContextNode**](icontextnode.md) no longer references any strokes, this method deletes the **IContextNode** and any ancestor **IContextNode** objects that no longer have any child nodes.</span></span>

<span data-ttu-id="072c3-115">Dopo la rimozione del tratto da [**IContextNode**](icontextnode.md), questo metodo aggiorna l'area dirty dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) per includere il rettangolo di delimitazione del tratto rimosso.</span><span class="sxs-lookup"><span data-stu-id="072c3-115">After this method removes the stroke from the [**IContextNode**](icontextnode.md), it updates the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) to include the bounding box of the removed stroke.</span></span>

<span data-ttu-id="072c3-116">Se *plStrokeId* non identifica un tratto associato a [**IInkAnalyzer**](iinkanalyzer.md), questo metodo restituisce senza aggiornare Ink Analyzer.</span><span class="sxs-lookup"><span data-stu-id="072c3-116">If *plStrokeId* does not identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the ink analyzer.</span></span>

## <a name="requirements"></a><span data-ttu-id="072c3-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="072c3-117">Requirements</span></span>



| <span data-ttu-id="072c3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="072c3-118">Requirement</span></span> | <span data-ttu-id="072c3-119">Valore</span><span class="sxs-lookup"><span data-stu-id="072c3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="072c3-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="072c3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="072c3-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="072c3-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="072c3-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="072c3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="072c3-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="072c3-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="072c3-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="072c3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="072c3-125"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="072c3-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="072c3-126">DLL</span><span class="sxs-lookup"><span data-stu-id="072c3-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="072c3-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="072c3-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="072c3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="072c3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="072c3-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="072c3-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="072c3-130">**Metodo IInkAnalyzer:: AddStroke**</span><span class="sxs-lookup"><span data-stu-id="072c3-130">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="072c3-131">**Metodo IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="072c3-131">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="072c3-132">**Metodo IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="072c3-132">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="072c3-133">**Metodo IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="072c3-133">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="072c3-134">**Metodo IInkAnalyzer:: RemoveStrokes**</span><span class="sxs-lookup"><span data-stu-id="072c3-134">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="072c3-135">**Metodo IInkAnalyzer:: GetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="072c3-135">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="072c3-136">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="072c3-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




