---
description: Associa i tratti specificati a questo IContextNode.
ms.assetid: 5ce8893a-da59-4cec-a349-d5ffc4f43905
title: 'Metodo IContextNode:: sestrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be7fd1645af70e34c747894bc8ab4317b08e2d70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307416"
---
# <a name="icontextnodesetstrokes-method"></a><span data-ttu-id="0f6bd-103">Metodo IContextNode:: sestrokes</span><span class="sxs-lookup"><span data-stu-id="0f6bd-103">IContextNode::SetStrokes method</span></span>

<span data-ttu-id="0f6bd-104">Associa i tratti specificati a questo [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="0f6bd-104">Associates the specified strokes with this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f6bd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f6bd-105">Syntax</span></span>


```C++
HRESULT SetStrokes(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="0f6bd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f6bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f6bd-107">*ulStrokeIdsCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f6bd-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f6bd-108">Il numero di identificatori di tratto in *plStrokeIds*.</span><span class="sxs-lookup"><span data-stu-id="0f6bd-108">The number of stroke identifiers in *plStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="0f6bd-109">*plStrokeIds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f6bd-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f6bd-110">Identificatori dei tratti da associare a questo [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="0f6bd-110">The identifiers of the strokes to associate with this [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f6bd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f6bd-111">Return value</span></span>

<span data-ttu-id="0f6bd-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0f6bd-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0f6bd-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f6bd-113">Remarks</span></span>

<span data-ttu-id="0f6bd-114">Questo metodo non aggiorna l'area dirty dell'analizzatore di input penna (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="0f6bd-114">This method does not update the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="0f6bd-115">Utilizzare questo metodo quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="0f6bd-115">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="0f6bd-116">Utilizzare questo metodo per assegnare i dati del tratto a un nodo di contesto specifico.</span><span class="sxs-lookup"><span data-stu-id="0f6bd-116">Use this method to assign stroke data to a specific context node.</span></span> <span data-ttu-id="0f6bd-117">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con **IInkAnalyzer**, vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0f6bd-117">For more information about synchronizing your application data with the **IInkAnalyzer**, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="0f6bd-118">Se uno dei tratti specificati è già associato a [**IInkAnalyzer**](iinkanalyzer.md), questo metodo restituisce **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="0f6bd-118">If any of the specified strokes are already associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f6bd-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f6bd-119">Requirements</span></span>



| <span data-ttu-id="0f6bd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f6bd-120">Requirement</span></span> | <span data-ttu-id="0f6bd-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0f6bd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f6bd-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f6bd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0f6bd-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0f6bd-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0f6bd-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f6bd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0f6bd-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0f6bd-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0f6bd-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f6bd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f6bd-127"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0f6bd-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0f6bd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0f6bd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f6bd-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f6bd-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0f6bd-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f6bd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f6bd-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="0f6bd-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="0f6bd-132">**Metodo IInkAnalyzer:: AddStroke**</span><span class="sxs-lookup"><span data-stu-id="0f6bd-132">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="0f6bd-133">**Metodo IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="0f6bd-133">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="0f6bd-134">**Metodo IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="0f6bd-134">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="0f6bd-135">**Metodo IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="0f6bd-135">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="0f6bd-136">**Metodo IInkAnalyzer:: AddStrokesToCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="0f6bd-136">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="0f6bd-137">**Metodo IInkAnalyzer:: AddStrokeToCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="0f6bd-137">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="0f6bd-138">**Metodo IInkAnalyzer:: RemoveStroke**</span><span class="sxs-lookup"><span data-stu-id="0f6bd-138">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="0f6bd-139">**Metodo IInkAnalyzer:: RemoveStrokes**</span><span class="sxs-lookup"><span data-stu-id="0f6bd-139">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="0f6bd-140">**IContextNode::GetStrokeId**</span><span class="sxs-lookup"><span data-stu-id="0f6bd-140">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="0f6bd-141">**IContextNode:: GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="0f6bd-141">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="0f6bd-142">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="0f6bd-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




