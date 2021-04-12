---
description: Recupera tutti i nodi foglia.
ms.assetid: 5534053c-c5b9-4576-857f-c8af39e821a7
title: 'Metodo IInkAnalyzer:: FindLeafNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f923afe94c25e45dbcbfe79d554282b69ebec3a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526497"
---
# <a name="iinkanalyzerfindleafnodes-method"></a><span data-ttu-id="587fe-103">Metodo IInkAnalyzer:: FindLeafNodes</span><span class="sxs-lookup"><span data-stu-id="587fe-103">IInkAnalyzer::FindLeafNodes method</span></span>

<span data-ttu-id="587fe-104">Recupera tutti i nodi foglia.</span><span class="sxs-lookup"><span data-stu-id="587fe-104">Retrieves all of the leaf nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="587fe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="587fe-105">Syntax</span></span>


```C++
HRESULT FindLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="587fe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="587fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="587fe-107">*ppContextNodesFound* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="587fe-107">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="587fe-108">Puntatore alla raccolta [**IContextNodes**](icontextnodes.md) contenente tutti i nodi foglia.</span><span class="sxs-lookup"><span data-stu-id="587fe-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all leaf nodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="587fe-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="587fe-109">Return value</span></span>

<span data-ttu-id="587fe-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="587fe-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="587fe-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="587fe-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="587fe-112">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodesFound* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="587fe-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="587fe-113">I nodi foglia non contengono nodi figlio.</span><span class="sxs-lookup"><span data-stu-id="587fe-113">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="587fe-114">Esempi di nodi foglia input penna sono gli oggetti InkWord, TextWord, image, InkDrawing e InkBullet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="587fe-114">Examples of ink leaf nodes are InkWord, TextWord, Image, InkDrawing, and InkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="587fe-115">Per altre informazioni, vedere [tipi di nodo di contesto](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="587fe-115">For more information, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="587fe-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="587fe-116">Requirements</span></span>



| <span data-ttu-id="587fe-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="587fe-117">Requirement</span></span> | <span data-ttu-id="587fe-118">Valore</span><span class="sxs-lookup"><span data-stu-id="587fe-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="587fe-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="587fe-119">Minimum supported client</span></span><br/> | <span data-ttu-id="587fe-120">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="587fe-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="587fe-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="587fe-121">Minimum supported server</span></span><br/> | <span data-ttu-id="587fe-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="587fe-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="587fe-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="587fe-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="587fe-124"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="587fe-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="587fe-125">DLL</span><span class="sxs-lookup"><span data-stu-id="587fe-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="587fe-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="587fe-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="587fe-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="587fe-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="587fe-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="587fe-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="587fe-129">**Metodo IInkAnalyzer:: FindInkLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="587fe-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="587fe-130">**Metodo IInkAnalyzer:: FindInkLeafNodesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="587fe-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="587fe-131">**Metodo IInkAnalyzer:: FindNode**</span><span class="sxs-lookup"><span data-stu-id="587fe-131">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="587fe-132">**Metodo IInkAnalyzer:: FindNodesOfType**</span><span class="sxs-lookup"><span data-stu-id="587fe-132">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="587fe-133">**Metodo IInkAnalyzer:: FindNodesOfTypeForStrokes**</span><span class="sxs-lookup"><span data-stu-id="587fe-133">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="587fe-134">**Metodo IInkAnalyzer:: FindNodesOfTypeInSubTree**</span><span class="sxs-lookup"><span data-stu-id="587fe-134">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="587fe-135">**Metodo IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="587fe-135">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="587fe-136">**Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="587fe-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="587fe-137">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="587fe-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

