---
description: Recupera tutti gli oggetti IContextNode del tipo specificato che contengono i tratti specificati.
ms.assetid: c674a03b-841c-4a9c-8268-302bc4038934
title: 'Metodo IInkAnalyzer:: FindNodesOfTypeForStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dd98c72007a69521506e2be21ad10edeb46df27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307390"
---
# <a name="iinkanalyzerfindnodesoftypeforstrokes-method"></a><span data-ttu-id="f53b1-103">Metodo IInkAnalyzer:: FindNodesOfTypeForStrokes</span><span class="sxs-lookup"><span data-stu-id="f53b1-103">IInkAnalyzer::FindNodesOfTypeForStrokes method</span></span>

<span data-ttu-id="f53b1-104">Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) del tipo specificato che contengono i tratti specificati.</span><span class="sxs-lookup"><span data-stu-id="f53b1-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type that contain the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f53b1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f53b1-105">Syntax</span></span>


```C++
HRESULT FindNodesOfTypeForStrokes(
  [in]  const GUID          *pNodeType,
  [in]        ULONG         ulStrokeIdsCount,
  [in]        LONG          *plStrokeIds,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="f53b1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f53b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f53b1-107">*pNodeType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f53b1-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f53b1-108">Identificatore univoco globale (GUID) che specifica il tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="f53b1-108">The globally unique identifier (GUID) that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="f53b1-109">*ulStrokeIdsCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f53b1-109">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f53b1-110">Numero di identificatori di tratto passati.</span><span class="sxs-lookup"><span data-stu-id="f53b1-110">The number of stroke identifiers passed in.</span></span>

</dd> <dt>

<span data-ttu-id="f53b1-111">*plStrokeIds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f53b1-111">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f53b1-112">Matrice degli identificatori del tratto.</span><span class="sxs-lookup"><span data-stu-id="f53b1-112">An array of the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="f53b1-113">*ppContextNodesFound* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f53b1-113">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f53b1-114">Raccolta di oggetti [**IContextNode**](icontextnode.md) che contengono tutti i nodi di tipo *pNodeType* che contengono i tratti con identificatori nella matrice *plStrokeIds* .</span><span class="sxs-lookup"><span data-stu-id="f53b1-114">The collection of [**IContextNode**](icontextnode.md) objects that contain all the nodes of type *pNodeType* that contain the strokes with identifiers in the *plStrokeIds* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f53b1-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f53b1-115">Return value</span></span>

<span data-ttu-id="f53b1-116">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f53b1-116">For a description of return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f53b1-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f53b1-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="f53b1-118">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppContextNodesFound* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f53b1-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="f53b1-119">La proprietà *pNodeType* deve contenere un GUID dalle costanti dei [tipi di nodo di contesto](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="f53b1-119">The *pNodeType* property must contain a GUID from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="f53b1-120">Se il tipo di nodo specificato non è un nodo foglia, ma uno dei discendenti del nodo fa riferimento a un tratto nella raccolta Strokes, tale nodo viene aggiunto alla raccolta restituita.</span><span class="sxs-lookup"><span data-stu-id="f53b1-120">If the specified node type is not a leaf node, but one of the node's descendants references a stroke in the strokes collection, that node is added to the collection that is returned.</span></span>

<span data-ttu-id="f53b1-121">Se [**IInkAnalyzer**](iinkanalyzer.md) non contiene alcun [**IContextNode**](icontextnode.md), viene restituita una raccolta [**IContextNodes**](icontextnodes.md) vuota.</span><span class="sxs-lookup"><span data-stu-id="f53b1-121">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="f53b1-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f53b1-122">Requirements</span></span>



| <span data-ttu-id="f53b1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f53b1-123">Requirement</span></span> | <span data-ttu-id="f53b1-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f53b1-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f53b1-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f53b1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f53b1-126">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f53b1-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f53b1-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f53b1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f53b1-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f53b1-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f53b1-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f53b1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f53b1-130"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f53b1-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f53b1-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f53b1-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f53b1-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f53b1-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f53b1-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f53b1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f53b1-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="f53b1-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="f53b1-135">**Metodo IInkAnalyzer:: FindInkLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="f53b1-135">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="f53b1-136">**Metodo IInkAnalyzer:: FindInkLeafNodesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="f53b1-136">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="f53b1-137">**Metodo IInkAnalyzer:: FindLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="f53b1-137">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="f53b1-138">**Metodo IInkAnalyzer:: FindNode**</span><span class="sxs-lookup"><span data-stu-id="f53b1-138">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="f53b1-139">**Metodo IInkAnalyzer:: FindNodesOfType**</span><span class="sxs-lookup"><span data-stu-id="f53b1-139">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="f53b1-140">**Metodo IInkAnalyzer:: FindNodesOfTypeInSubTree**</span><span class="sxs-lookup"><span data-stu-id="f53b1-140">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="f53b1-141">**Metodo IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="f53b1-141">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="f53b1-142">**Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="f53b1-142">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="f53b1-143">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="f53b1-143">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

