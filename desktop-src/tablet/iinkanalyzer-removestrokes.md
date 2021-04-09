---
description: Rimuove i tratti specificati da IInkAnalyzer.
ms.assetid: ea7c8a9f-a427-4781-b5ba-97ffd983dbe5
title: 'Metodo IInkAnalyzer:: RemoveStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 00f065e01f9a4ff1459988d76fc9393ba24aa894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129450"
---
# <a name="iinkanalyzerremovestrokes-method"></a><span data-ttu-id="a558d-103">Metodo IInkAnalyzer:: RemoveStrokes</span><span class="sxs-lookup"><span data-stu-id="a558d-103">IInkAnalyzer::RemoveStrokes method</span></span>

<span data-ttu-id="a558d-104">Rimuove i tratti specificati da [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="a558d-104">Removes the specified strokes from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a558d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a558d-105">Syntax</span></span>


```C++
HRESULT RemoveStrokes(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes
);
```



## <a name="parameters"></a><span data-ttu-id="a558d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a558d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a558d-107">*ulStrokeIdCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a558d-107">*ulStrokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a558d-108">Il numero di identificatori di tratto in *plStrokes*.</span><span class="sxs-lookup"><span data-stu-id="a558d-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="a558d-109">*plStrokes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a558d-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a558d-110">Identificatori per i tratti da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a558d-110">The identifiers for the strokes to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a558d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a558d-111">Return value</span></span>

<span data-ttu-id="a558d-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a558d-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a558d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a558d-113">Remarks</span></span>

<span data-ttu-id="a558d-114">Questo metodo rimuove i dati del pacchetto per i riferimenti e ai tratti specificati da [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="a558d-114">This method removes the packet data for and references to the specified strokes from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="a558d-115">Questo metodo rimuove i tratti dal nodo di contesto foglia che fa riferimento ai tratti.</span><span class="sxs-lookup"><span data-stu-id="a558d-115">This method removes the strokes from the leaf context node that references the strokes.</span></span> <span data-ttu-id="a558d-116">Se un [**IContextNode**](icontextnode.md) non fa più riferimento ad alcun tratto, questo metodo elimina **IContextNode** e tutti gli oggetti **IContextNode** predecessore che non hanno più nodi figlio.</span><span class="sxs-lookup"><span data-stu-id="a558d-116">If any [**IContextNode**](icontextnode.md) no longer references any strokes, this method deletes the **IContextNode** and any ancestor **IContextNode** objects that no longer have any child nodes.</span></span>

<span data-ttu-id="a558d-117">Dopo la rimozione dei tratti da [**IContextNode**](icontextnode.md), questo metodo aggiorna l'area dirty dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) per includere il rettangolo di delimitazione dei tratti rimossi.</span><span class="sxs-lookup"><span data-stu-id="a558d-117">After this method removes the strokes from the [**IContextNode**](icontextnode.md), it updates the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) to include the bounding box of the removed strokes.</span></span>

<span data-ttu-id="a558d-118">Se un tratto identificato in *plStrokes* non è associato a [**IInkAnalyzer**](iinkanalyzer.md), questo metodo ignora l'identificatore.</span><span class="sxs-lookup"><span data-stu-id="a558d-118">If a stroke identified in *plStrokes* is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="a558d-119">Se nessuno dei tratti identificati in *plStrokes* è associato a Ink Analyzer, questo metodo restituisce senza aggiornare [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="a558d-119">If none of the strokes identified in *plStrokes* are associated with the ink analyzer, this method returns without updating the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="a558d-120">Questo metodo restituisce un codice di errore e quando *plStrokes* è null.</span><span class="sxs-lookup"><span data-stu-id="a558d-120">This method returns and error code when *plStrokes* is null.</span></span>

## <a name="requirements"></a><span data-ttu-id="a558d-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a558d-121">Requirements</span></span>



| <span data-ttu-id="a558d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a558d-122">Requirement</span></span> | <span data-ttu-id="a558d-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a558d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a558d-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a558d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a558d-125">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a558d-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a558d-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a558d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a558d-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a558d-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a558d-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a558d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a558d-129"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a558d-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a558d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a558d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a558d-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a558d-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a558d-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a558d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a558d-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a558d-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a558d-134">**Metodo IInkAnalyzer:: AddStroke**</span><span class="sxs-lookup"><span data-stu-id="a558d-134">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="a558d-135">**Metodo IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="a558d-135">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="a558d-136">**Metodo IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="a558d-136">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="a558d-137">**Metodo IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="a558d-137">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="a558d-138">**Metodo IInkAnalyzer:: RemoveStroke**</span><span class="sxs-lookup"><span data-stu-id="a558d-138">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="a558d-139">**Metodo IInkAnalyzer:: GetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="a558d-139">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="a558d-140">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="a558d-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




