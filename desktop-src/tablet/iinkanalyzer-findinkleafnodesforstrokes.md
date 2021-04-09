---
description: Recupera i nodi foglia dell'input penna che contengono i tratti specificati.
ms.assetid: d9ebc57d-63f5-4175-8bb6-a688b98823d4
title: 'Metodo IInkAnalyzer:: FindInkLeafNodesForStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d19bed823f5385533dfc938eb9f6013b4a5640c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879337"
---
# <a name="iinkanalyzerfindinkleafnodesforstrokes-method"></a><span data-ttu-id="98908-103">Metodo IInkAnalyzer:: FindInkLeafNodesForStrokes</span><span class="sxs-lookup"><span data-stu-id="98908-103">IInkAnalyzer::FindInkLeafNodesForStrokes method</span></span>

<span data-ttu-id="98908-104">Recupera i nodi foglia dell'input penna che contengono i tratti specificati.</span><span class="sxs-lookup"><span data-stu-id="98908-104">Retrieves the ink leaf nodes that contain the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="98908-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98908-105">Syntax</span></span>


```C++
HRESULT FindInkLeafNodesForStrokes(
  [in]  ULONG         ulStrokeIdsCount,
  [in]  LONG          *plStrokeIds,
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="98908-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="98908-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98908-107">*ulStrokeIdsCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98908-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98908-108">Numero di identificatori di tratto passati.</span><span class="sxs-lookup"><span data-stu-id="98908-108">The number of stroke identifiers passed in.</span></span>

</dd> <dt>

<span data-ttu-id="98908-109">*plStrokeIds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98908-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98908-110">Matrice degli identificatori del tratto.</span><span class="sxs-lookup"><span data-stu-id="98908-110">An array of the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="98908-111">*ppContextNodesFound* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="98908-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98908-112">Raccolta di oggetti [**IContextNode**](icontextnode.md) che contengono tutti i nodi foglia dell'input penna che contengono i tratti con identificatori nella matrice *plStrokeIds* .</span><span class="sxs-lookup"><span data-stu-id="98908-112">The collection of [**IContextNode**](icontextnode.md) objects that contain all the ink leaf nodes that contain the strokes with identifiers in the *plStrokeIds* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98908-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98908-113">Return value</span></span>

<span data-ttu-id="98908-114">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="98908-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="98908-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="98908-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="98908-116">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodesFound* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="98908-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="98908-117">I nodi foglia non contengono nodi figlio.</span><span class="sxs-lookup"><span data-stu-id="98908-117">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="98908-118">I nodi Ink contengono dati Stroke.</span><span class="sxs-lookup"><span data-stu-id="98908-118">Ink nodes contain stroke data.</span></span> <span data-ttu-id="98908-119">Esempi di nodi foglia input penna sono oggetti InkWord, InkDrawing, andInkBullet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="98908-119">Examples of ink leaf nodes are InkWord, InkDrawing, andInkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="98908-120">Per altre informazioni, vedere [tipi di nodo di contesto](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="98908-120">For more information, see [Context Node Types](context-node-types.md).</span></span>

<span data-ttu-id="98908-121">Se nessun nodo contiene i tratti specificati, viene restituita una raccolta [**IContextNodes**](icontextnodes.md) vuota.</span><span class="sxs-lookup"><span data-stu-id="98908-121">If no nodes contain the specified strokes, an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span> <span data-ttu-id="98908-122">Analogamente, se *ulStrokeIdsCount* è zero, viene restituita una raccolta **IContextNodes** vuota.</span><span class="sxs-lookup"><span data-stu-id="98908-122">Similarly, if *ulStrokeIdsCount* is zero, an empty **IContextNodes** collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="98908-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98908-123">Requirements</span></span>



| <span data-ttu-id="98908-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="98908-124">Requirement</span></span> | <span data-ttu-id="98908-125">Valore</span><span class="sxs-lookup"><span data-stu-id="98908-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98908-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98908-126">Minimum supported client</span></span><br/> | <span data-ttu-id="98908-127">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="98908-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="98908-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98908-128">Minimum supported server</span></span><br/> | <span data-ttu-id="98908-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="98908-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="98908-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98908-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="98908-131"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="98908-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="98908-132">DLL</span><span class="sxs-lookup"><span data-stu-id="98908-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98908-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98908-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="98908-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98908-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98908-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="98908-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="98908-136">**Metodo IInkAnalyzer:: FindInkLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="98908-136">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="98908-137">**Metodo IInkAnalyzer:: FindLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="98908-137">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="98908-138">**Metodo IInkAnalyzer:: FindNode**</span><span class="sxs-lookup"><span data-stu-id="98908-138">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="98908-139">**Metodo IInkAnalyzer:: FindNodesOfType**</span><span class="sxs-lookup"><span data-stu-id="98908-139">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="98908-140">**Metodo IInkAnalyzer:: FindNodesOfTypeForStrokes**</span><span class="sxs-lookup"><span data-stu-id="98908-140">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="98908-141">**Metodo IInkAnalyzer:: FindNodesOfTypeInSubTree**</span><span class="sxs-lookup"><span data-stu-id="98908-141">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="98908-142">**Metodo IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="98908-142">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="98908-143">**Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="98908-143">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="98908-144">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="98908-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

